# Andrew Kobelev

**Python Developer · Backend Engineer · AI Engineer**

I build backend systems where AI agents are architectural components — not API wrappers.
Currently a Python developer at a startup working on industrial automation and AI.

![Python](https://img.shields.io/badge/Python-1a1a1a?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-1a1a1a?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-1a1a1a?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-1a1a1a?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-1a1a1a?style=flat-square&logo=docker&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1a1a1a?style=flat-square&logo=langchain&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-1a1a1a?style=flat-square)

---

## Specialization

**AI-powered backend systems and agent architecture.** The model is one component inside a larger
system — bounded by deterministic logic, connected to tools and knowledge sources, wired into real
business processes.

**Deterministic planning, LLM generation.** Control flow and formally checkable rules live in code;
the model handles only what genuinely requires reasoning.

**Agents as platform components.** Stateful graphs with human-in-the-loop interrupts, parallel
fan-out and custom reducers for concurrent writes — shipped with auth, integration contracts and
offline tests, not as standalone scripts.

**Tools and MCP instead of direct coupling.** A production MCP server with JWT auth and scoped
tokens serves a nested knowledge agent; the calling agent never touches the protocol.

**Hard real-time budgets.** Concurrent graphs under a fixed per-turn limit with fallback replies,
semaphore-limited model concurrency, field-level Redis merges between parallel graphs.

---

## Engineering Skills

| | |
|---|---|
| **Backend & Data Design** | Async services, layered structure, multi-tenant models, explicit state machines, migration discipline |
| **System Architecture** | Multi-service decomposition, service boundaries, service-to-service auth, graceful degradation |
| **Agent Architecture** | Graph design, explicit state, interrupts and resumption, tool interfaces, agent authorization |
| **AI Engineering** | Prompting under anti-hallucination constraints, structured outputs, provider fallback, latency and cost budgets |
| **Retrieval & Knowledge** | Vector search with metadata filtering and LLM reranking, exposed to agents through tools |
| **Async Processing** | Task queues with specialized worker pools, distributed locks, pub/sub, progress streaming |
| **Integrations & Automation** | CRM, telephony, speech and storage providers; webhooks; end-to-end automated pipelines |
| **Testing & Delivery** | Black-box API suites, offline graph tests, container stacks, monitoring, CI/CD |
| **Technical Ownership** | End-to-end from schema to deployment; mentoring developers; integration guides and deploy runbooks |

---

## Tech Stack

**Core** · Python 3.12 · FastAPI · SQLAlchemy 2.0 (async) · Pydantic v2 · Alembic · pytest

**Agents & LLM** · LangGraph · LangChain · MCP / FastMCP · tool calling · structured outputs

**Retrieval** · Qdrant · ChromaDB · embeddings · metadata filtering · LLM reranking

**Models & inference** · Whisper / faster-whisper · GigaAM · YOLOv8 · PyTorch · vLLM · OpenAI API

**Data & Queues** · PostgreSQL · Redis · S3 / MinIO · TaskIQ · Celery · ARQ · RabbitMQ

**Infrastructure** · Docker & Compose · nginx · Grafana · Loki · Prometheus · GitHub Actions

**Integrations** · Bitrix24 · amoCRM · LiveKit (WebRTC / SIP) · ElevenLabs · Telegram Bot API

**Secondary** · Next.js · TypeScript — internal consoles and dashboards

---

## Architecture

The recurring shape across my projects: a thin API layer, background workers doing the heavy work,
and an agent runtime whose state is explicit, observable and testable offline.

<p align="center">
  <picture>
    <source
      media="(prefers-color-scheme: dark)"
      srcset="https://raw.githubusercontent.com/andrey-kobelev/andrey-kobelev/main/assets/architecture-dark.png">
    <img
      alt="Thin FastAPI layer, background workers, and a LangGraph agent runtime wired to Redis, MCP tools, a vector store and external systems"
      src="https://raw.githubusercontent.com/andrey-kobelev/andrey-kobelev/main/assets/architecture-light.png"
      width="880">
  </picture>
</p>

---

## Selected Work

Commercial projects, mostly in private repositories — described without client-identifying details.

**Real-time voice AI agent.** Live inbound phone calls. Three concurrent graphs: the dialogue agent,
a checker running *while the caller is still speaking*, and a background worker for profile
extraction and knowledge lookups. Deterministic script planning, 9-second turn budget, self-hosted
Russian ASR. 11 services, 667 offline tests.

**Document compliance agent.** Validates official documents against a formal regulation. One graph
turns the regulation into per-section rules offline; a second runs structural checks in code and
semantic checks as parallel LLM calls, streaming progress live.

**Call analysis platform with MCP.** Scores call recordings pulled from CRM with a two-tier agent —
a scoring agent that delegates knowledge questions to a nested knowledge agent, which reaches the
knowledge base through a production MCP server with a forwarded token chain.

**Conversational requirements agent.** 18-node graph with human-in-the-loop interrupts, parallel
fan-out, and an LLM resolver mapping free text onto available choices. Paired with a FastAPI
platform: role-based access, Celery workers, service-to-service auth.

**Industrial defect detection.** Four-model YOLOv8 cascade on GPU, from an industrial camera feed
through to PLC actuation of a physical reject mechanism.

---

## Current Focus

- Agent orchestration — coordination, recovery and state across multi-graph systems
- MCP as the integration layer between agents and business systems
- Retrieval architecture — ingestion pipelines, hybrid vector + keyword search
- Making AI systems observable, testable and reproducible in production

---

## Contact

[Telegram](https://t.me/andrew_kobe) · [heiskobe@yandex.ru](mailto:heiskobe@yandex.ru)

Open to conversations about agent architecture, LLM-driven backends and AI automation.
