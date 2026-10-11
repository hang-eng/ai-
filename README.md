# AI 智能伴侣

一个基于 Streamlit + DeepSeek 的 AI 聊天伴侣应用。可以自定义伴侣的昵称和性格，支持多会话管理、流式输出，聊天记录本地保存。

> 这是一个个人学习项目，用来练习 Streamlit 和调用大模型 API，并非生产级应用。

## 功能

- 自定义伴侣昵称与性格，通过系统提示词塑造人设
- 微信风格的简短回复，支持 emoji
- 流式输出，边生成边显示
- 多会话管理：新建、切换、删除会话
- 聊天记录以 JSON 保存在本地 `session/` 目录

## 环境要求

- Python 3.9+
- 一个 DeepSeek API Key（在 https://platform.deepseek.com 申请）

## 安装

```bash
pip install -r requirements.txt
```

## 配置 API Key

代码通过环境变量 `DEEPSEEK_API_KEY` 读取密钥，不要把密钥写进代码里。

Windows CMD：

```cmd
set DEEPSEEK_API_KEY=你的密钥
```

Windows PowerShell：

```powershell
$env:DEEPSEEK_API_KEY="你的密钥"
```

macOS / Linux：

```bash
export DEEPSEEK_API_KEY=你的密钥
```

## 运行

```bash
streamlit run AI智能伴侣.py
```

浏览器会自动打开 `http://localhost:8501`。

## 使用说明

- 在左侧「伴侣信息」里修改昵称和性格，立刻生效
- 点「新建会话」开始一段新对话，旧会话自动保存
- 点会话历史里的条目切换会话，点 ❌ 删除

## 项目结构

```
.
├── AI智能伴侣.py       # 主程序
├── requirements.txt    # 依赖清单
├── .gitignore
└── session/            # 会话记录（本地生成，已被 git 忽略）
```

## 说明

- `session/` 目录里保存的是明文聊天记录，已加入 `.gitignore`，不会被提交
- 本项目仅用于学习和交流

## License

MIT
