VLESS项目

[![](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/likeflowercome/lessthan.git)


类型：VLESS协议

端口：443

路径：/vless

传输协议：ws

安全类型：tls

加速脚本代码：
```
addEventListener(
  "fetch",event => {
  let url=new URL(event.request.url);
  url.hostname="替换成自己的Heroku域名地址";
  let request=new Request(url,event.request);
  event. respondWith(
  fetch(request)
  )
  }
  )
```