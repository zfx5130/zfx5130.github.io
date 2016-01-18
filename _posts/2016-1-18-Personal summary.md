---
layout: post
title: 年度个人总结
categories: [blog ]
tags: [总结,]
description:  年度个人总结
---

时间如白驹过隙，转瞬即逝。不知不觉中，一年的大好时光又过去了。下面我将以评分的形式对自己在工作，生活等方面做总结。

## 工作

个人觉得70分。

* 一直保持认真对待。
* 工作中从不开小差。
___

剩余30分

* 对代码的要求没有达到自己的要求。
* 技术能力有待提高。


## GitHub Pages 博客相关服务及工具一览

搭建一个基于 GitHub 的博客，一般会利用到一下的一些服务及工具（仅作了解，不需要深究）：

1. GitHub 知名代码托管平台。博客的所有文档都存放在 GitHub 的个人项目里。博客是用了其中的一个服务：GitHub Pages；
2. Jekyll 基于 GitHub 的模板系统，可选取相关的主题作为自己的博客样式。初次之外，也可选用；
3. Markdown 写作博文时使用的文本语法，条理分明，易于掌握；
4. Git 一种代码版本管理的程序，包括我们博客更新也是依赖于此；
5. Godaddy.com / Gandi.net / NameCheap.com 购买个人域名的网站，前两个支持支付宝/银联，第三个只有双币信用卡才能购买；
6. DNSPod 配置 DNS 解析服务的网站；
7. Qiniu / imgur.com 托管博客图片的图床，当然图片较少时也可在 GitHub 项目里直接存放，但容量有些，只有200M，最好是图床托管，只把博客设置中有关的 博客 Logo/个人头像/博客主题图片放在 GitHub 项目里；
8. Mou / MacDown / Typora Markdown 编辑器 写作博客时常备的写作工具，主要保存（使用）格式为 md；
9. TextMate / Sublime Text 业界知名的编辑器，用于打开和编辑各类程序文档，在修改一些博客设定的文档时会用到；
10. GitHub for Mac GitHub 的官方客户端.拥有图形界面 使用很傻瓜化 平时博客都可以通过客户端来发布和提交修改。

## GitHub for Mac 客户端使用说明

