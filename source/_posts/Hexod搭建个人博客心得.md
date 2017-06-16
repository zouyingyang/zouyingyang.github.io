---
title: Hexo搭建个人博客心得
date: 2016-06-25 14:56:58
tags:
    - Hexo
categories: Hexo
comments: true
---

最近突然想建个个人博客,然后花了一个晚上的时间利用hexo,github搭建了一个,跟大家聊一下我在搭建过程中的一些心得.
<!--more-->

### 环境要求
Node
Git
(网上有很多教程,就不赘述了)

### 全局安装Hexo
在终端中输入 `$ sudo npm install -g hexo`

### blog项目下安装
新建blog项目文件
cd到你的blog项目下面 `$ cd blog`
初始化`blog$ hexo init`
生成静态页面`blog$ hexo generate`
终端命令显示如下命令则表示生成静态页面成功
```
INFO  Start processing
INFO  Files loaded in 922 ms
INFO  Generated: archives/2017/02/index.html...
```

本地启动`$ blog$ hexo server`
终端命令显示如下命令表示本地启动成功
```
INFO  Start processing
INFO  Hexo is running at http://localhost:4000/. Press Ctrl+C to stop.
```
浏览器输入http://localhost:4000
如正常显示页面
则本地已经调试成功

### Github配置
注册github账号
建立Repository
（需要注意的是仓库名必须用 username.github.io。比如我的用户名为 abc 则仓库名称为 abc.github.io）
打开blog项目下的_config.yml文件
搜索关键字 `deploy`，按下面格式修改
deploy:
&nbsp;&nbsp;&nbsp;&nbsp;type: git
&nbsp;&nbsp;&nbsp;&nbsp;repo: &nbsp;&nbsp;&nbsp;&nbsp;https://github.com/zouyingyang/zouyingyang.github.io.git   （改成你的用户名)
&nbsp;&nbsp;&nbsp;&nbsp;branch: master

安装一个依赖
`blog$ npm install hexo-deployer-git --save`

部署到github
`blog$ hexo deploy`
在浏览器中打开http://zouyingyang.github.io/

Hexo命令简写
hexo new 博客名称 : hexo n 博客名称 //新建博客
hexo generate : hexo g  //生成静态页面
hexo server : hexo s  //启动本地服务
hexo deploy : hexo d  //部署


blog
　｜
　｜－－ _config.yml （配置文件）
　｜－－ node_modules
　｜－－ public (静态文件)
　｜－－ source (需要提交的都放在这里。比如：文章，图片)
　｜－－ db.json
　｜－－ package.json
　｜－－ scaffolds
　｜－－ themes （主题）

### 参考文献：
[Jekyll迁移到Hexo搭建个人博客](http://www.ezlippi.com/blog/2016/02/jekyll-to-hexo.html#more)
[Next主题](http://theme-next.iissnan.com/)
[hexo命令及Markdown语法](http://www.tuicool.com/articles/I36zYr)



