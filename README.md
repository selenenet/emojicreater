# EmojiReactor for Kettu — GitHub Pages 发布文件

此目录是可直接上传到新 GitHub 仓库根目录的静态站点。`manifest.json` 和 `index.js` 必须与 `index.html` 位于同一层。

上传到 [selenenet/emojicreater](https://github.com/selenenet/emojicreater) 后，在仓库 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**，选 `main` 分支和 `/(root)`，保存。等待 GitHub Pages 发布后，在 Kettu **设置 → Plugins → +** 中粘贴站点根网址：

```text
https://selenenet.github.io/emojicreater/
```

末尾保留 `/`。手机浏览器先访问 `https://selenenet.github.io/emojicreater/manifest.json`，确认可以看到 JSON，再到 Kettu 安装。

此目录不含 Discord Token、频道配置、账号资料或本机路径。请勿上传本机 `%APPDATA%\Vencord\settings`、个人导出配置或 Discord 日志。配置应由每位使用者在 Kettu 中自行填写。

设置页内有诊断计数：收到事件、匹配消息、尝试请求和请求成功，以及最近一次跳过原因。更新插件后若反应未触发，先查看这几项，无需提供消息正文或 Token。

2026-09-23 更新：修正手机端 Discord HTTP 模块的查找与 `put(url)` 调用方式。插件仍通过 Discord 客户端模块处理认证，不读取 Token。

诊断栏现在还显示最近事件的频道 ID、作者 ID、bot/Webhook 标记，以及实际保存的频道与白名单，便于排查配置没有保存或事件来源不一致的问题。不会记录消息正文。

所有频道事件与目标频道事件分别计数，其他频道的消息不会覆盖目标频道的最近处理结果。

安装本身无需将 Kettu 源码也传到 GitHub。GitHub Pages 只是提供 Kettu 下载本插件的两个静态文件。
