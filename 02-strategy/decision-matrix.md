# AI Solution Decision Matrix · Juno

## The decision

Whether RocketShip builds Automated Prioritization in Juno as a Hybrid (RAG + Agentic) Copilot, vs buying a generic LLM API or fine-tuning a model on our corpus.

Why now: roadmap discussions are driven by the loudest voice in Slack rather than customer evidence. Priorities reverse weekly, and the PM cannot defend the call to leadership.

## Options scored

| Option | Cost | Speed | Control | Moat | Risk | Score |
|---|---|---|---|---|---|---|
| Build | 2 | 2 | 5 | 5 | 4 | 3.6 |
| Buy / API | 5 | 5 | 2 | 1 | 2 | 3.0 |
| Fine-tune | 3 | 2 | 4 | 4 | 3 | 3.2 |

## Recommendation

Build the Juno product and orchestration layer while using a general-purpose LLM API with RAG for model capabilities. A Buy / API approach is faster and cheaper and can still retrieve and cite RocketShip sources when combined with RAG, but relying on an off-the-shelf product would provide less control over Juno’s prioritization logic, workflow integration, guardrails, and differentiated PM experience. Fine-tuning adds cost and maintenance without solving the need for live retrieval of changing internal evidence. The differentiation comes from Juno’s product layer, proprietary context, retrieval design, and prioritization workflow rather than from training a foundation model. Autonomy stays Copilot: Juno drafts the ranked backlog with citations, and the PM approves before publish.
