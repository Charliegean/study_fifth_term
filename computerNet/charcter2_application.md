---


---

<h1 id="application">application</h1>
<h4 id="charliegean-2018-10-30">charliegean 2018-10-30</h4>
<ol>
<li>网路应用的架构：其规定了在各个段系统上组织应用程序的方法，具体包括客户-服务器架构，对等架构。</li>
<li>客户-服务器架构：服务器（一台总在线的运行着服务程序的主机，具有永久的IP地址，使用主机集群或者数据中心提高处理能力），客户机：（需要时与服务器通信，可能间断的连接到网络上，使用动态的IP地址，不与其他客户机直接通信）。</li>
<li>P2P架构：没有总运行的服务器，任意一对端系统（对等方）可以直接通信，对等方使用动态IP间接连接，每个对等方可以请求服务以及提供服务。</li>
<li>进程通过套接字发送和接收报文，套接字是进程与网络的接口，也是应用层和传输层的接口，同时是应用程序和网络之间的API。</li>
<li>进程编址：为了接收报文，每个进程必须有标识，主机使用IP地址进行标识。一般使用端口号区分同一个主机上的不同进程。进程标识包括：IP地址和与该进程有关的端口号。</li>
<li>因特网提供的传输服务包括TCP和UDP。TCP包括面向连接（客户进程与服务器进程需要建立连接），可靠传输（发送进程与接收进程之间可靠传输），流量控制（发送进程不至于压垮接收进程），拥塞控制（网络超载时抑制发送进程），不提供及时性和最低带宽保证。UDP是发送进程和接收进程之间不可靠传输，不提供：连接建立、可靠传输、流量控制、拥塞控制、及时性、最低带宽保证。</li>
<li>应用层协议定义了交换的报文类型、报文语法（报文中的字段及其描述）、报文语义（各自段信息的含义）、进程何时及如何发送/响应报文的规则。</li>
<li>RTT（round-trip Time）：一个小分组从客户发送到服务器在返回客户的时间）。对于非持久HTTP的响应时间：建立TCP连接用时一个RTT，发送HTTP请求至收到相应的前几个字节用时一个RTT）。下载一个对象的时间=2RTT+对象传输的时间。下在一个网页的时间=下载一个对象的时间*对象的个数</li>
<li>HTTP报文格式：请求报文和响应报文。请求报文的报头包括：请求行、首部行和一个额外的回车换行（表示报头结束）。响应报文：状态行、首部行和数据。</li>
<li>HTTP响应状态代码：200 OK（request succeeded, requested object later in this message）<br>
301 Moved Permanently（requested object moved, new location specified later in this message 【Location:】）、400 Bad Request（request message not understood by server）、404 Not Found（requested document not found on this server）505 HTTP Version Not Supported。</li>
<li>代理服务器：代表原始服务器满足HTTP请求的网络实体，保存最近请求过的对象的拷贝。</li>
<li>web缓存：既是服务器也是客户机，减少客户请求的响应时间，减少机构接入链路上的流量。</li>
<li></li>
</ol>

