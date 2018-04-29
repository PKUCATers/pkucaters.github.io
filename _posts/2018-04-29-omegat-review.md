---
date: 2018-04-29 12:54:17+00:00
layout: post
title: Omegat本地化项目的审校
categories: 本地化
tags: 
---

利用omegat的脚本，我们可以把翻译结果导出，类似如下结构

```
1786                             #片段数
Project Specific External Search #原文
项目特定的外部搜索               #译文

Administrator                    #最后修改者
Bundle.properties                #所在文件

1787
Items
项目

xulihang
Bundle.properties
```

把结果按每人对应的片段，可以再分出31个文件，即把每个人负责的片段都整个到一个文本文件里。依次提交commit并传到github上。然后我们可以查看每个文件的commit。在有错误的行的左边点击“+”，可以进行评论。这就相当于对某位同学的翻译进行审校。

![](https://github.com/pkucaters/pkucaters.github.io/raw/master/album/omegat/review-commit.JPG)

![](https://github.com/pkucaters/pkucaters.github.io/raw/master/album/omegat/review-comment.JPG)

收到建议后，原来片段的负责人可以用omegat打开项目进行修改，并在github上回复已修改。

审校以三个同学为一组，每个人要对其它两位的翻译进行审校。

具体分工见[表格](http://pkucaters.github.io/assets/审校分工.xlsx)。

另外还有之前的[完整分工表](http://pkucaters.github.io/assets/分工new.xlsx)

