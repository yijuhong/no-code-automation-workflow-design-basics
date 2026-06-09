# Agent Instructions

## Authority

- `MISSION.md` is binding; follow it exactly.
- Never weaken, skip, reinterpret, or generalize it.
- Validate material changes, deliverables, and PRs; stop and surface conflicts.

## Discipline

- Check repo facts before guessing.
- Ask only when intent, scope, or acceptance criteria are not derivable.
- Stay scoped.
- Missing evidence, requirement gaps, unsupported claims, and unapproved extras block delivery.

## Gates

- Before any PR, run a read-only subagent review against `MISSION.md` and changes.
- Classify the PR as final completion or scoped partial completion; unclear claims fail.
- Validate final PRs against all of `MISSION.md`; validate partial PRs against their claimed scope and consistency with `MISSION.md`.
- Return `PASS` or `FAIL` with concise reasons.
- Deliverables must match required type, intent, scope, and completeness; templates, plans, drafts, incomplete work, unsupported claims, and extras fail.
