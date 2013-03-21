---
layout: post
title: "kindle touch 修复"
date: 2012-07-14 20:10
comments: true
categories: 
---
本人有一已越狱且换过字体的kindle touch，系统版本5.0.3，直接升级5.1.0失败，提示错误006。

于是将其恢复出厂设置，果断杯具，文字无法正常显示，均变成“口口口口口口口口口”，忽然想起换过字体，于是字体文件拷回kindle touch，显示正常。

打算换回原有字体并且反越狱，折腾N久未果，大怒，于是将kindle touch恢复到最初的5.0.0，记录之。
<!-- more -->
*   下载5.0.0完整镜像,Google **mmcblk0p1-kt-5.0.0.img** 即可下载；
*   进入工程模式，并且在工程模式中打开SSH；
*   使用SSH登录kindle，将下载的 mmcblk0p1-kt-5.0.0.img 文件拷到 /mnt/us/目录，Windows下可以使用WinSC；
*   命令行下执行 dd if=/mnt/us/mmcblk0p1-kt-5.0.0.img of=/dev/mmcblk0p1 bs=4K ，等几分钟执行完成，现在系统已经是原始的5.0.0版了；
*   升级，在官网[下载](http://www.amazon.com/gp/help/customer/display.html/ref=hp_left_cn?ie=UTF8&amp;nodeId=200790650 "Amazon官网kindle升级包")升级包，按照常规方式升级，ok，搞定！

![kindletouch](http://farm9.staticflickr.com/8505/8410898542_3886db9534_b.jpg "kindletouch")

打开后发现5.1.0系统自带的中文字体已经比较好看了，比起之前自带的坑爹字体好很多，所以也没必要越狱换字体了，就这么用了。
