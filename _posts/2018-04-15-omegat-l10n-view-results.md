---
date: 2018-04-15 22:05:17+00:00
layout: post
title: 查看本地化后的Omegat网站、文档和UI
categories: 本地化
tags: 
---

我们可以在OmegaT的网站项目下直接运行jekyll生成网页，在omegat的源码包里从docbook文档生成html文件来验证翻译。

但是以上两个操作在配置环境方面需要花费较长时间，我们可以配置好一台linux vps服务器，然后大家把翻译好的文件用git push上去就可以自动查看结果了。

具体是如何做到的可以参见以下两个网页：

[搭建自己的GitHub Pages服务器](http://blog.xulihang.me/build-your-own-github-pages-server/)

[从omegat的docbook构建成品文档](http://blog.xulihang.me/build-omegat-docbook/)

以下是具体操作方法。

## 生成网站

### 1、克隆仓库

`git clone ssh://git@cattc-contest.com:43999/home/git/web`

输入密码后完成操作。

### 2、更新文件

在omegat里点生成已译文档，到项目文件夹下找到target/website文件夹，把里面的内容替换仓库的内容。

### 3、提交更改并上传文件

依次运行以下命令（或者使用客户端）：

`git add .`

`git commit -m "update"`

`git push`

输入密码以完成操作，会看到窗口里显示正在重新构建网站。

### 4、查看结果

访问[http://cattc-contest.com:8080/zh_CN](http://cattc-contest.com:8080/zh_CN)查看结果。


## 生成文档

操纵和生成网站类似，clone地址变为`ssh://git@cattc-contest.com:43999/home/git/doc`。将target/doc_src里的文件替换到zh_CN文件夹。

查看地址是[http://cattc-contest.com:8080/zh_CN/docs/index.html](http://cattc-contest.com:8080/zh_CN/docs/index.html)。

## 加载UI

加载中文UI文件很简单，将创建已译文档生成的`Bundle_zh_CN.properties`复制到OmegaT的目录下，运行如下命令启动OmegaT：

`java -jar OmegaT.jar resource-bundle=Bundle_zh_CN.properties`
