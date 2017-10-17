# HTTP协议

## 一、网络基础

### 1、TCP/IP协议族各层作用

#### 应用层

决定了向用户提供应用服务时通信的活动

比如：FTP、DNS、HTTP

#### 传输层

提供数据传输

比如：TCP、UDP

#### 网络层

处理在网络上流动的数据包（网络传输最小单位）

比如IP协议

#### 链路层

用来处理连接网络的硬件部分

### 2、TCP/IP 通信传输流

发送端从应用层往下走，接收端则往应用层往上走

发送端每经过一层打上一个该层的首部信息  -》 封装

接收端每经过一层把首部信息消去

### 3、关系密切的IP、TCP、DNS协议

```sh

IP协议的作用是把各种数据包传送给对方。 IP地址和MAC地址。 ARP协议（解析地址的协议)。

TCP协议把数据准确的传给对方，可以分割大数据。 为了准确传输，采用三次握手策略。

*三次握手
发送端发送一个带有SYN标志的数据包给对方
接收端收到后，回传一个带有SYN/ACK标志的数据包表示确认信息
发送端再回传一个ACK标志的数据包，代表握手结束

DNS服务提供域名到IP地址之间的解析服务  发送端发送http://t66y.com/，DNS解析对应一个IP地址，然后访问服务器

```

### 4、URI和URL

http://t66y.com/index.php  => URI
http://t66y.com/ => URL

## 二、简单的HTTP协议

客户端：请求访问文本或图像等资源的一端
服务端：提供资源响应的一端

### 1、通过请求和响应的交换达成通信

请求报文是由请求方法、请求URI、协议版本、可选的请求首部字段和内容实体构成

响应报文是由协议版本、状态码、状态码的原因短语、可选的响应首部字段和主体构成
