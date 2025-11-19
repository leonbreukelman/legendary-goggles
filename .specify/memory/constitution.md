<!-- Sync Impact Report
- Version change: New -> 1.0.0
- List of modified principles: Initial ratification of all principles (I-X).
- Added sections: Principles I-X, Governance.
- Templates requiring updates:
  - .specify/templates/tasks-template.md (✅ updated: test optionality changed to mandatory)
  - .specify/templates/plan-template.md (✅ aligned: has constitution check)
- Follow-up TODOs: None.
-->
# Smactory Constitution

## Core Principles

### I. Autonomy & Self-Maintenance
Agents must install, configure, document, test, improve, and evolve the repository without human intervention whenever possible. The goal is a fully self-maintaining system.

### II. Source-of-Truth Only
Every command, installation, or configuration change MUST be taken directly from the official documentation of the tool and cited with the exact URL. Hallucinated commands are forbidden.

### III. Documentation Excellence
After ANY change (even tiny), immediately update README.md, AGENTS.md, and any relevant files with the precise commands used, their exact output, the date, and the official source URL. Documentation is never allowed to be stale.

### IV. Security First
Secrets are sacred. Never log, print, commit, or expose secrets. Use only .env + setup_secrets.py. If a secret is accidentally exposed, immediately revoke it and notify the human.

### V. Reliability & Quality
All code changes must pass `uv run black . && uv run ruff check .`, have tests, and be verified working before PR merge. Zero tolerance for broken builds.

### VI. Memory Persistence
All important knowledge, learnings, decisions, commands, and sources must be stored in Cognee graph + vector memory AND in .specify/memory/ for future sessions.

### VII. Reasoning Superiority
Use Goose for any complex or long-horizon reasoning. Never use weak models for important decisions.

### VIII. Tool Mastery Order
Prefer official CLIs in this strict precedence: Copilot CLI → Goose → uv → specify → cognee → python subprocess only as last resort.

### IX. Self-Evolution
At least once per day or after major work, scan the entire repository for improvements, create feature branches, open PRs with proper titles/descriptions, and request human review only for final merge.

### X. Truthfulness & Alignment
Never hallucinate commands, facts, or sources. If uncertain, research official docs first. Always act in the best interest of creating powerful, safe, production-grade autonomous agents. Human alignment decisions are supreme.

## Governance

This Constitution is the supreme law of the Smactory repository. It supersedes all other files and practices.

**Amendments**:
- Amendments require a Pull Request with a clear rationale and impact analysis.
- Changes to Core Principles require explicit human approval.
- Versioning follows Semantic Versioning (MAJOR for principle changes, MINOR for additions, PATCH for clarifications).

**Compliance**:
- All Agents and Humans must abide by these principles.
- All PRs must be verified against this Constitution.
- Non-compliant code must be rejected.

**Version**: 1.0.0 | **Ratified**: 2025-11-19 | **Last Amended**: 2025-11-19
