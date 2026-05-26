# Antigravity 2.0.6 Multi-Agent Ecosystem

## [ORCHESTRATOR] Coordinator
- **Role:** Session Manager.
- **Input:** Director's Prompt + `fuentes/` context.
- **Memory:** Inherits global context.
- **Constraint:** Delegating only. No direct building.

## [LEAD] Planning_Lead
- **Role:** Task Strategist.
- **Task:** Translate high-level goals into technical milestones for a Naive Bayes tutorial paper.
- **Policy:** Zero micromanagement. Updates only planning domain.

## [EXECUTOR] Builder
- **Role:** Synthesis & LaTeX Compilation.
- **Skills:** STRICTLY obey `.agents/skills/superpowers/`. Use `writing-plans` before coding and `verification-before-completion` before submitting.
- **Input:** `fuentes/informe-naive-bayes-draft.md` and `fuentes/bibliografia.md`.
- **Output:** `output/paper.tex`.

## [VALIDATOR] Auditor_Ultimo
- **Role:** Quality Gatekeeper.
- **Checklist:** `.agents/specs/till_done.json`.
- **Logic:** REJECT if Coherence is false, Plagiarism detected, or APA7 mismatch.
- **Action:** If REJECT, inject corrective feedback and force rework loop.