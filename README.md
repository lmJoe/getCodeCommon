# getCodeCommon
微信公众号自定义网页授权获取code
配置回调函数 我们在微信客户端访问第三方网页（即我们自己的网页）的时候，我们可以通过微信网页授权机制，我们不仅要有前面获取到的appid和appsecret还需要有当用户授权之后，回调的域名设置，即用户授权后，页面会跳转到哪里。
![](https://raw.githubusercontent.com/lmJoe/gitAllImg/main/images/%E7%AC%AC%E4%B8%80%E6%AD%A5.jpg)
填写回调域名，如下图
![](https://raw.githubusercontent.com/lmJoe/gitAllImg/main/images/%E7%AC%AC%E4%BA%8C%E6%AD%A5.jpg)
![](https://raw.githubusercontent.com/lmJoe/gitAllImg/main/images/%E7%AC%AC%E4%B8%89%E6%AD%A5.jpg)
请求获取code的参考链接
https://open.weixin.qq.com/connect/oauth2/authorize?appid=appid&redirect_uri=https://域名/wechattransfer.html&response_type=code&scope=snsapi_userinfo&state=https://域名/index.html#wechat_redirect
其中REDIRECT_UR为urlEncode编码之后的 
`https://域名/index.html`是授权后会跳转的地址,在这个页面中会解析路径参入从而进入`https://域名/index.html`

下载index.html之后配置在你的服务器上，在微信授权下的域名能够访问到
`https://域名/index.html`是要进入的页面
带参数链接
https://open.weixin.qq.com/connect/oauth2/authorize?appid=wx16a3abc5b33035cf&redirect_uri=https://static-quickvideotest.29293.com/qkv2/phone.html?code=A18772119&apkType=7003&response_type=code&scope=snsapi_userinfo&state=https://static-quickvideotest.29293.com/qkv2/phone.html?code=A18772119&apkType=7003#wechat_redirect
不带参数链接
https://open.weixin.qq.com/connect/oauth2/authorize?appid=wx16a3abc5b33035cf&redirect_uri=https://static-quickvideotest.29293.com/qkv2/phone.html&response_type=code&scope=snsapi_userinfo&state=https://static-quickvideotest.29293.com/qkv2/phone.html#wechat_redirect


使用微信开发工具访问上面参考链接，最后会进入下面链接，同时带上code
https://域名/index.html?code=0014rK302cHWcV0w7K502IhK3024rK3u
