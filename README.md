# 使用create-next-app零配置创建React App

自我介绍：青青子衿，悠悠我心，但为前端，沉吟至今。大家好，我叫王朋，来自陆金所大前端工程师，目前负责p2p产品线的前端开发。

本文翻译来自[create-next-app](https://github.com/segmentio/create-next-app)，大家想看原文可以点击此链接或文章下面的【阅读原文】


## 前言

随着时间的推移，构建一个生产级的React应用程序越来越多的依赖Babel和Webpack作为默认的工具链。开发者往往面临难以辨认的配置文件和大量的插件，工具不仅更新快，而且独立变化，教程往往迅速过时。

为了快速地进行构建使用 React 的项目，小编介绍一款无需配置的、用于快速构建开发环境的脚手架工具 create-next-app。

### 使用的原因以及特性

* 无需配置；

* 集成了对 React, JSX, ES6 和 Flow 的支持；

* 集成了开发服务器；

* 配置好了浏览器热加载的功能；

* 在 JavaScript 中可以直接 import CSS 和图片；

* 自动处理 CSS 的兼容问题，无需添加 -webkit 前缀；

* 集成好了编译命令，编译后直接发布成产品，并且还包含了 sourcemaps；

 <img width="600" alt="Create Next App running in terminal" src="https://cloud.githubusercontent.com/assets/20238205/26140120/8c51e07a-3b07-11e7-9bb6-6b16783af8ad.png" />

## 先动手看看效果
执行以下命令创建项目

```sh
npm install -g create-next-app

create-next-app my-app
cd my-app/
npm run dev
```
在浏览器中http://localhost:3000,即可在浏览器看到运行后的结果，并且已经实现了热加载的功能。

当你准备将你的项目部署到生成环境中时，执行`npm run build` 命令 就可以将应用程序压缩打包，然后执行 `npm run start`即可运行项目。

<img width="600" alt="Create Next App running in terminal" src="https://cloud.githubusercontent.com/assets/1026125/25556236/0ac91ca6-2cae-11e7-87ae-bb7974285063.png" />
<img width="600" alt="Create Next App running in terminal" src="https://cloud.githubusercontent.com/assets/1026125/25556240/111fc3b6-2cae-11e7-84b6-961de4fd27f9.png" />


## 快速入门

与Webpack 或 Babel工具相比，你并不需要像他们那样，需要安装大量插件和写大量的配置文件.Create Next App 预先隐藏了配置，这样你就可以只专注于你的代码，而不需要为大量的配置文件而烦恼。

### 安装

全局安装create-next-app


##### `$ npm install -g create-next-app`


#### 要注意的几个点 
* Node 的版本必须 >= 4，推荐 Node >= 6 and npm >= 3，另外，你可以使用[nvm](https://github.com/creationix/nvm#usage)在不同的项目直接切换node版本。

* 运行起来后浏览器已经实现了热加载刷新，修改代码保存后浏览器会自动刷新；

* 你不需要使用node 作为你的主要后端。node 安装仅仅是为了在开发和生成环境中使用create-next-app和 运行Next.js。


###创建App

要想创建一个新的app,执行下面命令，即在当前目录下创建了一个名为my-app 的目录。

##### `create-next-app my-app`



执行cd my-app进入my-app目录，在my-app 目录中，你就会发现已经生成的项目结构，并且已经安装了必要的依赖项，如下图所示。

```
my-app/
  components/
    head.js
    nav.js
  node-modules
  pages/
    index.js
  static/
    favicon.ico
  .gitignore
  next.config.js
  package.json
  README.md

```  


* Next.js使用[filesystem作为API](https://zeit.co/blog/next#zero-setup.-use-the-filesystem-as-an-api)，所以每个放到pages文件夹中的组件将会自动映射为一个基于服务器的路由。比如，磁盘上的`pages/about.js`组件将会自动服务于`/about`这个URL。`./pages/index.js` 文件将会自动映射为 `/`。

* `./static` 在next服务中将直接映射到`./static` ，因此，你可以所有的静态资源，如图片、编译的CSS放在里面。

* 总结:我们发现在构建app时，没有做大量的配置，也没有复杂的文件夹结构，一旦安装成功，你就可以在你的项目目录中运行一些命令来构建一个App。

### 开发模式下运行
在开发模式下执行下面命令命令，然后打开http://localhost:3000 就可以在浏览器中看到运行效果,如下图所示:。

##### `npm run dev` or `yarn dev`

一旦修改代码，页面就会重新刷新加载。

在项目构建中，你可以在终端中看到构建中的错误和警告。
![react2](https://cloud.githubusercontent.com/assets/20238205/26141459/9432721c-3b0e-11e7-9f44-043bcf7514f0.png)

### 生产打包

执行下面命令就可以把应用程序优化、压缩、打包到生产环境的.next目录。

##### `npm run build` or `yarn build`
### 生产模式下运行

##### `npm run start or yarn start`
只有执行`npm run build`命令，成功编译后，你的应用程序才能够在生产模式下成功的运行。

现在你已经准备好了代码和部署你的应用程序！
## 从实例出发
点击这里[Next.js repo](https://github.com/zeit/next.js/tree/master/examples/) 
有大量的实例供你学习参考，通过实例可以快速引导你构建应用程序。

举个例子:

1. 进入 [https://open.segment.com/create-next-app#examples
](https://open.segment.com/create-next-app#examples)

2. 通过名称搜索你需要的例子(如 `basic-css`)

3. 运行: `create-next-app --example basic-css example-app`

4. 完成 💥


## 好文回顾

[Opera 涅磐重生，华丽归来](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483850&idx=1&sn=abcff21a05f9b1e9144868dbcb26abb7&chksm=9b6b895eac1c00485fe16e7cf45427257e961b85ec46a08edd05ae4a5d54a17a7350e6ecd9c6&scene=0#rd)

[Spring云数据流1.2 RC1发布](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483850&idx=2&sn=e3e388a0a389fff7e9f369678910da84&chksm=9b6b895eac1c0048446ae870a21a872891c161be0bca38d07f2405e4b4000d756d2e83ea5a85&scene=0#rd)

[Temper Chrome 一款好用到飞起的HTTP请求修改插件](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483847&idx=1&sn=26a5125537d81324bfc1b38a3364d8bc&chksm=9b6b8953ac1c00459029c4f0e6f9cde42034825a224c3d4f7a2f1e5d4e146284d56df21e970e&scene=21#wechat_redirect)

[chroma.js 交互式色彩空间资源管理器](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483831&idx=1&sn=8133126f3749ac28a1d72bda1cb96d5a&chksm=9b6b8923ac1c0035824a1af20164006ecd6b56833eb904f2004869f6eb207b25f59c976267ac&scene=21#wechat_redirect)

[MoveTo，一款无依赖、轻量级的滚动插件](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483821&idx=1&sn=ab2b9405d4c269afcb48f53dbd53bbef&chksm=9b6b8939ac1c002f37af9242bff8140e7d6515f71df9598789011826d935d5aeab57d4bb72d1&scene=21#wechat_redirect)

[没有程序员鼓励师？我们可以自己造一个啊](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483817&idx=1&sn=1f1e3fc4c54f2cea1eac9a2e5bbba7de&chksm=9b6b893dac1c002b4ab5f38c26609ad88b9608c96c6a882004397c23ea1be945af7be60f5bcd&scene=21#wechat_redirect)

[CSS 网格的春天](http://mp.weixin.qq.com/s?__biz=MzAwODcwODYwMw==&mid=2247483847&idx=1&sn=26a5125537d81324bfc1b38a3364d8bc&chksm=9b6b8953ac1c00459029c4f0e6f9cde42034825a224c3d4f7a2f1e5d4e146284d56df21e970e&scene=21#wechat_redirect)

如对其他文章感兴趣，可以关注大前端工程师</br>

![weixinhao](https://cloud.githubusercontent.com/assets/20238205/26142454/2d2b04bc-3b13-11e7-85d4-cf6d5277722c.png)
