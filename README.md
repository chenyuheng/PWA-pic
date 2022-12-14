# PWA-pic 可离线显示单图的 PWA 应用

（可用于核酸码）

从 MDN 的 A2HS 示例（[pwa-examples/a2hs at master · mdn/pwa-examples · GitHub](https://github.com/mdn/pwa-examples/tree/master/a2hs)）改造而来，诉求是可以快速调出核酸码（大部分核酸码支持截图使用）。

核酸码使用方法如下，如果需要展示其他的图片可以对应修改 `manifest.webmanifest`、`index.html`、`sw.js` 等文件的相关内容。

## 核酸码使用方法

首先在电脑操作：

1. 克隆或下载本仓库。

2. 将 images/截图.jpg 替换为自己的核酸码或其他需要显示的单图，如果不修改其他文件此文件需要保持同名（截图.jpg）。

3. 在仓库根目录建立 HTTP 服务监听。（可以使用 `python3 -m http.server` 命令调用 python3 自带的 HTTP 服务应用）

4. 在电脑网络设置中找到电脑的内网 IP 地址（一般以 192.168 开头），记录下来。

5. 放开对 HTTP 监听端口的防火墙拦截。（这步不一定需要，可以先不做）

然后在手机端操作：

1. 把手机连入和电脑相同的 Wi-Fi 网络（即连入同一个局域网）。

2. 打开支持 PWA 的浏览器，比如 chrome，在地址栏输入电脑的内网 IP 地址，加上端口号。（如果是 python3 的 HTTP 服务，那么端口号是8000，假如电脑内网 IP 地址是 192.168.100.1，那么总的地址是：http://192.168.100.1:8000/）

3. 进入页面后打开浏览器菜单，选择“添加到主屏幕”，确认选择。

4. 返回桌面，找到新添加的应用，打开并等待加载完成。

5. 退出应用，关闭网络，重新打开应用测试是否可以离线工作。

手机端的操作可以参考本视频：[videos/demo.mp4](https://chenyuheng.github.io/PWA-pic/videos/demo.mp4)


