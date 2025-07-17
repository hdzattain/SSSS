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
安装依赖

bash
复制
编辑
npm install
配置环境变量

复制示例文件并编辑：

bash
复制
编辑
cp .env.example .env
打开 .env，填写你的 DIFY_API_KEY 等信息。

启动机器人

bash
复制
编辑
npm start
启动后在控制台会出现二维码，扫描登录 WhatsApp。

在群/私聊中发送消息，机器人会把你发的内容发送到 Dify 并返回结构化结果。

项目结构
bash
复制
编辑
.
├── index.js         # 入口脚本
├── package.json
├── .env.example
├── .gitignore
└── logs/            # （可选）消息日志
环境变量
请在项目根目录新建 .env，主要变量：

dotenv
复制
编辑
DIFY_API_KEY=your_dify_api_key
DIFY_BASE_URL=https://api.dify.ai/v1   # 如不修改可以不填
LOG_WHATSAPP_MSGS=true                  # 是否记录收到的 whatsapp 消息到 logs/whatsapp.log
依赖
whatsapp-web.js

axios

form-data

mime-types

dotenv

fs-extra

qrcode-terminal

License
MIT © hdzattain
