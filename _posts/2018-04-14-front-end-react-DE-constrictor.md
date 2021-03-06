---
layout: post
title: "前端react环境搭建 - 资料整理"
date: 2018-04-14 15:34:48 +0000
categories: 资料整理
---

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

* [0. 前言](#0-前言)
	* [0. 1 主旨](#0-1-主旨)
	* [0. 2 技术栈](#0-2-技术栈)
* [1. 正文](#1-正文)
	* [1. 1 npm 篇](#1-1-npm-篇)
	* [1. 2 webpack 篇](#1-2-webpack-篇)
	* [1. 3 脚手架篇](#1-3-脚手架篇)
		* [1. 3. 1 create-react-app](#1-3-1-create-react-app)
		* [1. 3. 2 dva-cli](#1-3-2-dva-cli)
* [2. 个人易用性的一些心得分享(其实就是说闲话)](#2-个人易用性的一些心得分享其实就是说闲话)
	* [2. 1 OS 篇](#2-1-os-篇)
	* [2. 2 Browser 篇](#2-2-browser-篇)
		* [2. 2. 1 chrome 插件分享(基于 chromium 开发的浏览器应该都通用)](#2-2-1-chrome-插件分享基于-chromium-开发的浏览器应该都通用)
	* [2. 3 IDE 篇](#2-3-ide-篇)
	* [2. 4 SE 篇](#2-4-se-篇)
* [3. 动机(其实就是说骚话)](#3-动机其实就是说骚话)
* [4. 结语](#4-结语)

<!-- /code_chunk_output -->

## 0. 前言

### 0. 1 主旨

**本文假设, 读者有前端基础, 并且了解前端`模块化`编程**

**本文旨在, 读者能以最快速度搭建出可用的react开发环境, 不涉及细节讲解, 细节请读者在实践中慢慢了解**

**本文是对网上现有的`快速开始`(quickly start)的整合, 因为这很`模块化`**

**本文以 Q&A 的格式, 便于记忆和查询, 基本套路是: `这是啥?` `怎么快速开始?` `注意事项` 以及 `官方文档`**

**图自网皆侵删**

### 0. 2 技术栈

> 现在的前端开发环境一般是基于 npm + webpack 搭建的. npm 负责装包, webpack 负责打包.
> 接下来会通过一些成熟的攻略让大家`快速开始`起来作者已经将【着重】部分标注出来, 请务必去实践. 其他均为扩展阅读.
> **一定要边看边跟着做**  
> **一定要边看边跟着做**  
> **一定要边看边跟着做**  
> happy hacking

---

## 1. 正文

### 1. 1 npm 篇

**<font color="#c00000">Q: 什么是 npm?</font>**

> Npm 是 JavaScript 的包管理器和世界上最大的软件注册表。 发现可重用代码的包, 并以强大的新方式组装它们.
>
> > 摘自 **[官网](https://www.npmjs.com/)**

**<font color="#c00000">Q: 如何快速开始?</font>**

**[戳这里【着重】](https://blog.csdn.net/qq_26562641/article/details/72235585)**

**<font color="#c00000"> Q: win10 出现 2503 权限不足?</font>**

> **[参考这个](https://blog.csdn.net/m075097/article/details/74910372)**

**<font color="#c00000"> Q: npm 常用命令</font>**

> **[参考这个【着重】](https://blog.csdn.net/m075097/article/details/74910372)**

### 1. 2 webpack 篇

**<font color="#c00000"> Q: 什么 webpack?</font>**

> 本质上，webpack 是一个现代 JavaScript 应用程序的静态模块打包器(module bundler)。当 webpack 处理应用程序时，它会递归地构建一个依赖关系图(dependency graph)，其中包含应用程序需要的每个模块，然后将所有这些模块打包成一个或多个 bundle。
>
> > 摘自 **[官网](https://www.webpackjs.com/concepts/)**

**<font color="#c00000"> Q: webpack 怎么快速开始?</font>**

> **[入门篇【着重】](https://www.jianshu.com/p/42e11515c10f)**
> 这篇攻略是基于`webpack 3.10.0` 写的.
> 笔者整理的时候已经是`webpack 4.5.0`
 > **[区别看这里](https://github.com/webpack/webpack/releases)**
 > **[官中文档](https://www.webpackjs.com/concepts/)**

### 1. 3 脚手架篇

**<font color="#c00000"> Q: 什么是脚手架? </font>**

> 以下是个人理解
>
> > 简单来说, 使用 npm + webpack 搭建环境就像自己配一台**组装机**, 而用脚手架搭就比较像厂商配好的**品牌机**
> >
> > |          | npm + webpack |  第三方脚手架  |
> > | :------- | :-----------: | :------------: |
> > | 自由度   |      高       | 根据第三方而定 |
> > | 性能     |  熟练度而定   |   第三方负责   |
> > | 时间成本 |  熟练度而定   |    开箱即用    |

> **所以应自己根据具体需求选择相应的方法.
> 下面介绍 react 方向的两个脚手架**

#### 1. 3. 1 create-react-app

**<font color="#c00000"> Q: 如何安装? 如何使用? </font>**

> **[官方 repo 地址](https://github.com/facebook/create-react-app)**
 > **<font color="#c00000">win10 请注意: </font>**
> 笔者于 2018-04-14, `npm 5.8.0`版本下, 测试官网推荐的 npx 命令, 发现其在 win10 平台上无法运行.官方还未给出正式修复补丁.
>
> > 所以请用`cnpm i -g create-react-app`安装
> > `create-react-app my-deom` 来创建项目

**<font color="#c00000"> Q: 什么? 你问啥是 npx? </font>**

> **[看这里](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)**

#### 1. 3. 2 dva-cli

**<font color="#c00000"> Q: 如何安装? 如何使用? </font>**

> **[官方 repo 地址](https://github.com/dvajs/dva-cli)**
 > **<font color="#c00000">请注意: </font>**
>
> > 笔者整理时 dva-cli 的版本还是`dva-cli 0.9.2`
> > 可用`cnpm i -g dva-cli@next`
> > 以获取`dva-cli version 1.0.0-bea.2` 可以提升体验.
> > 二者的主要区别在 **[这里](https://github.com/sorrycc/blog/issues/66)**

---

## 2. 个人易用性的一些心得分享(其实就是说闲话)

### 2. 1 OS 篇

**略**
因为笔者已经习惯了 Windows
没有也不打算去填 linux 和 Mac 的坑,

**个人观点:** 用自己习惯的就行了.
毕竟长年积累下来使用经验有益于体验和错误排查.

### 2. 2 Browser 篇

前些年前端框架还没有那么火, 浏览器之间的差异很容易产生各种奇妙的问题, 近年由于前端框架的火爆, 应对浏览器之间的差异已经被框架替你给做好了, 所以也不多赘述.

**<font color="#c00000"> Q: 怎么选择浏览器?</font>**

> 理论上除了 IE 都能拿来用笔者比较喜欢 Chrome(需要科学上网)

**<font color="#c00000"> Q: 为什么不推荐使用 IE</font>**

> ![日常黑IE](https://gss0.baidu.com/9vo3dSag_xI4khGko9WTAnF6hhy/zhidao/pic/item/aa18972bd40735fa67d1258d9d510fb30f2408e4.jpg)

#### 2. 2. 1 chrome 插件分享(基于 chromium 开发的浏览器应该都通用)

**[【基于 chromium 开发的浏览器一览】](https://www.oschina.net/news/16890/browsers-based-on-chromium)**

**React dev tools**
**[下载](https://chrome-extension-downloader.com/b351e6906b2853ea7c744c69174ad47f/https://chrome.google.com/webstore/detail/fmkadmapgofadopljbjfkapdkoienihi.crx)**
**[使用方法](https://github.com/facebook/react-devtools)**

**Redux dev tools**
**[下载](https://chrome-extension-downloader.com/d4e3610449e1134522f6364e614ed0f4/https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd.crx)**
**[使用方法](https://github.com/zalmoxisus/redux-devtools-extension)**

**Restlet Client**
**[下载](https://chrome-extension-downloader.com/c94cf075bc4df0e3a6d2e66c7980ff5f/https://chrome.google.com/webstore/detail/aejoelaoggembcahagimdiliamlcdmfm.crx)**
**[使用方法](https://restlet.com/documentation/client/user-guide/introduction)**

### 2. 3 IDE 篇

**笔者的策略是: 装两个, 一个用于开会展示时便于大家操作; 另一个自己习惯的, 理由同 OS 篇**.

笔者的 IDE 是`VSCODE`
**[配置仅供参考](https://gist.github.com/NgeKaworu/38b51b333113927aa3ffdf5c23c2ea07)** (需要科学上网)

### 2. 4 SE 篇

> 倘内事不决可问百度, 外事不决可问谷歌.
> 可惜谷歌必须科学上网了, 遥想谷歌当年啊.

**<font color="#c00000"> Q: 其他的不说下吗?</font>**

> ![对方不想说话,并且向你扔了一张图片](http://ws2.sinaimg.cn/mw600/82e98952gy1fqa5ki2udmj20u00imdiq.jpg)

---

## 3. 动机(其实就是说骚话)

一开始让我整理篇 web 前端开发环境攻略时, 其实我是拒绝的, 因为真的没什么好写的.

前端开发没有什么大型的 IDE 需要搭建, 也不用装什么运行库

简单说前端开发环境, 其实只需要 OS + notepad + browser 就 OK 了

刨去繁琐的 OS 和 browser 层, 用于提升易用性扩展配置

打开 notepad, 输入 Hello World, 保存, 把后缀名改成 html, 用 browser 打开, 就已经完成了最简单的前端开发了.

~~是的, 没错. 关于前端开发环境的搭建, 到这里就结束了. 谢谢大家的阅读. 再见. 欸! 欸! 欸! 那位带刀的大哥, 你先把 🔪 放下, 我认为这是人民内部的矛盾, 没有什么是不能慢慢讲的嘛.~~

仔细想了想我学前端的经历, 一开始是用 CDN 把 react 库直接引用到`<body>`标签的尾巴处

怎么突然之间就开始用 import require 了呢? emmmm... 思索了半天.

隐约的想起了这么一句话:

> **我安几个包去, 你就在此地, 不要走动**

顿时 一个轮廓从我的脑海中慢慢显现, 那就是 ——

##Nodejs {ignore=true}

下面的

#NPM {ignore=true}

---

## 4. 结语

本文到这里就结束了, 感谢收看.

笔者其实是先入的 ES6 坑, 才去了解的模块化 JS 编程, 起初只是觉得这个写法跟 include 很像, 所以很自然就会用了.

> **[延伸阅读 commonJS 模块化历史](https://github.com/seajs/seajs/issues/588)**

好了, 其实笔者并不懂前端, 我只是给 github 做搬运的. 前面都是我编的, 我实在编不下去了.
