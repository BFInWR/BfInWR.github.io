---
title: Java的四种引用
date: 2020-3-6 15:52:00
categories: "Java"
tags:
	- Java
	- JVM
	
---
## 四种引用
把对象的引用分为四种级别，更灵活控制对象的生命周期，这四种级别由高到低依次为：强引用、软引用、弱引用和虚引用。
<!--more-->
***
### 强引用（不会回收）
我们使用的大部分引用实际上都是强引用，这是使用最普遍的引用。当内存空间不足，Java虚拟机宁愿抛出OutOfMemoryError错误，使程序异常终止，也不会靠随意回收具有强引用的对象来解决内存不足问题。

### 软引用（内存不足才会）
软引用可用来实现内存敏感的高速缓存。
软引用在实际中有重要的应用，例如浏览器的后退按钮。

### 弱引用（发现就会回收）
弱引用可以和一个引用队列（ReferenceQueue）联合使用

###虚引用（任何时候都可能被垃圾回收）
