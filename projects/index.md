# Projects


<link rel="stylesheet" href="/projects.css">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<!-- {{< image width=100% src="/img/projects/penn-cloud/featured-image-alt1.JPG" >}} -->

<!-- Page Container -->
<div class="w3-content w3-margin-top" style="max-width:1400px;">

<p style="color:inherit;font-size:14px;margin-top: 1.0em;margin-bottom: 2.0em"><i class="fa fa-tags fa-fw"></i> <b>Categories:</b>&nbsp;&nbsp;<button class="button button1"><b><a href="/tags/distributed-systems" style="color:inherit;">Distributed Systems</a></b></button>&nbsp;&nbsp;<button class="button button1"><b><a href="/tags/deep-learning" style="color:inherit;">Deep Learning</a></b></button>&nbsp;&nbsp;<button class="button button1"><b><a href="/tags/computer-vision" style="color:inherit;">Computer Vision</a></b></button>&nbsp;&nbsp;<button class="button button1"><b><a href="/tags/natural-language-processing" style="color:inherit;">Natural Language Processing</a></b></button>

<!-- The Grid -->
<div class="w3-row-padding">

<div class="w3-half">
<!-- <div class="w3-col"> -->
<div class="w3-container w3-card w3-margin-bottom w3-border w3-round w3-hover-border-cyan">
<!-- <div class="w3-panel w3-border w3-round w3-hover-border-cyan"> -->
<div class="w3-container">
<p style="text-align:left;font-size:36px;margin-top: 0.55em;margin-bottom: 0.5em"><a href="/penn-cloud/"><i class="fa fa-folder-o fa-fw"></i></a>
	<span style="float:right;color:darkgray;font-size:20px">
    	<!-- <a href="/penn-cloud/"><i class="fa fa-external-link fa-fw"></i></a> -->
    	<i class="fa fa-github fa-fw"></i>
    	<i class="fa fa-file-pdf-o fa-fw"></i>
    	<a href="/penn-cloud/"><i class="fa fa-external-link-square fa-fw"></i></a>
	</span></p>
<!-- <p style="color:darkgray;font-size:14px;margin-top: 2.0em;margin-bottom: -0.5em">December 2021</p> -->
<h3><a href="/penn-cloud/" style="color: inherit;font-size:18px">PennCloud: Distributed Cloud Platform</a></h3>
<!-- <p style="color:darkgray;font-size:15px;margin-top: -0.5em"><i class="fa fa-user-circle fa-fw"></i><a href="/"> Roy Wu</a>, Thomas Donnelly, Katrina Ashton, Jacob Glenn</p> -->
<p style="color:gray;font-size:14px;margin-top: -0.75em">This repository contains implementation of a distributed software system. The goal is to design a small clone of Google Apps that primary consists of just two key apps: webmail and storage (similar to Gmail and Google Drive) and leaves out other fancy optics. The key components includes a web frontend and a key-value store backend.</p>
<!-- <p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.75em;margin-bottom: -0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/distributed-systems/" style="color:inherit;"> Distributed Systems</a>
	<span style="float:left;font-family:monospace;color:darkgray;font-size:14px">
        C++&nbsp;&nbsp;&nbsp;HTML
    </span></p><br> -->
<p style="font-family:monospace;color:darkgray;font-size:14px">C++&nbsp;&nbsp;&nbsp;HTML</p>
<p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.5em;margin-bottom: 1.75em"><i class="fa fa-tags fa-fw"></i><a href="/tags/distributed-systems/" style="color:inherit;"> Distributed Systems</a></p>
<!-- <p style="text-align: right;color:inherit;font-size:13px;margin-top: -1.0em;margin-bottom: 0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/distributed-systems/" style="color:inherit;"> Distributed Systems</a></p> -->
<!-- <a href="/penn-cloud/" style="color:inherit;"><button class="button button2"><b>blog</b></button></a> 
<button class="button button4"><b><span style="color:lightgray;">paper</span></b></button>
<button class="button button4"><b><span style="color:lightgray;">code</span></b></button> -->
<!-- <br><br> -->
<!-- <hr> -->
</div>
</div>
</div>

<div class="w3-half">
<!-- <div class="w3-col"> -->

<div class="w3-container w3-card w3-margin-bottom w3-border w3-round w3-hover-border-cyan">
<!-- <div class="w3-panel w3-border w3-round w3-hover-border-cyan"> -->
<div class="w3-container">
<p style="text-align:left;font-size:36px;margin-top: 0.55em;margin-bottom: 0.5em"><a href="/chat-server"><i class="fa fa-folder-o fa-fw"></i></a>
	<span style="float:right;color:darkgray;font-size:20px">
    	<!-- <a href="/artificial-anime-character-design/"><i class="fa fa-external-link fa-fw"></i></a> -->
