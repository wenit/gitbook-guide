# 高级扩展

> 掌握了“基本使用”，但有时候想要gitBook更美观，或者更符合我们自己的需求，则通过book.json配置进行自定义、以及安装一些常用的插件等。

## book.json

### 新建book.json文件

如下内容，是我自己定义的一个配置文件，下面对这些配置进行详细的说明
``` json
{
	"title": "GitBook入门指南",
	"description": "本文介绍GitBook的安装、基本使用和高级扩展。",
	"author": "wenit",
	"plugins": ["-sharing",
	"-search",
	"atoc",
	"search-pro",
	"toggle-chapters",
	"splitter",
	"tbfed-pagefooter"],
	"links": {
		"gitbook": false,
		"sharing": {
			"google": false,
			"facebook": false,
			"twitter": false,
			"all": false
		},
		"sidebar": {
			"Home": "http://wenit.github.io/"
		}
	},
	"pluginsConfig": {
	    "atoc": {
            "addClass": true,
            "className": "atoc"
        },
		"search-pro": {
			"cutWordLib": "nodejieba",
			"defineWord": ["Gitbook Use"]
		},
		"tbfed-pagefooter": {
			"copyright": "Copyright &copy www.wenit.cn 2017",
			"modify_label": "该文件修订时间：",
			"modify_format": "YYYY-MM-DD HH:mm:ss"
		}
	}
}
```

### 配置文件详细说明：
``` bash
title
# 设置书本的标题
"title" : "GitBook入门指南"
author
# 作者的相关信息
"author" : "wenit"
description
# 本书的简单描述
"description" : "本文介绍GitBook的安装、基本使用和高级扩展。"
language
# Gitbook使用的语言, 版本2.6.4中可选的语言如下：
en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw
# 配置使用简体中文
"language" : "zh-hans",
links
# 在左侧导航栏添加链接信息
"links" : {
    "sidebar" : {
        "Home" : "http://wenit.github.io/"
    }
}
styles
# 自定义页面样式， 默认情况下各generator对应的css文件
"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}
例如使<h1> <h2>标签有下边框， 可以在website.css中设置
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
plugins
# 配置使用的插件
"plugins": [
    "toggle-chapters"
]
# 添加新插件之间需要运行gitbook install来安装新的插件
Gitbook默认带有5个插件：
	• highlight
	• search
	• sharing
	• font-settings
	• livereload
# 如果要去除自带的插件， 可以在插件名称前面加-
"plugins": [
    "-search"
]
pluginsConfig
# 配置插件的属性
"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}

```

## 插件安装

gitbook install

如果book.json中指定了插件，一定要先执行`gitbook install`进行插件安装。
