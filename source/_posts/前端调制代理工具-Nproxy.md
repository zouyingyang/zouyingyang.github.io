---
title: 前端调制代理工具-Nproxy
date: 2016-07-05 23:38:46
tags:
    - 调试
categories: Nproxy
comments: true
---

给大家介绍一个我使用的第一款代理工具 Nproxy
<!--more-->

### 环境要求
Node

### 安装Nproxy
在终端中输入 `$ npm install -g nproxy`

### replace_rule.js配置
创建 replace_rule.js 文件
示例如下:
```javaScript
module.exports = [

  // 1. replace single file with local one
  {
    pattern: 'homepage.js',      // Match url you wanna replace
    responder:  "/home/goddyzhao/workspace/homepage.js"
  },

  // 2. replace single file with web file
  {
    pattern: 'homepage.js',      // Match url you wanna replace
    responder:  "http://www.anotherwebsite.com/assets/js/homepage2.js"
  },

  // 3. replace combo file with src with absolute file path
  {
    pattern: 'group/homepageTileFramework.*.js',
    responder: [
      '/home/goddyzhao/workspace/webapp/ui/homepage/js/a.js',
      '/home/goddyzhao/workspace/webapp/ui/homepage/js/b.js',
      '/home/goddyzhao/workspace/webapp/ui/homepage/js/c.js'
    ]
  },

  // 4. replace combo file with src with relative file path and specified dir
  {
    pattern: 'group/homepageTileFramework.*.js',
    responder: {
      dir: '/home/goddyzhao/workspace/webapp/ui/homepage/js',
      src: [
        'a.js',
        'b.js',
        'c.js'
      ]
    }
  },

  // 5. Map server image directory to local image directory
  {
    pattern: 'ui/homepage/img',  // must be a string
    responder: '/home/goddyzhao/image/' //must be a absolute directory path
  },

  // 6. Write responder with regular expression variables like $1, $2
  {
    pattern: /https?:\/\/[\w\.]*(?::\d+)?\/ui\/(.*)_dev\.(\w+)/,
    responder: 'http://localhost/proxy/$1.$2'
  },

  // 7. Map server image directory to local image directory with regular expression
  // This simple rule can replace multiple directories to corresponding locale ones
  // For Example,
  //   http://host:port/ui/a/img/... => /home/a/image/...
  //   http://host:port/ui/b/img/... => /home/b/image/...
  //   http://host:port/ui/c/img/... => /home/c/image/...
  //   ...
  {
    pattern: /ui\/(.*)\/img\//,
    responder: '/home/$1/image/'
  }
];
```

###用法：在replace_rule.js中设置你要重定向的文件路径,执行下面代码
`$ nproxy -l replace_rule.js`
### 参考文献：
[开发跨平台的静态资源替换工具——NProxy](http://goddyzhao.me/nproxy)



