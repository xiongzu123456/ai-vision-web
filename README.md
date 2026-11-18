# AI视觉点击 · 网页版

浏览器里运行的版本：填自己的 API 站点/密钥/识图模型，发网址读正文并总结，或上传手机截图让模型给出下一步点击位置与动作 JSON。

- 直接看页面：https://htmlpreview.github.io/?https://github.com/xiongzu123456/ai-vision-web/blob/main/index.html
- 建议在手机或电脑浏览器打开，右上角「设置」里填接口即可使用

## 边界（不假装能做的事）

浏览器沙箱不允许操作其他应用，所以网页版**不能模拟点击手机屏幕**。真正执行点击要用安卓版 APK（无障碍服务 + 手势注入）。网页版负责「读网页 / 看截图 / 出方案」。

## 抓网页的跨域问题

浏览器直连任意站点会被 CORS 拦。页面默认走一个公共 CORS 代理（`https://api.allorigins.win/raw?url=`），可在设置里换成自己的代理，否则读网页会失败。

## 想让它变成正式站点

仓库 Settings → Pages → Source 选 `main` / root，保存后即得到 `https://xiongzu123456.github.io/ai-vision-web/`。
