[TOC]



文档中关于转发到微信群的内容：

[接口说明](https://mp.weixin.qq.com/debug/wxadoc/dev/component/open-data.html)

[接口说明](https://mp.weixin.qq.com/debug/wxadoc/dev/api/share.html#wxgetshareinfoobject)

[接口说明](https://mp.weixin.qq.com/debug/wxadoc/dev/api/signature.html)



实例：

[实例1](http://wpweixin.com/post/20658/)

[王者荣耀群排名](http://www.wxapp-union.com/article-2217-1.html)

[pk步速](http://www.ifanr.com/minapp/867546)

[实例4](https://segmentfault.com/q/1010000011679659 )

[Ajax 进行网络请求（get/post）](https://www.cnblogs.com/smyhvae/p/8485028.html)



[一个前端大佬的GitHub](https://github.com/smyhvae/Web)

[vscode 配置小程序代码提示](https://www.jianshu.com/p/27aaa647c5c5)

## 小程序代码结构说明

**注意：为了方便开发者减少配置项，描述页面的四个文件必须具有相同的路径与文件名**



#### app.json

`app.json` 是当前小程序的全局配置，包括了小程序的所有页面路径、界面表现、网络超时时间、底部 tab 等。QuickStart 项目里边的 `app.json` 配置内容如下：

```json
{
  "pages": ["pages/index/index", "pages/logs/logs"],//描述当前小程序所有页面路径，这是为了让微信客户端知道当前你的小程序页面定义在哪个目录。格式为 路径+文件名，但不需要后缀
  "window": {//定义小程序所有页面的顶部背景颜色，文字颜色定义等
    "backgroundTextStyle": "light",
    "navigationBarBackgroundColor": "#fff",
    "navigationBarTitleText": "WeChat",
    "navigationBarTextStyle": "black"
  }
}
```

#### App.js

`App()` 函数用来注册一个小程序。接受一个 `Object` 参数，其指定小程序的生命周期回调等。

App() 必须在 app.js 中调用，必须调用且只能调用一次。不然会出现无法预期的后果。



### 会话密钥 session_key 有效性

使用接口 [wx.checkSession](https://developers.weixin.qq.com/miniprogram/dev/api/wx.checkSession.html)可以校验 session_key 是否有效，从而避免小程序反复执行登录流程。



## 创建新页面并导航

[创建页面](https://www.jb51.net/article/111375.htm)



## 群分享

那几个函数貌似只能用于小游戏

现在的想法是，使用



使用open-data就可以获得用户的信息，没写后台

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190117194605412.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzAzODYy,size_16,color_FFFFFF,t_70)



# 搭建本地测试

[手把手教你搭建Windows环境微信小程序的本地测试服务器](https://blog.csdn.net/myth13141314/article/details/81303034)



# express

[express API](http://www.expressjs.com.cn/4x/api.html#res) 要常查看

express 的路由是动态的，使用‘：’

对于url中，?xxx=xx,要取出xxx的值，可以使用req.query,显示的是{ xxx:'xx'},若要得到xx，可写req.query.xxx，从这里可以想到，在使用get时，可以使用通过xxx的值来进行参数匹配，用于用户的区分？！



post 有上传文件和上传文字的功能，但两者不一样 

req.body 是数据的主体，可用req.body.xxx来引用数据

app.use(bodyParser.xxx));,需要在项目下使用`npm install body-parser --save` 下载bodyParse



### 文件上传

 `npm insall multer --save`

[Nodejs进阶：基于express+multer的文件上传](https://www.cnblogs.com/chyingp/p/express-multer-file-upload.html)

[Node.js：上传文件，服务端如何获取文件上传进度](https://www.cnblogs.com/chyingp/p/nodejs-multer-how-to-get-upload-percentage.html)

[node.js 开发](http://www.cnblogs.com/chyingp/p/)

### 模板引擎 EJS

用于往静态的htlm嵌入动态的数据，如往返回的html文件嵌入数据库的数据

数组有 `.forEach()` 方法遍历

文件为`.ejs` 后缀



## 中间件

express.static('静态文件夹')，，可访问里面的静态文件，如图片等

app.use()

## 路由重构





## 淘宝源

https://npm.taobao.org

[npm 开源网站](https://www.npmjs.com/)





## 弹幕的搜索资料

[移动](https://www.cnblogs.com/shockw4ver/p/5886771.html)



# end

