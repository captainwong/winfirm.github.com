---
layout: post
category: "android"
title:  "基于Volley的网络请求工具"
tags: [Android,Volley]
---
####一、Volley基本处理流程
1、应用初始化Volley。  
2、Volley创建一个RequestQueue、NetworkDispatcher组及Network。  
3、RequestQueue即一个Request队列，RequestQueue会创建一个ExecutorDelivery。  
4、NetworkDispatcher实质是Thread，从RequestQueue中取Request，通过Network加以执行。  
5、Network负责网络请求处理，具体过程交给HttpStack处理。  
6、HttpStack分HttpClient(SDK_INT>=9)与HttpURLConnection两种方式。  
7、ExecutorDelivery负责处理请求结果，并与主线程进行交互。  
8、Volley在上述2-7的基础上增加了Cache等附加处理环节。

####二、基于Volley的网络请求工具
在Volley基础上进行了封装，方便使用。  
工程地址：<https://github.com/winfirm/android-volley-manager>

####三、早期使用的android-async-http改进型
工程地址：<https://github.com/winfirm/android-async-http>
