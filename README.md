# Lobe Chat Bangla — বাংলায় AI চ্যাট

Bangla-ready self-hosted LobeChat setup, built on **lobehub/lobehub** (formerly `lobehub/lobe-chat`).

- **Original repo:** https://github.com/lobehub/lobehub (LobeHub — super-agents for your team chats; the repo was renamed from `lobe-chat` to `lobehub`, Docker image stays `lobehub/lobe-chat`)

## কী আছে / What is inside

- `docker-compose.bangla.yml` — runs LobeChat on http://localhost:3210 (the port from the upstream README's Docker Compose guide).
- `bangla-assistants.json` — 3 ready Bangla assistants: বাংলা শিক্ষক (tutor), বাংলা লেখক (writing helper), কোড বন্ধু (coding helper that explains in Bangla).

## যা ঠিক করা হয়েছে / What was fixed

- Upstream ships with English-only defaults and no starter assistants. This adds Bangla system prompts and a minimal compose file (image `lobehub/lobe-chat:latest` — verified on Docker Hub, 6.7M+ pulls).
- The compose file does **not** invent a data volume path — upstream's own volume layout is not pinned in its README, so no fake path is included. Your chats live in the container unless you add your own volume.

## ব্যবহার / How to use

```bash
docker compose -f docker-compose.bangla.yml up -d
```

Open http://localhost:3210. Add a provider key (OpenAI, or a local Ollama model) in Settings, then create a new assistant and paste one `systemRole` from `bangla-assistants.json`.
