<div align="center">
  <img src="https://luna-vis.com/assets/images/logo_dark_bg.png" width="120" alt="LunaVIs Systems"/>

  # LunaVIs Systems

  **AI product company, not a consultancy.**

  Building on-prem computer vision and agentic automation for MENA/GCC SMBs — infrastructure that survives contact with production, not demos that die after the pitch.

  [Website](https://www.luna-vis.com) · [Contact](mailto:contact@luna-vis.com) · Lahore, Pakistan

</div>

---

## Who we are

LunaVIs Systems (SMC-Private Limited) is a Pakistan-incorporated AI product company targeting SMBs across MENA and the GCC. We're not a dev shop that ships one-off client work and moves on — we build products, own the roadmap, and iterate on real deployments.

The team is distributed across three time zones by design: engineering in Pakistan, leadership presence in Jordan and Egypt. Remote-first, output-driven, no bureaucratic overhead.

## What we build

Three products, one thesis: AI infrastructure that runs where the data lives, not wherever is cheapest to host.

### Fovea — On-prem computer vision

Full production CV platform for physical security and operations: face recognition, PPE compliance detection, zone/perimeter monitoring, emotion detection. Built for environments where camera feeds cannot leave the building — a hard requirement for most of our target market, not a nice-to-have.

- Multi-stream ingestion with per-stream engine binding (detection, recognition, PPE, zone logic run independently per camera)
- TensorRT-batched inference with downstream embedding/vector search separated from the hot detection path
- Cross-stream identity resolution with sub-second live dedup and a durable reconciliation pass
- Offline licensing with fail-closed behavior on safety-critical engines — no phone-home dependency for a camera system to keep working
- Retention-aware storage (partitioned, time-bounded) instead of unbounded frame accumulation

### Alfred — Agentic operator (WhatsApp/Telegram)

Not a lead-capture chatbot. Alfred is a full agentic operator that executes tasks end-to-end — books appointments, handles FAQs, adapts persona per tenant — with real short-term/long-term memory and adaptive skill routing across the conversation, not a fixed decision tree.

- Multi-memory architecture (STM/LTM) with schema-based procedural memory, tuned to avoid template-overfitting on paraphrased inputs
- Two-stage generation: fact extraction decoupled from voice/compose, so response tone never gets contaminated by raw retrieved text
- Affect-aware escalation — distressing or urgent input gets acknowledged before it gets solved
- Deployment topology built for both shared SaaS backends and fully client-hosted infra (self-hosted LLM support via OpenAI-compatible endpoints), because some clients won't put data on anyone else's servers
- Single-tenant per deployment, templated core — not rebuilt from scratch per client

### Lena — Web chat agent

Live on [luna-vis.com](https://www.luna-vis.com). Knowledge-base-grounded, hardened against prompt injection and information disclosure, multilingual (Arabic, Urdu, and Roman-script variants) out of the box, tuned to run efficiently on constrained context windows rather than assuming unlimited token budget.

## Engineering philosophy

We hold every product to what we internally call the **3026 standard**: it should feel impossibly advanced to someone who has no idea how any of it works, while being boring and predictable to the engineer running it in production. That tension — spectacle on the surface, discipline underneath — is the actual design brief.

In practice that means:

- **On-prem or client-hosted first.** Cloud dependency is a decision we make deliberately per product, not a default.
- **Fail-closed, not fail-open.** Safety-critical paths degrade to locked, never to silently-off.
- **No proof-of-concept debt.** What ships to a demo is the same architecture that ships to production — we don't rebuild the "real" version later.

## Stack

| Layer | Tools |
|---|---|
| CV / inference | C++20, TensorRT, DeepStream, ONNX, CUDA, InsightFace |
| Video pipeline | GStreamer, FFmpeg, RTSP |
| Agentic / LLM | LangGraph, Python, Groq, Anthropic, self-hosted (Ollama/LM Studio)-compatible endpoints |
| Data / infra | Postgres + pgvector, Redis, Supabase, Cloudflare Tunnel |

## Markets

Pakistan → UAE, Jordan, Egypt, and the wider GCC. SMBs who need real security and automation infrastructure without a hyperscaler contract or a data-residency headache.

---

<div align="center">
  <sub>Founded March 2026 · Lahore, Pakistan</sub>
</div>
