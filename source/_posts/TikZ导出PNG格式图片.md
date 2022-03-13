---
title: TikZ导出PNG格式图片
cover: https://gitee.com/spaceofzsj/pictures/raw/master/20220228001612.png
tags:
  - LaTeX
  - TikZ
abbrlink: aeaa5c03
date: 2022-02-27 16:37:07
categories:
---
利用`LaTeX`的`TikZ`宏包可以绘制图形，但是默认导出的为pdf格式。有时我们需要PNG等图片格式以便于插入在网页上，于是需要将pdf格式转换为图片格式。
<!--more-->
# 安装`ImageMagick`

首先，我们去[ImageMagick官网](https://imagemagick.org/script/download.php)下载合适版本的`ImageMagick`。下载完成后安装即可。安装完成后将安装目录添加到系统Path路径中(系统搜索**环境变量**)。

# 允许`-shell-escape`
不同编辑器允许`-shell-escape`的方式不同，可以在这个StackExchange问题下查找：[How can I enable shell-escape?](https://tex.stackexchange.com/questions/598818/how-can-i-enable-shell-escape)。

此处以`VScode`中的[`LaTeX Workshop`](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)插件为例。
打开`VScode`，确保已经安装`LaTex Workshop`。按下`Ctrl+Shift+P`，输入`Preferences: Open Settings (JSON)`。进入`settings.json`中添加如下代码
```json
"latex-workshop.latex.tools": [
    {
        "name": "latexmk",
        "command": "latexmk",
        "args": [
            "-shell-escape",  
            "-synctex=1",
            "-interaction=nonstopmode",
            "-file-line-error",
            "-pdf",
            "-outdir=%OUTDIR%",
            "%DOC%"
        ],
        "env": {}
    },
    ...
]
```
如果以前输入过，只需在`"args"`栏目中添加`"-shell-escape"`一项。这样就允许了`-shell-excape`。

# LaTeX代码设置

为了导出PNG格式，我们选用`standalone`文档类，调用其中的`convert`选项来完成格式转换。下面给出一个例子：
```latex
\documentclass[convert={convertexe={magick}}]{standalone}
\usepackage{tikz-cd}
\usepackage{amsmath,amssymb}
\usepackage{mathtools}
\pagecolor{white}
\begin{document}
\begin{tikzcd}[row sep=huge]
    &D^{2}\arrow[dl,shift right]\arrow[dr,shift left,"+S^{1}"]{+S^{1}}&\\
    \mathbb{R}^{2}\arrow[ur,shift right]\arrow[rr,"+\{\infty\}"] &         &S^{2}\arrow[ul,shift left,"-\{p\}"]
\end{tikzcd}
$\xRightarrow{\text{generlization}} S^{n}=\mathbb{R}^{n}\bigcup \{\infty\}$
\end{document}
```
注意以下几点：
1. 代码第一行的文档选项`convert={convertexe={magick}}`里面的`magick`为下载的`ImageMagick`中`.exe`文件的文件名（以后版本文件名也可能有变化，要注意改变）。网上其他相关的资料可能文档选项只有`convert`，因为`ImageMagick`早期版本可能文件名与现在不同。
2. 转换后得到的PNG图片可能背景是透明的,`\pagecolor{white}`可以让背景变为白色。
3. 默认得到的为300dpi的PNG格式图片。可以更改选项调整得到需要的图片，具体见：[`standalone`官方文档](https://ctan.org/pkg/standalone)。
   
该代码生成的图片为：![Relations](https://gitee.com/spaceofzsj/pictures/raw/master/cd20220227.png)
