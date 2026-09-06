# Juno PM

> An AI Associate PM that turns Slack, Notion, and Jira signals into a prioritized top-3 risk list so product managers can make faster, evidence-backed decisions.

_Matthew DeLeon, AI Product Management Certification, September 2026_

Repo: https://github.com/mdeleon86/juno-pm-

This repo is my final project for the AI Product Management Certification — **Juno PM**. Each module’s artefact lives in its own folder; this README is the dashboard and the pitch.

---

## Module artefacts

### M1 · Prompting
- **System prompt** — [`01-prompting/system-prompt.md`](01-prompting/system-prompt.md)
- **Prototype** — https://lovable.dev/projects/2f5ded51-63a2-405f-bc8f-822f42454dff?magic_link=mc_c7825c0f-5175-4d39-a094-48c78b506240

### M2 · Strategy
- **Decision matrix** — [`02-strategy/decision-matrix.md`](02-strategy/decision-matrix.md)
- **AI Strategy one-pager** — [`02-strategy/strategy-one-pager.md`](02-strategy/strategy-one-pager.md)

### M3 · RAG / AI PRD
- **AI PRD** — [`03-rag-prd/prd.md`](03-rag-prd/prd.md)

### M4 · AI-Native UX
- **AI user flow** — [`04-ai-ux/user-flow.md`](04-ai-ux/user-flow.md)
- **Trust-gap mitigations** — [`04-ai-ux/trust-gaps.md`](04-ai-ux/trust-gaps.md)

### M5 · Agentic Workflows
- **Agent Workflow Spec (AWSpec)** — [`05-agentic-workflows/awspec.md`](05-agentic-workflows/awspec.md)
- **Agent Control Panel** — [`05-agentic-workflows/agent-control-panel.md`](05-agentic-workflows/agent-control-panel.md)

### M6 · Evals &amp; Guardrails
- **Eval stack** — [`06-evals/eval-stack.md`](06-evals/eval-stack.md)
- **Human evaluation rubric** — [`06-evals/human-rubric.md`](06-evals/human-rubric.md)

---

## PM Execution Plan

### Where Juno is today
- M1-M6 artifacts are fully specified and committed.
- The prototype validates Juno’s core PM copilot flow.
- The evaluation stack, human rubric, guardrails, and governance framework are defined; production eval automation and reviewer staffing remain to be implemented.

### What ships next (next 2 sprints)
- Sprint 1: Implement the evaluation harness against the golden set, wire Juno’s Slack and retrieval tools, and validate citation, grounding, refusal, and safety checks.
- Sprint 2: Launch a controlled beta with PM users, apply the human evaluation rubric, collect user feedback, and use evaluation results to refine prompts, retrieval, guardrails, and agent behavior.

### What I watch (dashboards)
- Daily: thumbs-down rate, regeneration rate, abandonment rate, handoff rate, latency, and tool failures.
- Weekly: human-rubric scores by dimension, safety/refusal performance, citation grounding, and cost per run.
- Per release: golden-set accuracy and automated format, citation, refusal, and safety pass rates.

### Red lines (what blocks shipping)
- Any critical safety failure or PII leakage blocks release.
- Golden-set accuracy below 90% blocks release.
- Failed citation or grounding checks block release.
- Fabricated customer information triggers immediate review.
- P99 latency above 5 seconds or cost above $0.50 per run requires PM review before scaling.

### Governance
Compliance: Protect customer data and PII; review regulatory and data-handling requirements before deployment.
Safety: Defend against prompt injection, misuse, fabricated information, and unsafe actions; require human review for high-risk or low-confidence decisions.
Reliability: Monitor accuracy, citations, latency, tool failures, and model performance; use confidence thresholds, fallback paths, and graceful degradation when Juno cannot respond reliably.
Reputation: Prevent unsupported or customer-facing actions from being published without appropriate review; monitor failures and maintain clear escalation and response procedures.

---

## Build Insights

- **Friction point.** Keeping Juno’s requirements consistent across the system prompt, RAG architecture, user flow, agent workflow, and evaluation criteria.
- **Key learning.** AI product decisions need to connect across the full system, from strategy and prompts to agent controls and evaluation.
- **Aha moment.** The AI system is the product, not just the interface; prompts, retrieval, guardrails, agent behavior, and evals all shape the user experience.

---

_Certification submission — AI Product Management Certification._
