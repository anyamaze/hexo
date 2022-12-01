# hexo
hexo相关使用教程
博客网站的实现方法有很多种，常用的博客框架主要有wordpress、Z-Blog、hexo、Typecho、Halo等。



Hexo官网：https://hexo.io/zh-cn/

Hexo是快速、简洁且高效的博客框架，通过Hexo可完成博客网站的快速搭建。Hexo有多种博客主题供选择，用户也可自定义博客主题。



Hexo博客框架特点：

- **超快速度**

  Node.js 所带来的超快生成速度，让上百个页面在几秒内瞬间完成渲染。

- **支持 Markdown**

  Hexo 支持 GitHub Flavored Markdown 的所有功能，甚至可以整合 Octopress 的大多数插件。

- **一键部署**

  只需一条指令即可部署到 GitHub Pages, Heroku 或其他平台。

- **插件和可扩展性**

  强大的 API 带来无限的可能，与数种模板引擎（EJS，Pug，Nunjucks）和工具（Babel，PostCSS，Less/Sass）轻易集成

  

# Hexo系列（二）：Hexo安装



```bash
#1.安装nodejs和npm
yum install epel-release -y
yum install nodejs npm -y

#2.安装git
yum install git -y

#3.安装hexo
npm install hexo-cli
npm install hexo

#4.检查是否安装成功
[root@node1 ~]# npm list
root@ /root
├── hexo-cli@4.3.0
└── hexo@6.3.0
通过npm list可以看到hexo和hexo-cli的相关信息，说明安装成功

#5.初始化网站
hexo init myhexo
初始化成功后，会在当前目录生成myhexo的网站目录
cd myhexo/
npm install

结果信息
[root@node1 ~]# hexo init myhexo
INFO  Cloning hexo-starter https://github.com/hexojs/hexo-starter.git
INFO  Install dependencies
INFO  Start blogging with Hexo!

#6.启动hexo
hexo server
防火墙放开4000端口
firewall-cmd --zone=public --add-port=4000/tcp --permanent
firewall-cmd --zone=public --add-port=4000/udp --permanent
firewall-cmd --reload

#7.访问hexo
http://192.168.111.132:4000

```


