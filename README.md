# 内网穿透小工具（golang源码）
### 源码下载地址：
https://www.wwwoop.com/home/Index/projectInfo?goodsId=37&typeParam=2

### 什么是内网穿透？如何实现？
#### 1、什么是内网穿透？
内网穿透是一种技术，通过使用一台具备公网 IP 的服务器，将你的内网服务暴露到公网中，使得其他人在公网可以直接访问你的内网服务。简单来说，它是将家中或公司内部网络中的服务映射到互联网的桥梁。

#### 2、场景需求
假设你在家中的电脑上搭建了一个网站，但这个网站只能在本地访问。现在，你希望通过任何电脑的浏览器都能访问这个网站，这时候就需要用到内网穿透技术！

#### 3、实现内网穿透需要具备的条件
#### ① 一台具备公网 IP 的服务器
这台服务器是关键，用于接收来自公网的请求并转发到你的内网

#### ②家中的电脑（Windows 10 系统）
你的内网服务需要运行在这台电脑上，比如网站或其他服务

#### ③内网穿透软件
内网穿透软件通常分为两个端：

o 服务端：运行在具备公网 IP 的服务器上，用于监听和转发请求

o 客户端：运行在家中的电脑上，与服务端保持连接，确保内网服务可被访问

#### 4、个人实现：基于 Golang 的内网穿透代码
使用 Golang 语言实现内网穿透非常高效，以下是一个简单的示例代码供大家学习和参考：

服务端代码 
![image](https://github.com/user-attachments/assets/a291780c-0ad0-4bb2-8573-38b54076473d)

客户端代码
![image](https://github.com/user-attachments/assets/54af4d76-f19b-4c63-afd3-32e1fcb0d0ba)

#### 5、如何编译为 Windows 和 Linux 可执行文件？

为了在不同系统中运行内网穿透程序，你需要将代码编译成对应平台的可执行文件。以下是具体命令：

#### 编译为 64 位 Linux 可执行文件
1.打开命令提示符（cmd）

2.执行以下命令

set GOARCH=amd64

set GOOS=linux

go build -o myapp main.go

#### 编译为 64 位 Windows 可执行文件
1.打开命令提示符（cmd）

2.执行以下命令：

set GOARCH=amd64

set GOOS=windows

go build -o myapp.exe main.go

通过内网穿透技术，即使你的内网服务无法直接暴露在公网中，也可以轻松让他人访问。你只需要准备一台公网服务器和内网穿透工具即可快速实现。以上代码和教程仅供参考，欢迎大家尝试实现自己的内网穿透工具！

### 更多资料获取：
https://www.wwwoop.com/

微信公众号：万物oop
