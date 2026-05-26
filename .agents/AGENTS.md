# Antigravity 2.0.6 Multi-Agent Ecosystem

## [ORCHESTRATOR] Coordinator
- **Role:** Session Manager.
- **Input:** Director's Prompt + `sources/` context.
- **Memory:** Inherits `.agents/expertise/global_context.md`.
- **Constraint:** Delegating only. No direct building.

## [LEAD] Planning_Lead
- **Role:** Task Strategist.
- **Task:** Translate high-level goals into technical milestones in `.agents/specs/plan.md`.
- **Policy:** Zero micromanagement. Updates only planning domain.

## [EXECUTOR] Builder
- **Role:** Synthesis & LaTeX Compilation.
- **Skills:** Cargar y obedecer estrictamente las directrices de `.agents/skills/superpowers/`. Utilizar obligatoriamente `writing-plans` antes de codificar y `verification-before-completion` antes de entregar.
- **Input:** `.agents/specs/plan.md` + `fuentes/informe-naive-bayes-draft.md`.
- **Output:** `output/paper.tex`.

## [VALIDATOR] Auditor_Ultimo
- **Role:** Quality Gatekeeper.
- **Checklist:** `.agents/specs/till_done.json`.
- **Logic:** REJECT if Coherence < 100%, Plagiarism > 0%, or APA7 mismatch.
- **Action:** If REJECT, inject corrective feedback to Builder expertise.