---
applyTo: "**"
---

# Agent Orchestration Policy

## ⚙️ Model Configuration

_(Update the models in this list to dynamically change routing across all workflows)_

- **Orchestrator:** `GPT-5.4`
- **UI & Front-End:** `Claude Sonnet 4.6`
- **Core Logic:** `GPT-5.3-Codex`
- **Review & QA:** `GPT-5.4`

## Task-Based Model Routing

Copilot MUST dynamically select the most capable model based on the specific domain of the task. Always reference the **Model Configuration** list above to determine the correct assignment:

- **Orchestration:** Use the designated Orchestrator model to break down requests, manage subagents, and synthesize final outputs.
- **UI & Front-End:** Route UI rendering, styling, and component structures to the designated UI model.
- **Core Logic:** Route algorithms, state management, database queries, and data transformations to the designated Core Logic model.
- **Review & QA:** Route code reviews, security audits, and unit test generation to the designated Review model.

## Subagent Delegation Mandate

Copilot MUST utilize the "subagent" architecture to decompose workflows into specialized tasks.

### Core Delegation Principles

1.  **Decomposition First**: Analyze the overall request and split it into distinct structural domains (e.g., separating the UI implementation from the algorithmic logic).
2.  **Smart Routing**: Dispatch each decomposed sub-task to the appropriate model based on the routing rules above.
3.  **Validation Loops**: Every primary code output must be passed to a Review subagent for verification before being presented as final.

## Workflow Integration

For every request, strictly adhere to this internal execution sequence:

1.  **Plan**: Draft the high-level architecture and map out which models will handle which specific components.
2.  **Delegate**: Spawn parallel sub-tasks and invoke the highly-specialized models for each required domain.
3.  **Synthesize**: Collect the subagent outputs and use the primary Orchestrator to stitch them into a cohesive, working implementation.
4.  **Verify**: Perform a final pass using the Review model to ensure the specialized contributions were integrated flawlessly and meet quality standards.

> "Efficiency is found in specialization. Complex tasks require diverse model consensus."
