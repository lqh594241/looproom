# Looproom

第 3 个英文工具站，源码独立，无运行依赖或付费 API。双击 `index.html` 可用。本站：Audio Speed Changer, AB Loop Player & Metronome。

## 本地与构建

无需 npm install。安装 Node.js 后：

```
npm run dev
npm test
npm run build
```

本地地址：http://127.0.0.1:4175。构建输出 `dist`。

## 部署

建议单独 GitHub 仓库，上传本目录内容。Cloudflare Pages：框架 None，构建命令 `npm run build`，输出目录 `dist`。同仓库部署时根目录设为 `looproom`。Workers 静态资源目录同样为 `dist`，使用控制台提供的静态资源部署配置。

生产环境设置 `SITE_URL=https://实际域名`（不要路径），构建生成该域名的 canonical、og:url、sitemap 和 robots sitemap 地址。未设置不编造域名。

## 广告与统计

`ads.js` 已接入本次提供的 Looproom 专属 HilltopAds 横幅与弹窗链接。顶部全宽横幅正常占位，可用 × 关闭，不悬浮；空广告位或加载失败时折叠，手机上按可用宽度缩放。

首次真实点击 `#play`（播放）、`#metronome`（节拍器）或 `#export-loop`（WAV 导出）时尝试打开广告新标签页，每次页面加载最多一次，不拦截原功能。文件选择、停止、AB 设置、导航和关闭横幅不触发；禁用按钮及脚本模拟点击不触发。浏览器可能限制弹窗，不会反复重试。

所有页面保留现有 Ahrefs Web Analytics 和验证代码，不重复加载。广告仅在工具首页启用，隐私说明已更新。构建会自动包含 `ads.js`，广告填充和内容由平台控制。

## 范围

Local audio playback with browser pitch preservation, pitch-linked playback, approximate AB looping, a separate synthesized metronome, and original-speed PCM WAV selection export. No independent pitch shifting or processed-speed export. Files are limited to 25 MB and 10 minutes; WAV selections to 120 seconds.

没有验证关键词的真实搜索量、竞争度或收益，不承诺收录、排名或 AI 引用。英文静态页面提供公式、使用说明、限制、FAQ、隐私与条款。
