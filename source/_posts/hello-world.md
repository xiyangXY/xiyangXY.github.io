---
# 标题
title: 使用Hexo搭建博客教程(window环境)
# 置顶
top: true
# 打赏
reward: true
# 分类
categories:
- 前端
# 标签
tags:
- Hexo
- node
- npm
- git
- github

---
Hexo 是一个快速、简洁且高效的博客框架，使用它你会发现搭建个人博客是如此的简单快捷，本篇文章将带你从零开始搭建个人博客并部署到github page上托管。

<!-- more -->
Hexo简介
=================
[Hexo](https://hexo.io/zh-cn/) 是一个基于nodejs 的静态博客网站生成器，作者是来自台湾的 Tommy Chen

特点：
* 不可思议的快速 ─ 只要一眨眼静态文件即生成完成
* 支持 Markdown
* 仅需一道指令即可部署到 GitHub Pages 和 Heroku
* 已移植 Octopress 插件
* 高扩展性、自订性
* 兼容于 Windows, Mac & Linux

环境搭建
=================

Hexo搭建步骤:
1. 安装nodejs
2. 安装git
3. 安装Hexo
4. 部署到github

安装nodejs
-----------------
Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。Node.js 使用了一个事件驱动、非阻塞式 I/O 的模型,使其轻量又高效。Node.js 的包管理器 npm,是全球最大的开源库生态系统。

[nodejs官网](http://nodejs.cn/)，选择LTS版本就行了

![nodejs](/images/nodejs.jpg)

根据步骤安装完成后打开命令行
``` cmd
node -v
npm -v
```

看到如下图结果表明已安装完成

![cmd](/images/cmd-node.jpg)

安装git
-----------------
Git 是一个开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。
Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。
Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。

[git官网](https://git-scm.com/), 直接下载最新版本就行了

![git](/images/git.png)

根据步骤安装完成后打开命令行
``` cmd
git --version
```

看到如下图结果表明已安装完成

![cmd-git](/images/cmd-git.jpg)

安装Hexo
-----------------
Hexo是一款基于Node.js的静态博客框架，依赖少易于安装使用，可以方便的生成静态网页托管在GitHub和Coding上，是搭建博客的首选框架。大家可以进入hexo官网进行详细查看，因为Hexo的创建者是台湾人，对中文的支持很友好，可以选择中文进行查看。

[Hexo官网](https://hexo.io/zh-cn/), 根据官网安装流程来安装

![git](/images/hexo.jpg)

使用 npm 安装 Hexo

``` cmd
npm install -g hexo-cli
```

根据步骤安装完成后打开命令行
``` cmd
hexo -v
```

看到如下图结果表明已安装完成

![cmd-hexo](/images/cmd-hexo.jpg)

选择一个工程放置的目录进行初始化，工程名称自己随便定义，我这里叫my-blog
``` cmd
hexo init my-blog
```

然后进入my-blog目录
``` cmd
cd my-blog
npm install
```

执行命令将hexo服务跑起来
``` cmd
hexo server
```

在浏览器输入localhost:4000就可以看到你生成的博客了

![cmd-hexo](/images/hexo-init.png)
