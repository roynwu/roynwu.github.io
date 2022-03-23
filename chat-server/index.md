# Chat Room: Replicated Chat Server With Multicast


This repository contains implementation of a simple replicated chat server that uses multicast to distribute the chat messages to the different replicas. The servers have the option to deliver clients’ messages following three different types of ordering protocols: Unordered, FIFO, or total. All communications are done via unicast UDP.

<!-- [**[paper](report.pdf)**] [**[code](https://github.com/roynwu/Artificial-Anime-Character-Design)**] -->

### Overview

The figure below shows a sketch of the system. There are two kinds of processes: servers (represented by orange squares) and clients (represented by yellow circles). Each client is connected to one of the servers, and each server is connected to all the
other servers. The clients and servers can all run on different machines, or (e.g., for testing) they can all run on the same machine.
<br/>
{{< image width="425" src="/img/projects/chat-server/architecture_diagram.png" caption="Sketch of system" >}}
The system provides different chat rooms. Clients can join one of the chat rooms and then post messages, which should be delivered to all the other clients that are currently in the same chat room. If there was only a single server, this would be easy: the server would simply send each message it receives to all the clients who are currently in the relevant room. However,
since there can be multiple servers, this simple approach does not work. Instead, the servers will internally use multicast to deliver the messages. 

To make this a little more concrete, consider the following example. In the figure, client D is connected to server S3. Suppose D joins chat room #3, which already contains A and B, and posts a message there (say, "Hello"). S3 then multicasts D's message to multicast group #3, so it will be delivered to the other servers. (All servers are members of all multicast groups.) The servers then forward D's message to all of the clients that are currently in chat room #3. In this case, S3 will echo it back to D, and S1 will send it to A and B. S2 does not currently have any clients that are in chat room #3, so it ignores the message.

The servers should support three different ordering modes:

1. **Unordered multicast:** Each server delivers the messages to its clients in whatever order the server
happens to receive it

2. **FIFO multicast:** The messages from a given client C should be delivered to the other clients in the
order they were sent by C

3. **Totally ordered multicast** The messages in a given chat room should be delivered to all the clients
in that room in the same order

The system is fully distributed; in other words, there should not be any central ‘sequencing nodes’. All communication, both between clients and servers and among the servers are via unicast UDP (and not using the OS's built-in multicast primitive). There is an assumption that there is no message loss, and that the messages between servers and clients are not reordered. 

### Specification

#### The Client

The user can invoke the client from the command line with the IP address and port (i.e., the bind address) of a particular server as a parameter. Note that each client is connected to exactly one server. The user can then be able to type lines of text (commands or chat messages), and, whenever the user has entered a new line, the chat client can send the line to the server in a single UDP packet (without any trailing CR or LF). The client also listens for UDP packets from the server; whenever it
receives such a packet, it prints its contents to the terminal.

#### Commands

When the server receives a line of text from the user, it checks whether it begins with a forward slash (/). If not, the server considers the line to be a chat message; otherwise, it treats it as a command. The following commands are supported:

1. /join \<roomID\>: Used to join a particular chat room (Example: /join 7). The roomID is an integer in the set {1, 2, …, N}, where N is the total number of chat rooms. It supports at least N = 10 chat rooms (i.e., with room IDs 1,2,3,...,10). If the command succeeds, the server responds with a line that starts with +OK (Example: +OK You are now in chat room #7). If the user tries to join more than one chat room at a time, or if the specified chat room does not exist (e.g., the specified room is outside your supported range of room IDs), the server responds with a line that starts with -ERR (Example: -ERR You are already in room #9).

2. /part: Used to leave the current chat room. If successful, the server sends a response that starts with +OK (Example: +OK You have left chat room #7). If the user is not currently in a chat room, the server sends a response that starts with -ERR.

3. /nick: Used to set the user's nickname (Example: /nick Linh). The server responds with a line that starts with +OK. If the user does not explicitly set a nickname, the server uses its IP and port (Example: 127.0.0.1:5005). If the /nick command is used more than once, the server uses the latest nickname. 

4. /quit: When the user enters this special command, the chat client sends the command to the server and then terminate. The server removes the chat client from its list of active clients. 

If the user sends a text message without having joined a chat room, the server responds with a line that starts with -ERR. Each client cannot be in more than one chat room at a time. Each text message sent by the user is at most 1000 bytes. If the user
terminates the client using CTRL+C, the client behaves in the same way as if it has received a /quit command. If the user enters an invalid command, i.e., the text begins with “/” but does not fall into the above commands, the client responds with a line that starts with -ERR.

Below is an example session (the lines in bold are typed by the user):
<br/><br/>
{{< image width="500" src="/img/projects/chat-server/example_session.png" caption="Example session" >}}

#### The Server

This implementation assumes static membership: each server will have access to a configuration file that contains the addresses of all the servers in the system. 

Each server will have two potentially different addresses. The first is the forwarding address: this is the IP and port number that other servers use as the destination address when they want to send a message to this server. The second is the bind address: this is the IP and port number on which the server listens for UDP messages from clients and from other servers; it is the address that the server binds to, and also the address that its clients connect to.

The server program requires two command-line arguments. The first is the name of a configuration file that contains the forwarding address and the bind address of all the server instances, and the second is the index of the current server instance in this list. The file should contain one line for each server instance. If the line contains only one IP address and port number (Example: 127.0.0.1:5000), this address serves as both the forwarding address and the bind address for that server. If the line contains two IPs and port numbers separated by a comma (Example: 127.0.0.1:8001,127.0.0.1:5001), the first address is the forwarding address and the second is the bind address. The index of the first server is 1.

For instance, suppose the file foo.txt contains the following lines:
<br/><br/>
{{< image width="350" src="/img/projects/chat-server/example_file.png" caption="Example file" >}}

and the server is invoked like this: chatserver foo.txt 2, then the server listens for (all) messages on its bind address, i.e., on 127.0.0.1:5001. When it has a message for the third server, it sends the message to (the third server’s forwarding address) 127.0.0.1:8002, and when it has a message for the first server, it sends the message to (the first server’s forwarding address)
127.0.0.1:8000. In addition, the user would invoke a client of the server using the server’s bind address – e.g., a client of the second server can be invoked like this: chatclient 127.0.0.1:5001.

The server also accepts a option -o on the command line. The -o option is used to select an ordering mode: choices are -o unordered (the default), -o fifo, and -o total.

This implementation is able to support at least 10 servers, with up to 250 clients in total.
