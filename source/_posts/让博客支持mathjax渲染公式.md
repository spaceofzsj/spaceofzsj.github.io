---
title: 让博客支持mathjax渲染公式
abbrlink: 20f2bfce
date: 2021-11-15 17:31:55
tags:
- 博客搭建
- 计算机
- 技术
categories:
- 博客搭建
---
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=1852502698&auto=0&height=66"></iframe>
>从起床折腾到晚上，累趴。。。

<!--more-->

总体思路是卸载掉hexo默认的`hexo-renderer-marked`，改用`hexo-renderer-pandoc`。（就是这么简单的一步。。。）

首先如果没安装`pandoc`的话，去[官网](https://www.pandoc.org/)下载。安装完重启电脑。

然后命令行里进入博客的路径(.../blog)，利用`npm uninstall hexo-renderer-marked --registry=https://registry.npm.taobao.org`卸载掉原来的`hexo-renderer-marked`。执行`npm install hexo-renderer-pandoc --registry=https://registry.npm.taobao.org`安装上`hexo-renderer-pandoc`。

打开theme的_config.yml，修改里面的`mathjax`的`false`为`true`。

在blog目录下的_config.yml加上下面的代码：
```YAML    
math:
  engine: 'mathjax' # or 'katex'
  mathjax:
    # src: custom_mathjax_source
    config:
      # MathJax config
```
保存并退出。接下来执行`hexo clean`，`hexo g`，`hexo s`即可看到公式被渲染。