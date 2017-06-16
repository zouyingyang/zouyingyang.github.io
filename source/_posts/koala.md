---
title: Koala
date: 2016-08-25 12:14:29
tags:
    - Koala
categories: Koala
comments: true
---
Koala使用教程
![Alt koala](http://cdn.w3cplus.com/cdn/farfuture/F6MhuypX5htj1MvbS1WNtIIp9t5q3GRbNZ-U59FFWns/mtime:1370526886/sites/default/files/styles/print_image/public/tools/koala/koala.jpg "koala")
<!--more-->

## 上图中四个数字分别对应四个区域：

### 第一区域：
第一个按钮用于添加项目，第二个按钮打开编译文件的错误提示，第三个按钮设置koala，里面可以设置所有文件默认的编译输出方式，需要过滤的文件，界面语言（中文/英文）等。当然这里也包括目前koala的版本号及作者等信息。

### 第二区域：
project区域，可以直接把项目拖进该区域

### 第三区域：
需编译的文件列表，默认以下划线开头的文件不出现列表中，绿色表示动态编译的文件，灰色表示非动态编译。单击相应的文件，出现第四个区 块，设置文件编译的选项。如果你的文件是后添加的那么请点击上面的refresh按钮刷新需要编译的文件，当然也可以通过下面的几个all/less /sass/coffee来过滤自己要编译的文件。

### 第四区域：
设置文件编译的选项，这个区域得选中第三个区域的某个需要编译的文件才会出现。以sass为例，第一个选项表示是否启用动态编译；第二组 表示是否启用这四个功能，我这边为了方便调试所以启用debug info，当然如果你使用compass那就得启用compass；第三组表示输出的css格式，分为四 种：nested，compressed，compact，expanded；最后一个compile按钮可以手动编译。

既然熟悉了界面，我们就实际使用下吧，步骤走起：

## 简单的使用步骤

### 第一步：
首先点击我们第一区域的那个齿轮按钮，设置下默认文件的编译方式，并把界面语言设置为中文。
![Alt koala](http://cdn.w3cplus.com/cdn/farfuture/BP1PW54_zBmxFw97SPBtKPblvK6AxH8lhXH1e0Nm0Go/mtime:1370527209/sites/default/files/styles/print_image/public/tools/koala/step1-1.jpg "koala")
 ![Alt koala](https://app.yinxiang.com/shard/s57/res/3a0fdc16-3225-43b2-9784-bc6904a3bc24 "koala")
### 第二步：
添加我们要编译的项目文件，可通过第一区域的加号那个按钮添加，也可以直接将项目拖到第二个project区域。
### 第三步：
单击我们需要编译的文件，出现第四区域设置下该文件具体的编译方式，如果没什么特别的，直接用默认设置的就ok，如果不需要动态编译，直接勾掉“即时编译”那个checkbox，其余的按照上面说的操作。
 ![Alt koala](https://app.yinxiang.com/shard/s57/res/3a755866-6733-4866-8f43-9eb1ea05e46d "koala")
### 第四步：
右键单击需要编译的文件，出现我们常用的几个操作：打开文件，打开文件目录，打开输出文件目录，设置输出文件目录，编译，删除。一般这里我们需要设置下我们输出文件的目录。
 ![Alt koala](https://app.yinxiang.com/shard/s57/res/41d38fcf-8e4c-4d7f-aca1-97644ae034e4 "koala")
### 第五步：
如果你的文件既有less，sass还有coffee，那么就最好有必须点击下面的过滤条件，选择你要动态编译的文件，不然一锅煮头都大了。
 ![Alt koala](http://cdn.w3cplus.com/cdn/farfuture/bL1BBY4LxOBa9QPG3oBDQXGc_WbH7H3hBb60Ol4Pw-8/mtime:1370527578/sites/default/files/styles/print_image/public/tools/koala/step5.jpg "koala")