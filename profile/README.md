<div align="center">

# Trivian Technologies

**AI Governance Infrastructure — Built for Production**

Make AI deployable, auditable, and safe for enterprise adoption.

[![Website](https://img.shields.io/badge/Website-triviantech.com-1A6FC4?style=flat-square&logo=globe&logoColor=white)](https://triviantech.com)
[![X](https://img.shields.io/badge/X-@TrivianOS-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/TrivianOS)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Trivian_Technologies-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/awakening-the-architect)
[![Email](https://img.shields.io/badge/Contact-se@trivianinstitute.org-B8922A?style=flat-square&logo=gmail&logoColor=white)](mailto:se@trivianinstitute.org)

</div>

---

<p align="center">
  <img
    src="https://github.com/Trivian-Technologies/trivian-build-activity/blob/main/assets/build-activity.svg"
    alt="Trivian Technologies — Build Activity"
    width="860"
  />
</p>

## What We Build

Trivian Technologies builds **AI governance middleware** — the infrastructure layer between AI models and the production systems that deploy them.

Enterprises deploying AI agents face a real problem: models hallucinate, drift, and produce outputs that violate compliance requirements. No model provider solves this at the infrastructure level. We do.

Our flagship product, **Syzygy Rosetta**, is a containerised, API-first governance engine that evaluates every AI input and output before it reaches an end user — applying deterministic policy rules and ML-based risk scoring to return a structured, auditable decision in real time.

---

## Syzygy Rosetta
```bash

POST /evaluate

```
Every `POST /evaluate` call returns exactly these 8 fields:

```json
{
  "decision": "allow | rewrite | escalate",
  "risk_score": 0.12,
  "confidence": 0.91,
  "violations": [],
  "rewrite": null,
  "reasoning": "Input within acceptable parameters for financial context.",
  "field_notes": [],
  "timestamp": "2026-03-21T14:32:00Z"
}
```

### Decision thresholds

| Risk Score | Decision | What happens |
|---|---|---|
| `< 0.4` | `allow` | Input passed through. `violations` is empty. |
| `0.4 – 0.7` | `rewrite` | Soft violation. `rewrite` field contains corrected output. |
| `> 0.7` | `escalate` | Hard violation. Routed to human review. |

---

One endpoint. Every AI output evaluated, scored, and governed — before it reaches production.

**What Rosetta is not:** a chatbot, a foundation model, a UI layer, or a prompt wrapper.

**What Rosetta is:** infrastructure. It sits between your AI and your users and makes sure what goes through is safe, compliant, and auditable.

---
How It Works
1	`safety_layer.py`	Pre-classifies input — tags authority, manipulation, dependency, escalation patterns

2	`policy engine`	Matches against industry-specific deterministic rules (finance / healthcare / general)

3	`risk_scoring.py`	ML composite scorer — KeywordScorer + FeatureScorer + LLMScorer

4	Decision logic	Threshold applied — allow / rewrite / escalate

5	Audit log	Full evaluation appended to `logs/evaluations.json`
---

## Why It Matters

| Problem | What Rosetta Does |
|---|---|
| AI outputs violate compliance requirements | Policy engine flags and rewrites violations before they surface |
| No audit trail for AI decisions | Every evaluation logged with full decision record |
| Models behave differently across contexts | Industry-specific rulesets for finance, healthcare, general |
| Agents drift and degrade over time | Confidence scoring and drift detection built in |
| Enterprise procurement requires auditability | Structured logs exportable for compliance reporting |

---

## Repositories

| Repo | Description | Status |
|---|---|---|
| [syzygy-rosetta-originbase](https://github.com/Trivian-Technologies/syzygy-rosetta-originbase) | Core governance engine — spec-compliant, Docker deployment in progress — `POST /evaluate` | 🔄 Active |
| [syzygy-rosetta-sandbox](https://github.com/Trivian-Technologies/syzygy-rosetta-sandbox) | Multi-agent testing and before/after drift simulation | 🔵 Planned |
| [syzygy-rosetta-docs](https://github.com/Trivian-Technologies/syzygy-rosetta-docs) | Full technical documentation | 🔄 Active |
| [syzygy-rosetta-sdk](https://github.com/Trivian-Technologies/syzygy-rosetta-sdk) | Official Python and JS SDK | 🔵 Planned |
| [Trivian-Infrastructure](https://github.com/Trivian-Technologies/Trivian-Infrastructure) | Future infrastructure — Trivian Lattice Engine, Gaian Interface	Early Design | 🔵 Planned |
| [TrivianTech-website](https://github.com/Trivian-Technologies/TrivianTech-website) | Official website source	In Development | 🔄 Active |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python_3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Uvicorn](https://img.shields.io/badge/Uvicorn-4B0082?style=flat-square&logo=python&logoColor=white)

---

## Quick Start
```bash

\# Clone the core engine

git clone https://github.com/Trivian-Technologies/syzygy-rosetta-originbase.git

cd syzygy-rosetta-originbase



\# Build and run (STILL IN PROD)

docker build -t rosetta .

docker run -p 8000:8000 rosetta



\# Evaluate your first input

curl -X POST http://localhost:8000/evaluate \\

-H "Content-Type: application/json" \\

-d '{

"input": "Your AI output here",

"context": {

"industry": "healthcare",

"user_id": "demo",

"environment": "staging"

}

}'

```

Full documentation → [docs.triviantech.com](https://github.com/Trivian-Technologies/syzygy-rosetta-docs)
---

## Who This Is For

**Enterprise teams** deploying AI agents in regulated environments — healthcare, financial services, legal, compliance-heavy sectors — who need a governance layer they can audit, configure, and own.

**Developers and AI engineers** building on top of LLM providers who need structured output validation before their system acts on model responses.

**Fintech companies** requiring regulatory compliance enforcement

**Healthcare platforms** handling sensitive AI outputs

**AI agent developers** needing multi-agent governance

**Regulated SaaS platforms** with enterprise compliance requirements

**Compliance and risk functions** that need a documented, exportable audit trail of every AI decision made in production.

---

## Status

Syzygy Rosetta core engine is spec-compliant and confirmed working. The full 8-step evaluation pipeline is live — safety classification, deterministic policy enforcement, ML risk scoring, structured decision output, and persistent audit logging. Docker deployment and multi-agent sandbox testing are in progress.

Syzygy Rosetta is in active development. MVP delivery in progress.

For enterprise pilot enquiries, API trial access, or partnership discussions:

**se@trivianinstitute.org**

---

<div align="center">

*Trivian Technologies — AI Governance Infrastructure*
*Built to make AI safe for production.*

</div>
