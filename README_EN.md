<div align="right">

[**🇺🇸 English**](./README_EN.md) | [**🇨🇳 中文说明**](./README.md)

</div>

# 🌍 Unified LLM Gateway: OpenAI, Claude, Gemini & Grok

[![Status](https://img.shields.io/badge/Status-Production-success)](https://okrouter.com)
[![Integration](https://img.shields.io/badge/Integration-OpenAI%20Compatible-blue)](https://okrouter.com)
[![Payment](https://img.shields.io/badge/Payment-Crypto%20%2F%20Card-orange)](https://okrouter.com)

> **🚀 One API Key, All Models.**
> Stop managing multiple billing accounts and SDKs. Access **GPT-5, o4, Claude 4.5, and Gemini 3** through a single, standardized OpenAI-compatible interface.

## ⚡ The "All-in-One" Solution for Developers

Building AI apps today is fragmented. You have to deal with OpenAI's API, Anthropic's specific SDK, and Google's complex setup.

**[OKRouter](https://okrouter.com)** unifies them all.

* **Standardized:** Use the `openai` python/node library for EVERYTHING (including Claude & Gemini).
* **Efficient:** Switch models by changing just one string (`model="claude-4.5"`).
* **Flexible:** Pay with **Crypto (USDT)** or Credit Card. No monthly subscriptions, pay-as-you-go.

👉 **[Get Your API Key](https://okrouter.com)**

---

## 💎 Supported Models (2025)

| Provider | Model ID (Use this in code) | Why use it? |
| :--- | :--- | :--- |
| **OpenAI** | `gpt-5` / `openai-o4` | Top-tier reasoning & logic. |
| **Anthropic** | `anthropic/claude-4.5-sonnet` | Best for coding & complex architecture. |
| **Google** | `google/gemini-3-pro` | Massive context window for document analysis. |
| **xAI** | `grok-3` | Real-time knowledge & uncensored output. |

---

## 🛠️ Integration (Drop-in Replacement)

You don't need to rewrite your code. Just change the `base_url`.

### 🐍 Python Example (Using standard OpenAI SDK)

```python
from openai import OpenAI

client = OpenAI(
    # 1. Use OKRouter Endpoint
    base_url="[https://api.okrouter.com/v1](https://api.okrouter.com/v1)",
    # 2. Use your OKRouter Key
    api_key="sk-okrouter-YOUR_KEY"
)

# ✨ Access Claude 4.5 using the OpenAI SDK!
# No need to install 'anthropic' SDK.
response = client.chat.completions.create(
    model="anthropic/claude-4.5-sonnet",
    messages=[{"role": "user", "content": "Write a snake game in Python."}]
)

print(response.choices[0].message.content)
🌐 Node.js ExampleJavaScriptimport OpenAI from 'openai';

const openai = new OpenAI({
  baseURL: '[https://api.okrouter.com/v1](https://api.okrouter.com/v1)',
  apiKey: 'sk-okrouter-YOUR_KEY',
});

// Switch to Gemini instantly
const completion = await openai.chat.completions.create({
  messages: [{ role: 'user', content: 'Analyze this data.' }],
  model: 'google/gemini-3-pro',
});
🛡️ Why use OKRouter over Direct APIs?FeatureOKRouterDirect ProvidersIntegrationOne SDK for AllMultiple incompatible SDKsBillingSingle Wallet (Crypto/Card)Multiple Credit Card BillsPrivacyEmail Only (No Phone Req)Phone Verification RequiredSpeedEnterprise RoutingStandard Latency🔗 LinksDeveloper Dashboard: https://okrouter.comPricing & Limits: https://okrouter.com/pricing🔍 KeywordsLLM Aggregator, Unified AI API, OpenAI Compatible Gateway, Buy GPT-4 with Crypto, Claude 4.5 API Key, No KYC AI, AI Middleware, Developer Tools.
