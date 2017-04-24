# 安装

> 在使用GitBook 之前, 我们需要先安装一些必须的工具，Node.js、GitBook和markdown的编辑器。

## Node.js安装

> Node.js 是一个基于Chrome JavaScript 运行时建立的一个平台，用来方便地搭建快速的，易于扩展的网络应用· Node.js借助事件驱动，非阻塞 I/O 模型变得轻量和高效，非常适合 run across distributed devices 的 data-intensive 的实时应用。


**1、win下安装Node.js**
直接到[Node.js](https://nodejs.org/en/)官网下载，简单安装即可，此处不再细述。

**2、检测是否安装成功**
``` bash
node -v
v6.9.1
```

## GitBook安装

> GitBook 是一个基于 Node.js 的命令行工具，可使用 Github/Git 和 Markdown 来制作精美的电子书。通过Node.js命令安装GitBook

**1、npm安装Gitbook**
``` bash
#安装命令
npm install -g gitbook
#卸载命令
npm uninstall -g gitbook
```

**2、安装gitbook cli**
想在系统上的任何地方的gitbook命令，需要安装“gitbook cli”，执行以下命令

``` bash
#安装命令
npm install -g gitbook-cli
#卸载命令
npm uninstall -g gitbook-cli
```

**3、检验下是否安装成功**
``` bash
gitbook -V
CLI version: 2.3.0
GitBook version: 3.2.2
```

## Markdown编辑器安装

markdown的编辑器有很多，我使用的是[Haroopad](http://pad.haroopress.com/)，大家可自行下载，如果熟悉markdown的语法，任何文本编辑器，都能使markdown的编辑器。