GitHub 客户端下载地址：[GitHub for Mac](https://desktop.GitHub.com/)

在本地管理博客，我们需要用到 GitHub for Mac。这是一款由 GitHub 官方推出的一个 git 客户端，用于日常提交和同步项目变动。虽然这个客户端功能相对简单，但对于博客管理来说，已经足够我们使用。

使用 GitHub for Mac 需要登录自己的 GitHub 账户。

### 登录 GitHub 账户
打开 GitHub 的菜单（切换到 GitHub 界面，Mac 左上角的应用菜单），选择 Preference 偏好选项，点选 Account 登录个人 GitHub 账户。

![GitHubID](http://7s1rzi.com1.z0.glb.clouddn.com/GitHubID.png)

### Clone 或 Add 个人博客项目

![GitHub for Mac](http://7s1rzi.com1.z0.glb.clouddn.com/GitHubPic1.png)

在登录后，将已经 Fork 的 GitHub Pages 项目从 GitHub （云端）中， Clone 到本地来，以便于修改。

博客项目一般的命名都是「个人 ID + GitHub.io」形式。不然无法作为作为个人博客存在。

### 提交和同步博客的修改

下载完项目后，可以在 Finder 里打开，然后进行查看、修改文档、添加博文之类的操作。

在修改文件（修改文件和添加博文的方法，将在后边说明。）完成后，GitHub 客户端会将文件的修改细节（包括位置和次数）显示出来。由于文件是在本地修改的，因而还需要提交到 GitHub 的服务器上，修改才会最终生效。

![GitHub for Mac2](http://7s1rzi.com1.z0.glb.clouddn.com/GitHubPic2.png)

上图显示的就是提交的流程：

    0. 选择相应的项目（这是是博客项目）；
    1. 如有修改，在 Description 填写说明（可以非常简要，但不能省略）；
    2. 点击「Commit to master」，提交修改；
    3. 点击右上角的「Sync」；
    4. 文件同步完成，片刻后更新生效。

说完 GitHub for Mac 如何提交修改和同步了，咦，好像漏了什么？

那我们回过来，说说我们刚才下载到本地的项目到底该如何处理吧——如何修改博客和添加博文。这是接下来要讲的。

## GitHub Pages 项目文档说明

打开 clone 到本地的 GitHub 项目，一般目录里有以下类型的文件。 

基础目录结构：

    |-- _config.yml
    |-- index.html
    |-- _includes
    |-- _layouts
    |   |-- default.html
    |   `-- post.html
    |-- _assets
    |-- _posts
    |   `-- 2015-04-27-Like-Kissing.md
    |-- images
    |   `-- Leah.png 
    |-- CNAME
    |-- _404.html
    |-- About.md
    |—— feed.xml
    `-- README.md

目录文档详细说明：    

* _config.yml **博客配置**文档（包括博客标题、favicon、博主 ID、头像、描述、联系方式等基本信息都在这个文档修改）；
* index.html 博客架构文档；
* _includes 存放博客调用的模块文件（比如导航栏、底栏、博文内容显示、评论模块等）的文件夹，一般不需要管；
* _layouts 存放博客调用的页面模板文件（比如博客主页、具体博文页）的文件夹；
* _assets 博客系统的相关程序文档；
* _posts **博客正文**存放的文件夹。命名有规定，必须为「日期 + 标题」的模式，即「2015-04-27-Like-Kissing.md」，才能发布到博客里；
* images 图片文件夹，存放博客相关素材，包括博客 favicon、博主头像等图片及博文贴图素材；
* CNAME **绑定个人域名**配置文档；
* 404.html 「404 Not Found.」，站点链接无法访问时的展示页。
* About.md 博客中的个人说明文档（About Me）；
* feed.xml 博客的 RSS 订阅工具；
* README.md 项目说明文档。用于 GitHub 个人项目主页的说明（描述）。

## 常用文档

自定义修改中，需要自己修改的文档包括：_config.yml、About.me、CNAME，以及 Public 文件夹下的存放的 Logo、头像一类。一些博客还需要（看具体需求）修改_includes 下的 sidebar 文件，当然这个博客可以不管。

编辑器(用于打开及修改上述的文档)：

* [TextMate](https://macromates.com/) 
* Sublime Text 

Markdown 编辑器（写博文时用到的写作应用）：

* [MacDown](http://macdown.uranusjr.com/)
* [Mou](http://25.io/mou/)

## 常用博文模板

博文存放在 _posts 文件夹中。格式必须为 「日期 + 英文标题」，不然无法识别和发布。

博文的文件格式一般为 md(Markdown )格式。HTML 格式作为博文发布其实也可，但语法复杂，不利于写作，在此不具体说明。

每一篇 Markdown 文档的开头（第一行都为「 ---」）都必须添加一段代码，用以将文档收录到博客以及标签系统中。

代码类型如下：

    ---  
    layout: post  
    title:   
    description:     
    headline: 
    categories: Blog  
    tags: 
      -   
    comments: ture  
    published: true  
    ---  
    正文...

这其中，Title 一项是必须添加的。Categories 可以换，这个博客默认归档在 Blog 目录下。Tags 可以自己按照文章主题添加，也可以不加。

所以有必要保存一份在本地，便于发布文章的时候能随时取用。

以下是一篇博文内容的例子：

    ---
    layout: post  
    title: 夏天的烟花（作为标题）  
    description:   
    headline:     
    categories: Blog（作为目录）  
    headline:  
    tags: 
      - Photo（添加的第一个标签） 
      - Instagram（添加的第二个标签，另起一行） 
    comments: ture  
    published: true  
    ---
    正文...


一个可用的 md 格式博文代码模板（仅供 [HMFAYSAL Omega THeme](http://www.hossainmohdfaysal.com/hmfaysal-omega-theme/) 模板使用）下载地址：

* 百度云 - [Dl from BaiduYun](http://pan.baidu.com/s/16XGCY)
* box.com - [Dl from box.com](https://app.box.com/s/48d5f5q8osbhaewr3jruec7qvl3fqe4g)
* dropbox - [Dl from dropbox](https://dl.dropboxusercontent.com/u/64524965/Sample.md)

直接下载 Sample.md 文档后填写相应的内容，开始写博文。Dropbox 文档可以预览时复制粘贴格式到本地的编辑器开始写。

写好文档后将文档保存（修改）为「日期 + 标题」的模式，如：「2015-04-27-Like-Kissing.md」。

然后将 md 文档复制或拖放到 _posts 文件夹里。在 GitHub for Mac 客户端 commit 和 sync，稍等片刻新添加的博文就会自动发布到博客里啦。

## 网页端在线发布博文

除了利用 GitHub 客户端以外，我们还可以通过 GitHub 网站发布博文。这时，如果写作时使用图片，得借助图床，因为网页端无法上传图片。

登录 GitHub 网站。

找到自己的 gh-Pages 博客项目主页（对，就是 ID.GitHub.io 命名的那只）。

点击主目录中的 _posts 文件夹。然后点击「+」，创建新博文。

![GitHubWeb](http://dreamofbook.qiniudn.com/GitHubWeb.jpg)

博文结构还是一样：

* 标题
* 博文代码
* 正文

![](http://dreamofbook.qiniudn.com/GitHubWeb2.png)

写完后，为本次创建文档的操作输入一段描述，而后确认提交就发布啦。

## Markdown 语法

回过头来再简要介绍一下 Markdown 语法。

博文一般都使用 Markdown 语法写作。

Markdown 语法是对纯文本格式的强化，能使文本显示得更清晰、有条理。但它依旧算是简单的文本，很容易修改和扩展，常用于快速写作之中。

Markdown 格式的简洁特性，使之能快速转换为各种互联网上的常用格式，比如 HTML、Word、PDF 等，所以目前越来越常用。

关于 Markdown 语法的细则，请参看 [Markdown 简明语法参考](http://azeril.me//blog/2015/08/19/Markdown-Syntax/)。

本篇说明就到此为止啦。

期待某人新博文的诞生。


