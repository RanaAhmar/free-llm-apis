# 🚀 Free LLM APIs

> A curated, weekly-updated list of free Large Language Model (LLM) APIs, rate limits, and code samples for modern AI engineers. 

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)]()
[![Updated Weekly](https://img.shields.io/badge/Updated-Weekly-orange.svg)]()

Finding completely free, robust LLM API access can be tedious. This repository tracks the best available free LLM APIs, including context sizes, rate limits, and language-specific code snippets to get you building in seconds.

## 🌟 The Roster

| Provider | Models | Free Tier Limits | API Compatible | Required |
| --- | --- | --- | --- | --- |
| **Groq** | Llama 3, Mixtral, Gemma | Heavy (Dynamic per model) | OpenAI | API Key |
| **Together AI** | 100+ Open Source Models | $5 Free Credit | OpenAI | API Key |
| **Cohere** | Command R, R+ | 10k req/month | Native | API Key |
| **Google Gemini** | Gemini 1.5 Pro/Flash | 15 RPM / 1M TPM | Native | API Key |
| **OpenRouter** | 20+ Free Models | Dynamic routing | OpenAI | API Key |
| **HuggingFace**| Llama 3, Zephyr, various | Rate limited per IP | Custom | Access Token |

---

## 💻 Quick Start Code Samples

### 1. Groq (OpenAI Compatible)
Groq provides LPU-accelerated inference for incredibly fast AI responses. Note that their API is OpenAI-compatible.

```javascript
import OpenAI from "openai";

const groq = new OpenAI({
  apiKey: process.env.GROQ_API_KEY,
  baseURL: "https://api.groq.com/openai/v1",
});

async function main() {
  const chatCompletion = await groq.chat.completions.create({
    messages: [{ role: "user", content: "Explain quantum computing in one sentence." }],
    model: "llama3-8b-8192",
  });
  console.log(chatCompletion.choices[0].message.content);
}
main();
```

### 2. Google Gemini
Google offers an exceptionally generous free tier for Gemini 1.5 Flash.

```python
import google.generativeai as genai
import os

genai.configure(api_key=os.environ["GEMINI_API_KEY"])
model = genai.GenerativeModel('gemini-1.5-flash')

response = model.generate_content("Write a haiku about artificial intelligence.")
print(response.text)
```

## 🤝 Contributing
Found a new free API? Did a rate limit change? Please submit a PR! We rely on community contributions to keep this list 100% accurate.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewAPI`)
3. Commit your Changes (`git commit -m 'Add New Free API'`)
4. Push to the Branch (`git push origin feature/NewAPI`)
5. Open a Pull Request

---
### 🏢 About Stackaura
This project is proudly maintained backed and sponsored by **[Stackaura](https://www.stackaura.com/)**.
We specialize in building high-performance web applications, scalable SaaS architectures, and premium digital solutions.
👉 **[Visit Stackaura to supercharge your next project!](https://www.stackaura.com/)**
