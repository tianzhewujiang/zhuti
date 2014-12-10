Hexo-Theme-zhuti
===

特点


* Bootstrap - 基于 Bootstrap 3.1.1 ；
* 标签插件 - 专门编写了一系列的 Bootstrap tag plugins ，以最大程度的发挥 Bootstrap 的威力。包括：
* textcolor - 插入一段带有特殊颜色标记的文本；
* button - 插入一个按钮，并允许为其指定超链接、文本及颜色；
* label - 插入一个标签，并为其指定文本和样式；
* badge - 插入一个徽章，并为其指定文本；
* alert - 插入一段警报文本信息，并为其指定样式。

安装

* 安装主题：


`$ git clone git@github.com:tianzhewujiang/zhuti.git themes/zhuti`

* 安装 hexo-tag-bootstrap:

`$ npm install hexo-tag-bootstrap --save`

* 创建页面

zhuti 预先定义了 Categories（分类）、Tags（标签） 和 About（关于）页面，要使用它们，你需要先在你的博客的 source 目录中添加相应页面。

例如，要创建 Categories 页面，你可以在 source/categories/ 目录 1 1如果没有这个目录，就新建一个。 下创建一个 index.html 文件，内容如下：
```
title: Categories
layout: categories
---
```
Tags 页面和 About 页面与此类似，不同的是 layout 分别为 tags 和 page 虽然几个文件的创建都很简单，但无论如何要求用户手动创建文件的确不太友好。我打算以后把这一步取消，改为自动生成 Categories 和 Tags 页面。 。

如果你依然不太明白如何创建这几个文件，可以参考 zhuti 的 Demo 站点的 source 目录。

启用

修改 _config.yml 文件里的 theme 选项为 zhuti 即可。

更新

```
$ cd themes/zhuti
$ git pull
```

配置

zhuti 的配置文件如下：

```
slogan: Yet another bootstrap theme.
menu:
- title: Archives
url: archives
intro: All the articles.
icon: fa fa-archive
- title: Categories
url: categories
intro: All the categories.
icon: fa fa-folder
- title: Tags
url: tags
intro: All the tags.
icon: fa fa-tags
- title: About
url: about
intro: About me.
icon: fa fa-user
links:
- title: My Github
url: http://www.github.com/
intro: My Github account.
icon: fa fa-github
- title: My LinkedIn
url: http://www.linkedin.com/p
intro: My Linkin account.
icon: fa fa-linkedin
widgets:
- search
- category
- tagcloud
- recent_posts
- links
rss: atom.xml
favicon: favicon.png
fancybox: true
google_analytics: UA-49061001-1
```

其中：

* slogan - 修改显示在博客首页的个性签名；
* menu - 导航菜单；
* links - 修改 links 小挂件的推荐链接；
* widgets - 在博客边栏显示的挂件列表；
* rss - RSS 链接；
* fancybox - 是否启用 Fancybox；
*  google_analytics - Google Analytics ID。

Front-Matter

zhuti 主题额外提供了一些新的 front-matter 的选项，利用这些选项可以更好的装饰你的文章。

* description - 在文章顶部插入一段简短的摘要信息
* feature - 为文章添加一张 feature 图片，这张图片将展示在主页的文章列表中
* toc - 生成 table of contents

示例：
```

title: Tag Plugins
date: 2014-03-16 10:17:16
tags: plugins
categories: Docs
description: Introduce tag plugins in zhuti.
feature: images/tag-plugins/plugins.jpg
toc: true
---
```