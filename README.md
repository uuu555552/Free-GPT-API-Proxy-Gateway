<div align="right">

[**🇺🇸 English**](./README_EN.md) | [**🇨🇳 中文说明**](./README.md)

</div>

# ⚡️ OpenAI & Claude API Proxy Gateway (国内加速/防封)

[![Status](https://img.shields.io/badge/Status-Stable-success)](https://okrouter.com)
[![Proxy](https://img.shields.io/badge/Proxy-High%20Speed-blue)](https://okrouter.com)
[![Latency](https://img.shields.io/badge/Latency-30ms-green)](https://okrouter.com)

> 🛑 **停止寻找 Nginx 配置！**
> 你不需要自己购买服务器搭建反向代理。本项目提供**企业级 API 转发网关**，一行代码解决 `Connection Refused` 和 `Region Not Supported` 问题。

## 🚀 核心价值：解决连接痛点

在中国开发 AI 应用，你是否遇到过：
1.  `openai.APIConnectionError`: 连接超时？
2.  `Error 403`: 您的 IP 被 OpenAI/Claude 封禁？
3.  `Credit Card Declined`: 无法绑定国外信用卡？

**[OKRouter.com](https://okrouter.com)** 是最终解决方案。我们提供兼容 OpenAI 协议的 **API Gateway**，自动路由到全球最快的节点。

👉 **[获取加速 API Key / Get Proxy Key](https://okrouter.com)**

---

## ⚙️ 接入配置 (Infrastructure Setup)

只需将官方 API 域名替换为我们的加速域名即可。

### 1. 基础信息
* **加速接口 (Base URL):** `https://api.okrouter.com/v1`
* **API Key:** `sk-okrouter-你的密钥` (在官网注册)

### 2. 在常用框架中使用

#### 📦 Curl (命令行测试)
```bash
curl [https://api.okrouter.com/v1/chat/completions](https://api.okrouter.com/v1/chat/completions) \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer sk-okrouter-你的密钥" \
  -d '{
    "model": "gpt-4o",
    "messages": [{"role": "user", "content": "Ping!"}]
  }'
🦜 LangChain (Python)Pythonfrom langchain_openai import ChatOpenAI

# 直接替换 base_url 即可实现加速
llm = ChatOpenAI(
    model="gpt-4o",
    openai_api_key="sk-okrouter-你的密钥",
    openai_api_base="[https://api.okrouter.com/v1](https://api.okrouter.com/v1)"
)

print(llm.invoke("Hello, connection check!"))
🤖 AutoGPT / .env 配置如果你在使用开源项目（如 AutoGPT, MetaGPT），通常只需要修改 .env 文件：Ini, TOML# .env file
OPENAI_API_BASE=[https://api.okrouter.com/v1](https://api.okrouter.com/v1)
OPENAI_API_KEY=sk-okrouter-xxxxxxxx
🛡️ 为什么比自建代理好？对比项OKRouter 网关自建 Nginx 代理稳定性99.99% SLA (多线路负载)⚠️ 经常挂，IP 易被墙防封号企业级号池轮询⚠️ 单账号容易被封成本按量付费 (无月租)💸 VPS 月租 + 维护时间模型支持GPT-5, Claude 4.5, Gemini❌ 只能转 OpenAI🔗 资源链接控制台 (Dashboard): https://okrouter.comAPI 文档: https://okrouter.com/docs服务器状态: https://status.okrouter.com🔍 Search KeywordsOpenAI 接口代理, ChatGPT API 转发, OpenAI Reverse Proxy, Claude API Mirror, API Gateway for LLMs, 解决 OpenAI 连接超时, LangChain Base URL, OpenAI 国内中转.
