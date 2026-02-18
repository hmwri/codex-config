# AGENTS.md

This file defines mandatory execution rules for all coding agents working in this repository.

## 0) Repository folder structure documentation
- Agents must keep a folder structure section in this file at the top so contributors can quickly understand repository layout and ownership.
- When a new folder (or major structural directory) is created, agents must promptly append/update the folder structure description in this file within the same work unit.
- If the `0) Repository folder structure documentation` section is unfilled or partially missing, agents must inspect the repository structure and add missing entries before proceeding with implementation.
- To keep the documentation style reproducible, agents must describe folders using concrete bullets in the form `- \`path\`: purpose` (one line per directory), aligned with the existing "Current top-level structure (summary)" format.
- Folder structure notes must stay concrete (path + purpose) and avoid vague placeholders.
- Current top-level structure (summary):

## 1) Source of truth for requirements
- Agents must read and follow the latest versioned requirements file named `requirements_vX.X.md`.
- If multiple versions exist, use the highest version number unless explicitly instructed otherwise by the user.
- Do not implement behavior that conflicts with the active `requirements_vX.X.md`.
- If no `requirements_vX.X.md` and no `requirements.md` exist, agents must work with the user interactively to define both requirements and technical details before implementation.

## 2) Workflow compliance
- Agents must follow the implementation process in `workflow.md`.
- Work should be executed in the order and constraints defined there unless the user explicitly requests a different order.
- If there is any ambiguity between implementation choices, resolve it by checking `workflow.md` first, then the active `requirements_vX.X.md`.
- If `workflow.md` is missing, agents must create it based on the active requirements document (`requirements_vX.X.md` or `requirements.md`) and must ask the user for confirmation before creating it.

## 3) Git commit discipline
- Agents must commit to git frequently during substantial work.
- Minimum expectation: commit after each meaningful, testable unit of progress (not just at the very end).
- Commit messages should be specific and describe the concrete change delivered.

## 4) Progress logging is mandatory
- Agents must maintain `progress.md` as an ongoing execution log.
- If `progress.md` does not exist, create it before or with the first implementation change.
- After each meaningful work unit, append a specific summary including:
  - date/time (JST)
  - files changed
  - what was implemented or fixed
  - validation performed (tests/checks/run status)
  - next planned step
- Avoid vague entries like "updated code"; entries must be specific enough for handoff.

## 5) Conflict handling
- If instructions conflict, prioritize in this order:
  1. explicit user request
  2. active `requirements_vX.X.md`
  3. `workflow.md`
  4. this `AGENTS.md`
- When conflicts are discovered, document the decision and rationale in `progress.md`.

## 6) Rule division and subagent usage
- Agents must keep rules appropriately divided by concern and scope to reduce ambiguity and avoid duplicated guidance across files.
- Agents must proactively use subagent features for parallelizable or specialized tasks when it improves execution speed or quality.
- When subagents are used, record delegation scope and outcomes in `progress.md`.

## 7) Keeping process docs in sync with user-driven changes
- If user requests or mid-stream specification changes require updates to `workflow.md` and/or the active `requirements_vX.X.md`, agents must update those files promptly to reflect the new agreed behavior.
- When such updates are made, record the change, rationale, and impacted sections in `progress.md` (including date/time JST and files changed).
- If the change results in a new requirements version, create a new `requirements_vX.X.md` with an incremented version number and clearly document what changed from the previous version.
