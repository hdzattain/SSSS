# WhatsApp‑Dify Bot

一个基于 [whatsapp-web.js](https://github.com/pedroslopez/whatsapp-web.js) + [Dify](https://dify.ai) 的 WhatsApp 机器人示例。  
它支持文本、图片、语音消息转文字，并把消息发给 Dify 工作流，解析最后一次 `workflow_finished` 的输出，再以结构化 JSON 返回给用户。

## 功能

- 扫描二维码登录 WhatsApp  
- 接收文本、图片、语音消息  
- 图片/语音上传 Dify 或转文字  
- 与 Dify 工作流交互，解析 SSE 日志流  
- 自动提取最后一次 `workflow_finished` 并返回 `package_output`

## 快速开始

1. 克隆仓库  
   ```bash
   git clone https://github.com/your‑username/whatsapp‑dify‑bot.git
   cd whatsapp‑dify‑bot
