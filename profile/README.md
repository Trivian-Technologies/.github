<div align="center">

# Trivian Technologies

**Audit Receipts for AI-Assisted Financial Decisions**

When your AI assists with lending, AML monitoring, fraud review, or underwriting—every decision must be auditable, defensible, and regulatory-ready.

[![Website](https://img.shields.io/badge/Website-trivian.io-1A6FC4?style=flat-square&logo=globe&logoColor=white)](https://trivian.io)
[![Docs](https://img.shields.io/badge/Docs-docs.trivian.io-2496ED?style=flat-square&logo=book&logoColor=white)](https://docs.trivian.io)
[![X](https://img.shields.io/badge/X-@TrivianTech-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/TrivianTech)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Trivian_Technologies-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/trivian-technologies)
[![Email](https://img.shields.io/badge/Contact-hello@trivian.io-B8922A?style=flat-square&logo=gmail&logoColor=white)](mailto:hello@trivian.io)

</div>

---

## The Problem

Financial institutions are deploying AI across critical workflows:
- **AML Monitoring** — AI flags suspicious transactions
- **Fraud Detection** — AI prioritizes fraud cases  
- **Lending Decisions** — AI assists with underwriting
- **Underwriting** — AI scores creditworthiness

But regulators demand the same documentation for AI decisions as they do for human decisions:

> *"What did the AI do? Why? What policy applied? Was a human required to review it?"*

**Today, these answers are scattered across logs, spreadsheets, and case notes. Compliance teams spend weeks manually reconstructing evidence.**

---

## The Solution

**Syzygy Rosetta** creates tamper-evident audit receipts for every AI-assisted decision.

For every decision, Rosetta captures:
- **What the AI evaluated** — input, context, model output
- **What policy applied** — which compliance rules were checked
- **What risk signals emerged** — quantified risk scores
- **Whether escalation was required** — human review trigger
- **What the human decided** — if reviewed, what action they took
- **Final outcome** — what actually happened

The result: a complete, signed, audit-ready evidence chain.

---

## How It Works

```
Your AI System Output
         ↓
    Rosetta API
     ├─ Policy Evaluation
     ├─ Risk Scoring
     ├─ Human Review Routing
     └─ Audit Receipt Generation
         ↓
Tamper-Evident Evidence (Regulatory-Ready)
```

### One Endpoint. Complete Governance.

```bash
POST /v1/evaluate
```

**Request:**
```json
{
  "workflow": "aml_monitoring",
  "policy_version": "aml_policy_v2.1",
  "input": {
    "transaction_id": "txn-892847",
    "amount": 50000,
    "jurisdiction": "us",
    "customer_risk_score": 5.2
  },
  "ai_output": {
    "decision": "flag",
    "confidence": 0.78
  }
}
```

**Response:**
```json
{
  "decision": "escalate",
  "receipt_id": "receipt-2026-05-23-1847",
  "risk_score": 0.78,
  "risk_components": {
    "heuristic": 0.72,
    "semantic": 0.82
  },
  "violations": [
    {
      "rule": "high_amount",
      "threshold": 10000,
      "value": 50000,
      "severity": "high"
    }
  ],
  "escalation_target": "aml_team",
  "escalation_sla": 4,
  "audit_trail": [
    "policy_check_initiated",
    "violation_detected",
    "risk_scoring_complete",
    "escalation_triggered",
    "audit_receipt_generated"
  ],
  "timestamp": "2026-05-23T18:47:33Z",
  "processing_time_ms": 87
}
```

---

## Decision Thresholds

| Decision | When | What Happens |
|---|---|---|
| **allow** | Policy passes + Risk < threshold | Proceed without escalation |
| **escalate** | Policy ambiguous OR Risk borderline | Route to human reviewer |
| **block** | Policy violation OR Risk critical | Reject or escalate to senior review |

Every decision generates a tamper-evident audit receipt.

---

## Why Audit Receipts Matter

### Before Rosetta
- Compliance manually reconstructs every decision
- Audit cycles take 4-6 weeks
- Regulators question your governance
- Liability exposure for undocumented decisions

### After Rosetta
- Every decision is automatically documented
- Audit cycles compress to 3-5 days
- Regulators see complete evidence
- Defensible, compliant decision-making at scale

---

## Use Cases

### AML Monitoring
Prove to FinCEN that AI-flagged transactions were evaluated against your policy, risk-scored, and appropriately escalated for human review.

### Fraud Detection
Defend fraud blocks in chargebacks with complete decision evidence. Show OCC that fraud governance is documented and auditable.

### Lending Decisions
Document Fair Lending compliance. Prove the same policy factors were evaluated for all applicants. Defend adverse action notices with complete evidence.

### Underwriting
Score creditworthiness with AI. Document that human underwriters reviewed the recommendation. Create defensible adverse action documentation.

---

## Regulatory Alignment

✓ **NYDFS Part 504** — Documents your AI governance policies and compliance checks  
✓ **Fair Lending (ECOA)** — Proves consistent policy application across all applicants  
✓ **AML/BSA** — Creates evidence chains for SAR filings and regulatory audits  
✓ **OCC Guidance** — Demonstrates model oversight and decision documentation  
✓ **CMS/Healthcare** — Documents medical necessity and clinical decision-making  

---

## Repositories

| Repo | Purpose | Status |
|---|---|---|
| [syzygy-rosetta](https://github.com/Trivian-Technologies/syzygy-rosetta) | Core evaluation engine — policy, risk scoring, audit receipts | ✅ Active |
| [rosetta-sandbox](https://github.com/Trivian-Technologies/rosetta-sandbox) | Interactive demos, multi-workflow testing, before/after case studies | ✅ Active |
| [rosetta-docs](https://github.com/Trivian-Technologies/rosetta-docs) | Complete documentation — API reference, compliance guides, integration examples | ✅ Active |
| [rosetta-sdk](https://github.com/Trivian-Technologies/rosetta-sdk) | Official Python SDK + REST client libraries | 🔄 In Development |
| [trivian-website](https://github.com/Trivian-Technologies/trivian-website) | Product marketing website | 🔄 In Development |

---

## Tech Stack

![Python](https://img.shields.io/badge/Python_3.10+-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GCP](https://img.shields.io/badge/GCP_Cloud_Run-4285F4?style=flat-square&logo=google-cloud&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini_API-8B5CF6?style=flat-square&logo=google&logoColor=white)

---

## Quick Start (5 Minutes)

### 1. Get Your API Key
Sign up at [app.trivian.io](https://app.trivian.io) and create a project.

### 2. Install SDK
```bash
pip install rosetta-sdk
```

### 3. Make Your First Evaluation
```python
from rosetta import RosettaClient

client = RosettaClient(api_key="sk_live_abc123...")

response = client.evaluate(
    workflow="aml_monitoring",
    input={
        "transaction_id": "txn-892847",
        "amount": 50000,
        "jurisdiction": "us",
        "customer_risk_score": 5.2
    },
    ai_output={
        "decision": "flag",
        "confidence": 0.78
    },
    policy_version="aml_policy_v2.1"
)

print(f"Decision: {response.decision}")
print(f"Receipt ID: {response.receipt_id}")
print(f"Risk Score: {response.risk_score}")

# Retrieve full audit receipt
receipt = client.get_receipt(response.receipt_id)
print(receipt.to_json(pretty=True))
```

### 4. Verify Integrity
```python
# Verify receipt hasn't been tampered with
is_valid = client.verify_receipt(receipt)
assert is_valid, "Receipt compromised!"
```

---

## REST API

### Health Check
```bash
curl http://localhost:8000/healthz
```

### Evaluate a Decision
```bash
curl -X POST https://rosetta.trivian.io/v1/evaluate \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "workflow": "aml_monitoring",
    "input": {...},
    "ai_output": {...},
    "policy_version": "aml_policy_v2.1"
  }'
```

### Retrieve Receipt
```bash
curl https://rosetta.trivian.io/v1/receipts/{receipt_id} \
  -H "Authorization: Bearer YOUR_API_KEY"
```

---

## What Gets Logged

Every audit receipt includes:

- **Metadata** — unique receipt ID, timestamp, workflow, policy version
- **Input** — original request that triggered evaluation
- **Policy Evaluation** — which rules were checked, violations detected
- **Risk Scores** — heuristic + semantic scoring across risk dimensions
- **AI Output** — what the model recommended
- **Decision** — system decision (allow/escalate/block)
- **Human Review** — who reviewed, when, what they decided (if escalated)
- **Audit Trail** — chronological record of all events
- **Cryptographic Signature** — HMAC-SHA256 proof of integrity

**Result:** Tamper-evident, regulatory-ready documentation for every decision.

---

## Deployment

### Docker
```bash
docker build -t rosetta .
docker run -p 8000:8000 \
  -e GEMINI_API_KEY=your-key \
  -e POLICY_CONFIG=/config/policies.json \
  rosetta
```

### Cloud Run (GCP)
```bash
gcloud run deploy rosetta \
  --image gcr.io/your-project/rosetta \
  --set-env-vars GEMINI_API_KEY=your-key
```

### Environment Variables
```
GEMINI_API_KEY           # LLM scoring (optional but recommended)
POLICY_CONFIG            # Path to policy rules
LOG_LEVEL                # DEBUG, INFO, WARNING
AUDIT_LOG_PATH           # Where to write receipts
DATABASE_URL             # Postgres connection for receipt archive
```

---

## For Compliance Teams

**Looking for proof that your AI governance is working?**

→ [Audit Receipts Explained](https://docs.trivian.io/concepts/audit-receipts)

**Need to respond to a regulatory audit?**

→ [Compliance Framework](https://docs.trivian.io/compliance)

**Want to understand your current audit burden?**

→ [AML Workflow Example](https://docs.trivian.io/workflows/aml-monitoring)

---

## For Developers

**Want to integrate in 5 minutes?**

→ [Quick Start Guide](https://docs.trivian.io/integration/quick-start)

**Need complete API reference?**

→ [API Documentation](https://docs.trivian.io/integration/api-reference)

**Building a custom workflow?**

→ [Integration Examples](https://docs.trivian.io/integration/rest-examples)

---

## For Risk Officers & Model Governance

**Need to audit policy compliance at scale?**

→ [Audit Log & Search](https://docs.trivian.io/operations/audit-logs)

**Want to configure policies without code changes?**

→ [Policy Configuration Guide](https://docs.trivian.io/operations/policy-configuration)

**Monitoring model behavior drift?**

→ [Risk Scoring Framework](https://docs.trivian.io/concepts/risk-scoring)

---

## Enterprise Readiness

✓ **Authentication** — Bearer token auth + role-based access control  
✓ **Encryption** — TLS 1.3 in transit, AES-256-GCM at rest  
✓ **Audit Logging** — Immutable append-only audit trail  
✓ **Tenant Isolation** — Complete data isolation between customers  
✓ **High Availability** — Deployed on GCP Cloud Run, auto-scaling  
✓ **Monitoring** — Prometheus metrics, structured logging  
✓ **Compliance Ready** — HIPAA, SOC2, NYDFS Part 504 compatible  

---

## Support

- **Documentation:** [docs.trivian.io](https://docs.trivian.io)
- **Email:** [hello@trivian.io](mailto:hello@trivian.io)
- **Status:** [status.trivian.io](https://status.trivian.io)
- **Community:** [Slack](https://slack.trivian.io)

---

## Who This Is For

**Compliance & Risk Teams** — Get audit receipts instead of spreadsheets. Prove to regulators what happened.

**Financial Institutions** — AML monitoring, fraud detection, lending, underwriting—every decision documented and defensible.

**Regulated SaaS Platforms** — Healthcare, fintech, legal tech—any industry where AI decisions are scrutinized.

**Enterprise Security & Governance** — Teams overseeing AI model risk and policy compliance.

**Developers** — Building on LLM providers and needing structured output validation before deployment.

---

## Contributing

This is a closed-source commercial product. For partnership inquiries, enterprise pilots, or API access:

**[hello@trivian.io](mailto:hello@trivian.io)**

---

<div align="center">

**Trivian Technologies — Audit Receipts for AI-Assisted Financial Decisions**

*Making AI safe, auditable, and defensible for enterprise adoption.*

**[Try the Sandbox](https://demo.trivian.io) · [Read the Docs](https://docs.trivian.io) · [Contact Us](mailto:hello@trivian.io)**

</div>
