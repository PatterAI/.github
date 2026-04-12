<div align="center">

  <img src="https://raw.githubusercontent.com/PatterAI/Patter/main/docs/patter-logo-banner.svg" alt="Patter" width="400" />

  **The open-source Voice AI SDK**

  *by [Patter](https://getpatter.com)*

  [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/PatterAI/Patter/blob/main/LICENSE)
  [![Python](https://img.shields.io/pypi/v/patter?label=Python%20SDK)](https://pypi.org/project/patter/)
  [![npm](https://img.shields.io/npm/v/@patter-dev/sdk?label=TypeScript%20SDK)](https://www.npmjs.com/package/@patter-dev/sdk)
  [![GitHub Discussions](https://img.shields.io/github/discussions/PatterAI/Patter)](https://github.com/PatterAI/Patter/discussions)

  </div>

  ---

  🔊 **Patter is the open-source way to connect any AI agent to real phone calls.** Build voice-powered agents with a few lines of code — without managing telephony,
  speech pipelines, or audio infrastructure.

  Visit the [Patter docs](https://getpatter.com) to get started.
  SDK: [Python](https://github.com/PatterAI/Patter/tree/main/sdk) / [TypeScript](https://github.com/PatterAI/Patter/tree/main/sdk-ts)

  ## 🧐 What is Patter?

  Patter is a dual SDK (Python + TypeScript) that gives developers a unified API for the entire voice AI pipeline — speech-to-text, AI reasoning, text-to-speech, and
  telephony — wired together with sub-second latency so your agent sounds natural on a real phone call.

  ## ✨ Just like this

  ```python
  import asyncio
  from patter import Patter

  async def main():
      phone = Patter(
          openai_key="sk-...",
          phone_number="+15550001234",
          webhook_url="your.server.com",
      )

      agent = phone.agent(
          system_prompt="You are a friendly booking assistant for a dental clinic.",
          voice="nova",
          first_message="Hi! I'm calling from Smile Dental. How can I help?",
      )

      await phone.serve(agent, port=8000)

  asyncio.run(main())
```

  🚀 Key Features

  - 📞 Inbound & Outbound Calls — answer calls or dial out programmatically with Twilio or Telnyx
  - ⚡ 3 Voice Modes — OpenAI Realtime (lowest latency), Pipeline (custom STT+TTS), ElevenLabs ConvAI
  - 🔧 Tool Calling — let your agent check databases, book appointments, or transfer calls
  - 📊 Built-in Dashboard — real-time call monitoring, cost tracking, and analytics
  - 🧪 Test Mode — develop agents in your terminal, no phone needed
  - 💰 Per-Call Metrics — cost breakdown by provider (STT, TTS, LLM, telephony) with latency percentiles
  - 🛡️ Guardrails — content filtering and blocked terms before speech output
  - 🏠 Local Mode — runs entirely on your machine, no cloud dependency
  - 🤖 Any LLM — pluggable LLM loop, bring your own Anthropic, Gemini, or any provider

  🏁 Getting Started

  - 📥 Installation — install the SDK and set up your environment
  - 📖 Documentation — full guides for Python and TypeScript
  - 💬 Discussions — ask questions and share what you've built
  - 🐛 Issues — report bugs or suggest features
