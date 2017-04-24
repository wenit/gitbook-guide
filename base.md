# 基本使用

## 初始化项目

**1、建立项目目录**

mkdir gitbook-guide

**2、进入项目目录**

cd gitbook-guide

**3、初始化项目**

gitbook init

``` bash
> gitbook init
warn: no summary file in this book
info: create README.md
info: create SUMMARY.md
info: initialization is finished
```

会生成两个文件：
README.md 和 SUMMARY.md 是两个必须文件
README.md 是对书籍的简单介绍
SUMMARY.md 是书籍的目录结构


**4、SUMMARY.md说明**

```
# Summary

* [前言](README.md)
* [修订记录](version.md)
* [环境搭建](install/README.md)
    - [插件安装](install/pluin.md)
    - [redis安装](install/redis.md)
* [开发工具使用](yt-studio/README.md)
* [前端H5框架](h5/README.md)
* [前端接口框架](server/README.md)

```

SUMMARY.md 是书籍的目录结构，格式如上，每一行对应一个相应的文件。

执行 `gitbook init` 会根据 SUMMARY.md 目录生成对应的文件夹和 md 文件，每一个 md 文件对应每一章节，每一章节的内容在对应的 md 文件里编辑。

重新执行`gitbook init`，控制台信息如下：
```
> gitbook init
info: create version.md
info: create install/README.md
info: create install/pluin.md
info: create install/redis.md
info: create yt-studio/README.md
info: create h5/README.md
info: create server/README.md
info: create SUMMARY.md
info: initialization is finished
```

```
F:\test\gitbook-guide>tree /f
Folder PATH listing for volume 学习资料
Volume serial number is 0FE2-1355
F:.
│   README.md
│   SUMMARY.md
│   version.md
│
├───h5
│       README.md
│
├───install
│       pluin.md
│       README.md
│       redis.md
│
├───server
│       README.md
│
└───yt-studio
        README.md
```


如果想要新增章节，可以在 SUMMARY.md 里面新增，然后执行 gitbook init 就会新增对应的 md 文件，原有文件不会变化；如果想要删除章节，在 SUMMARY.md 里面删除，然后执行 gitbook init 想要删除的 md 文件并不会删除，需要手动删除。

## 生成html文件
gitbook build

执行`gitbook build`可生成html文件，默认生成的文件在当前目录下_book目录下，将_book目录部署到对应的web服务器就可以了正常访问了。

控制台输出：
```
F:\test\gitbook-guide>gitbook build
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 8 pages
info: found 6 asset files
info: >> generation finished with success in 1.2s !

```

目录信息：
```
F:\test\gitbook-guide>tree
Folder PATH listing for volume 学习资料
Volume serial number is 0FE2-1355
F:.
├───h5
├───install
├───server
├───yt-studio
└───_book
    ├───gitbook
    │   ├───fonts
    │   │   └───fontawesome
    │   ├───gitbook-plugin-fontsettings
    │   ├───gitbook-plugin-highlight
    │   ├───gitbook-plugin-lunr
    │   ├───gitbook-plugin-search
    │   ├───gitbook-plugin-sharing
    │   └───images
    ├───h5
    ├───install
    ├───server
    └───yt-studio

```

## 本地预览

gitbook serve

执行`gitbook serve`启动本地http服务，可在浏览器中直接预览生成html文件。
在浏览器中输入 http://localhost:4000 进行访问。

```
F:\test\gitbook-guide>gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 8 pages
info: found 6 asset files
info: >> generation finished with success in 1.5s !

Starting server ...
Serving book on http://localhost:4000
```

## 生成PDF

gitbook pdf

执行`gitbook pdf`可生成PDF文件，直接执行会报错，请先安装[calibre](http://calibre-ebook.com/)，才能正常生产PDF文件，及其他格式文件。

```
F:\test\gitbook-guide>gitbook pdf
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 8 pages
info: found 6 asset files
info: >> generation finished with success in 3.5s !
info: >> 1 file(s) generated
```