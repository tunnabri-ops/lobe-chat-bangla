# 💬 Lobe Chat Bangla

**A self-hosted Bangla AI chat — 6 ready Bangla assistants, running on your own machine with Docker.**

## ✨ Features

- `docker-compose.bangla.yml` — runs the chat on http://localhost:3210.
- `bangla-assistants.json` — 3 ready assistants: **বাংলা শিক্ষক** (tutor), **বাংলা লেখক** (writing helper), **কোড বন্ধু** (coding helper that explains in Bangla).
- `bangla-assistants-extra.json` — 3 more: **খবর সারাংশ** (news summarizer), **পরীক্ষা প্রস্তুতি** (SSC/HSC exam prep), **স্বাস্থ্য গাইড** (health guide).

## 🚀 How to use

```bash
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3210. Add a provider key (for example OpenAI) in Settings — or point it at a local Ollama model instead, no key needed. Then create a new assistant and paste one `systemRole` from `bangla-assistants.json`.

## ⚠️ Honest limits

- You need a provider key or a local model — the chat UI alone does not answer without a model behind it.
- Your chats live in the container unless you add your own volume — the compose file does not invent a storage path for you.
- The assistants are starter prompts: they guide the model, they do not add new knowledge to it.

## 🇧🇩 বাংলা

**লোব চ্যাট বাংলা — নিজের কম্পিউটারে চলা বাংলা এআই চ্যাট।**

- ডকার দিয়ে এক কমান্ডে চালু হয় — http://localhost:3210
- ৬টা তৈরি বাংলা অ্যাসিস্ট্যান্ট: শিক্ষক, লেখক, কোড বন্ধু, খবর সারাংশ, পরীক্ষা প্রস্তুতি, স্বাস্থ্য গাইড
- চাবি (API key) থাকলে সেটা দিয়ে, না থাকলে লোকাল Ollama মডেল দিয়ে চলবে

## 📄 License

MIT — use it however you like.