<!--     	<a href=""><i class="fa fa-github fa-fw"></i></a>
    	<a href=""><i class="fa fa-file-pdf-o fa-fw"></i></a>
    	<a href=""><i class="fa fa-external-link-square fa-fw"></i></a> -->
    	<i class="fa fa-github fa-fw"></i>
    	<i class="fa fa-file-pdf-o fa-fw"></i>
    	<a href="/chat-server/"><i class="fa fa-external-link-square fa-fw"></i></a>
	</span></p>
<!-- <p style="color:darkgray;font-size:14px;margin-top: 2.0em;margin-bottom: -0.5em">May 2020</p> -->
<h3><a href="/chat-server/" style="color: inherit;font-size:18px">Chat Room: Replicated Chat Server With Multicast</a></h3>
<!-- <p style="color:darkgray;font-size:15px;margin-top: -0.5em"><i class="fa fa-user-circle fa-fw"></i><a href="/"> Roy Wu</a>, Henglin Wu, Ruilin Zhao, Chenyuan Li</p> -->
<p style="color:gray;font-size:14px;margin-top: -0.75em">This repository contains implementation of a simple replicated chat server that uses multicast to distribute the chat messages to the different replicas. The servers have the option to deliver
clients’ messages following three different types of ordering protocols: Unordered, FIFO, or total. All communications are done via unicast UDP.</p>
<!-- <p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.75em;margin-bottom: -0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/computer-vision/" style="color: inherit;"> Computer Vision</a>
	<span style="float:left;font-family:monospace;color:darkgray;font-size:14px">
        Python&nbsp;&nbsp;&nbsp;PyTorch
    </span></p><br> -->
<p style="font-family:monospace;color:darkgray;font-size:14px">C/C++</p>
<p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.5em;margin-bottom: 1.75em"><i class="fa fa-tags fa-fw"></i><a href="/tags/distributed-systems/" style="color:inherit;"> Distributed Systems</a></p>  
<!-- <p style="text-align: right;color:inherit;font-size:13px;margin-top: -1.0em;margin-bottom: 0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/natural-language-processing/" style="color:inherit;"> Natural Language Processing</a></p> -->
<!-- <a href="/artificial-anime-character-design/" style="color:inherit;"><button class="button button2"><b>blog</b></button></a> 
<a href="/artificial-anime-character-design/report.pdf" style="color:inherit;" target="_blank"><button class="button button2"><b>paper</b></button></a> 
<a href="https://github.com/roynwu/Artificial-Anime-Character-Design" style="color:inherit;" target="_blank"><button class="button button2"><b>code</b></button></a> 
<br><br> -->
<!-- <hr> -->
</div>
</div>
</div>
</div>

<!-- The Grid -->
<div class="w3-row-padding">

<!-- <div class="w3-col"> -->
<div class="w3-half">
<div class="w3-container w3-card w3-margin-bottom w3-border w3-round w3-hover-border-cyan">
<!-- <div class="w3-panel w3-border w3-round w3-hover-border-cyan"> -->
<div class="w3-container">
<p style="text-align:left;font-size:36px;margin-top: 0.55em;margin-bottom: 0.5em"><a href="/headline-writer/"><i class="fa fa-folder-o fa-fw"></i></a>
	<span style="float:right;color:darkgray;font-size:20px">
    	<!-- <a href="/headline-writer/"><i class="fa fa-external-link fa-fw"></i></a> -->
    	<a href="https://github.com/roynwu/Headline-Writer"><i class="fa fa-github fa-fw"></i></a>
    	<a href="/headline-writer/report.pdf"><i class="fa fa-file-pdf-o fa-fw"></i></a>
    	<a href="/headline-writer/"><i class="fa fa-external-link-square fa-fw"></i></a>
	</span></p>
<!-- <p style="color:darkgray;font-size:14px;margin-top: 2.0em;margin-bottom: -0.5em">May 2020</p> -->
<h3><a href="/headline-writer/" style="color: inherit;font-size:18px">Headline-Writer: Abstractive Text Summarization</a></h3>
<!-- <p style="color:darkgray;font-size:15px;margin-top: -0.5em"><i class="fa fa-user-circle fa-fw"></i><a href="/"> Roy Wu</a>, Henglin Wu, Ruilin Zhao, Chenyuan Li</p> -->
<p style="color:gray;font-size:14px;margin-top: -0.75em">This repository contains implementations of Sequence-to-sequence (Seq2Seq) neural networks for abstractive text summarization. We implement Attention mechanism, Teacher Forcing algorithm, and Pointer-Generator Network (inspired by <a href="https://arxiv.org/abs/1704.04368">Get To The Point: Summarization with Pointer-Generator Networks</a>) in our experiment.</p>
<!-- <p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.75em;margin-bottom: -0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/natural-language-processing/" style="color:inherit;"> Natural Language Processing</a>
	<span style="float:left;font-family:monospace;color:darkgray;font-size:14px">
        Python&nbsp;&nbsp;&nbsp;PyTorch
    </span></p><br> -->
