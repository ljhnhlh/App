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



