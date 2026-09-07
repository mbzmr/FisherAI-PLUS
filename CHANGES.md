# CHANGES

本仓库为 `fisherdaddy/FisherAI`（Apache License 2.0，© 2024 Yoshiki Miura）的派生修改版。
按 Apache License 2.0 第 4(b) 条，以下列出被修改的文件与修改说明。

## 修改文件清单

| 文件 | 修改说明 |
|---|---|
| `manifest.json` | 提升版本号（1.2.0 → 1.4.1） |
| `scripts/side_panel.js` | 新增：对话快照保存/恢复/重绑复制按钮、Markdown 导出、图N→时间映射、时间水印、画面总结逻辑、启动恢复；修改：任务日志 `logEntry` 参数化、上下文隔离；移除：网页/视频翻译按钮处理 |
| `scripts/llm.js` | 新增：历史投影/恢复辅助、思考期防抖落盘、`finish_reason` 截断检测、`max_tokens` 透传、`options` 参数；修改：超时 180s→600s、思考块默认折叠 |
| `scripts/utils.js` | 新增：`getBilibiliVideoInfo`、`fetchBilibiliStoryboardFrames`（含 `pvdata.bin` 权威时间轴解析、宫格裁剪、填充检测）；修改：YouTube 字幕改为优先取自带字幕轨 |
| `scripts/content.js` | 新增：播放器抓帧（视频选择、元数据等待、VideoFrame 抓帧、帧变化校验、体积压缩）；修改：划词翻译功能整体禁用 |
| `scripts/constants.js` | 新增：`VISUAL_SUMMARY_PROMPT`、`ACTION_CAPTURE_VIDEO_FRAMES`、内置模型 `deepseek-v4-flash-vision-exp` 及图像支持列表 |
| `scripts/i18n.js` | 新增：画面总结多语言文案（zh-CN/en/ja/ko/fr/de/ru 七个分节） |
| `side_panel.html` | 新增：画面总结卡片、下载/新聊天按钮、tooltip、分享图标；移除：网页翻译/视频翻译卡片 |
| `css/styles.css` | 新增：下载/新聊天按钮样式 |
| `translations/zh.json` / `en.json` | 新增：导出与画面总结文案 |
| (新增) `README.md` / `CHANGES.md` | 本仓库文档 |

## 打包说明

可按原作者 README 的打包命令生成分发 zip：
`zip -r dist/fisherai.zip manifest.json background.js css images popup public scripts settings.html side_panel.html styles translations`
