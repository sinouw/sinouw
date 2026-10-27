# Yassine El Ouni

**Senior AI Engineer | Full-Stack & Cloud — LLM applications, RAG, AI agents, voice AI**

Senior software engineer with **6+ years** shipping production systems for clients in France, the UK and Saudi Arabia, now focused on applied AI: retrieval-augmented generation, tool-using and multi-agent systems on the Model Context Protocol, real-time voice agents and computer vision — measured with evaluation harnesses and tracing, not demos.

[Portfolio](https://yassine-elouni-profile.web.app/) · [LinkedIn](https://www.linkedin.com/in/yassineelouni) · [Email](mailto:yassine.elouni.dev@gmail.com)

---

## Featured projects

Most of my production work is for clients in private repositories. These three public projects show how I build AI systems: each one ships with tests, an eval suite and results from real runs.

### 1. [rag-agent-evals](https://github.com/sinouw/rag-agent-evals) — RAG agent with an evaluation harness

Document question-answering agent: hybrid dense + BM25 retrieval in Qdrant fused with Reciprocal Rank Fusion, cited answers streamed over SSE, and an agent loop with function calling (semantic search, read-only SQL, sandboxed calculator). A 65-question eval harness (Hit@k, MRR, LLM-as-judge correctness and faithfulness, citation precision) drove the retrieval design.

- Answer-passage **Hit@5 76% → 89%**, **MRR 0.55 → 0.72** from metadata cards + hybrid search
- **100%** correctness and faithfulness on the 32-question core set (gpt-oss-120b on Groq)
- A cross-encoder reranker was measured and left off: ~25x the latency
- Per-request OpenTelemetry traces (model calls, tools, tokens, cost) shown as a waterfall in the UI

**Stack:** Python · FastAPI · Qdrant · fastembed · React · TypeScript · OpenTelemetry · Docker

### 2. [mcp-ops-copilot](https://github.com/sinouw/mcp-ops-copilot) — multi-agent platform on MCP

Support-operations copilot: a supervisor and three scoped agents act only through self-built CRM and ticketing MCP servers. Refunds over $100 and every customer email pause for human approval, re-verified server-side.

- Layered prompt-injection defenses: untrusted-data fencing, per-agent tool scopes, a recipient-less reply tool, ownership checks, output validation
- **100% policy compliance** with a simulated fully hijacked model on a 16-scenario eval suite
- 69 unit and integration tests against real Postgres and MCP sessions, strict mypy

**Stack:** Python · official MCP SDK · FastAPI · PostgreSQL · React · TypeScript · OpenTelemetry · Docker

### 3. [Sawt · صوت](https://github.com/sinouw/sawt) — real-time multilingual voice agent

Phone-style clinic receptionist that understands and answers in Arabic (Modern Standard, Tunisian Derja, Gulf), French and English, books and cancels appointments through tool calls, and lets callers interrupt it mid-sentence.

- **2.54 s** median server time to first audio on the Groq free tier, timed stage by stage
- **94%** task success on the full audio path, 100% language ID, 3% character error rate
- Pluggable STT, LLM and TTS providers; hosted and local Whisper models compared

**Stack:** Python · FastAPI WebSockets · asyncio · Whisper (Groq, faster-whisper) · llama.cpp · edge-tts · Next.js · Docker

---

## Tech stack

**AI engineering:** RAG · hybrid retrieval (dense + BM25) · Qdrant · AI agents and function calling · multi-agent systems · MCP · LLM evaluation · OpenTelemetry · Groq · Gemini · Whisper · YOLOv8 · DeepFace

**Software engineering:** Python · TypeScript · JavaScript · Go · SQL · FastAPI · Node.js · NestJS · React · Next.js · Angular · Vue.js · React Native / Expo

**Architecture & data:** REST · GraphQL · microservices · event-driven and real-time systems · WebSockets · PostgreSQL · MongoDB · Prisma · Firestore

**Cloud & production:** GCP · AWS · Firebase · Docker · CI/CD · monitoring

---

## Experience

- **Independent Software & AI Engineering Consultant** (2023 – present): ZUPdeCO, Tested4you, SAHAB, Carrefour Links via Devoteam, PwC UK via Play Studios
- **Team Lead, Groupe HLi** (2025)
- **Technical Lead, Naxxum Group** (2022): led a 6-engineer team on a client platform serving 60k active users
- **Full-Stack Software Engineer, Naxxum Group** (2020 – 2022)

## Education

- **Engineering Degree (Master's level) in Data Science** — TEK-UP University, with distinction (evening program while working full-time)
- **Bachelor's Degree in Software Engineering** — ISET Nabeul

---

## Contact

Open to international opportunities as a Senior AI Engineer, AI Product Engineer or hands-on Tech Lead.

- LinkedIn: [linkedin.com/in/yassineelouni](https://www.linkedin.com/in/yassineelouni)
- Email: [yassine.elouni.dev@gmail.com](mailto:yassine.elouni.dev@gmail.com)
- Portfolio: [yassine-elouni-profile.web.app](https://yassine-elouni-profile.web.app/)