<p style="font-family:monospace;color:darkgray;font-size:14px">Python&nbsp;&nbsp;&nbsp;PyTorch</p>
<p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.5em;margin-bottom: 1.75em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/natural-language-processing/" style="color:inherit;"> Natural Language Processing</a></p>
<!-- <p style="text-align: right;color:inherit;font-size:13px;margin-top: -1.0em;margin-bottom: 0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/natural-language-processing/" style="color:inherit;"> Natural Language Processing</a></p> -->
<!-- <a href="/headline-writer/" style="color:inherit;"><button class="button button2"><b>blog</b></button></a> 
<a href="/headline-writer/report.pdf" style="color:inherit;" target="_blank"><button class="button button2"><b>paper</b></button></a> 
<a href="https://github.com/roynwu/Headline-Writer" style="color:inherit;" target="_blank"><button class="button button2"><b>code</b></button></a> 
<br><br> -->
<!-- <hr> -->
</div>
</div>
</div>

<!-- <div class="w3-col"> -->
<div class="w3-half">
<div class="w3-container w3-card w3-margin-bottom w3-border w3-round w3-hover-border-cyan">
<!-- <div class="w3-panel w3-border w3-round w3-hover-border-cyan"> -->
<div class="w3-container">
<p style="text-align:left;font-size:36px;margin-top: 0.55em;margin-bottom: 0.5em"><a href="/artificial-anime-character-design/"><i class="fa fa-folder-o fa-fw"></i></a>
	<span style="float:right;color:darkgray;font-size:20px">
    	<!-- <a href="/artificial-anime-character-design/"><i class="fa fa-external-link fa-fw"></i></a> -->
    	<a href="https://github.com/roynwu/Artificial-Anime-Character-Design"><i class="fa fa-github fa-fw"></i></a>
    	<a href="/artificial-anime-character-design/report.pdf"><i class="fa fa-file-pdf-o fa-fw"></i></a>
    	<a href="/artificial-anime-character-design/"><i class="fa fa-external-link-square fa-fw"></i></a>
	</span></p>
<!-- <p style="color:darkgray;font-size:14px;margin-top: 2.0em;margin-bottom: -0.5em">May 2020</p> -->
<h3><a href="/artificial-anime-character-design/" style="color: inherit;font-size:18px">Anime Character Design: Generative Adversarial Networks</a></h3>
<!-- <p style="color:darkgray;font-size:15px;margin-top: -0.5em"><i class="fa fa-user-circle fa-fw"></i><a href="/"> Roy Wu</a>, Henglin Wu, Ruilin Zhao, Chenyuan Li</p> -->
<p style="color:gray;font-size:14px;margin-top: -0.75em">Generative Adversarial Network (GAN) is a framework for deep learning models to generate superficial data. This repository contains implementations of GANs to design and generate new face images of anime characters. A few improvement techniques were implemented to enhance model performance and output quality.</p>
<!-- <p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.75em;margin-bottom: -0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/computer-vision/" style="color: inherit;"> Computer Vision</a>
	<span style="float:left;font-family:monospace;color:darkgray;font-size:14px">
        Python&nbsp;&nbsp;&nbsp;PyTorch
    </span></p><br> -->
<p style="font-family:monospace;color:darkgray;font-size:14px">Python&nbsp;&nbsp;&nbsp;PyTorch</p>
<p style="text-align:right;font-family:inherit;color:inherit;font-size:13px;margin-top: 0.5em;margin-bottom: 1.75em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/computer-vision/" style="color:inherit;"> Computer Vision</a></p>    
<!-- <p style="text-align: right;color:inherit;font-size:13px;margin-top: -1.0em;margin-bottom: 0.25em"><i class="fa fa-tags fa-fw"></i><a href="/tags/deep-learning/" style="color:inherit;"> Deep Learning</a>,<a href="/tags/natural-language-processing/" style="color:inherit;"> Natural Language Processing</a></p> -->
<!-- <a href="/artificial-anime-character-design/" style="color:inherit;"><button class="button button2"><b>blog</b></button></a> 
<a href="/artificial-anime-character-design/report.pdf" style="color:inherit;" target="_blank"><button class="button button2"><b>paper</b></button></a> 
<a href="https://github.com/roynwu/Artificial-Anime-Character-Design" style="color:inherit;" target="_blank"><button class="button button2"><b>code</b></button></a> 
<br><br> -->
<!-- <hr> -->
</div>
</div>
</div>
</div>

<!-- End Grid -->
</div>

<!-- End Page Container -->
</div>

<!-- {{< image width=100% src="/img/projects/penn-cloud/featured-image-alt1.JPG" >}} -->

<footer class="w3-container w3-center w3-margin-top">
  <i class="fa fa-test w3-hover-opacity"></i>
  <p style="font-size:14px;margin-top:1.05em">&nbsp;</p>
  <br><br>
</footer>
