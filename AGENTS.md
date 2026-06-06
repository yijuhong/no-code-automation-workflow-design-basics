# Agent Mission Compliance Harness

This repository is governed by `MISSION.md`. Agents must treat this file as
the mandatory execution contract for every implementation, validation, final
deliverable, commit, and pull request.

## Mission Authority

- `MISSION.md` is the single source of truth for the active assignment.
- Read `MISSION.md` in full before planning, editing, validating, committing, or
  opening a pull request.
- Follow every requirement in `MISSION.md` strictly, completely, and faithfully.
- Do not weaken, skip, replace, infer away, or loosely reinterpret mission
  requirements.
- If any user request, repository convention, assumption, tool behavior, or
  implementation detail conflicts with `MISSION.md`, stop and surface the
  conflict before proceeding.
- If `MISSION.md` is absent, do not invent mission scope or proceed with
  mission-bound implementation work. The only allowed exception is an explicit
  meta-task to create or maintain the mission harness itself.

## Execution Discipline

- Convert `MISSION.md` requirements into concrete acceptance criteria before
  editing files.
- Keep all work traceable to those criteria. Every material change must satisfy
  a stated mission requirement.
- Use the narrowest change that fully satisfies `MISSION.md`.
- Do not add unrelated features, documents, workflows, scaffolding, summaries,
  templates, or deliverables unless `MISSION.md` explicitly requires them.
- Do not substitute a plan, checklist, outline, review log, or process note for
  the deliverable that `MISSION.md` actually requires.
- If a requirement is ambiguous, preserve the strictest reasonable
  interpretation and identify the ambiguity in the final response or PR body.
- If a requirement cannot be satisfied with the available information or tools,
  stop and report the blocker instead of completing a partial or approximate
  substitute.

## Validation Gate

Before declaring work complete, committing, or opening a pull request, agents
must validate the full diff and final deliverable against `MISSION.md`.

Validation must confirm:

- Every required deliverable exists.
- Each deliverable has the document type, purpose, and character required by
  `MISSION.md`.
- No required section, evidence item, acceptance criterion, test, or artifact is
  missing or incomplete.
- No extra deliverable or unrelated artifact has been added outside the mission
  scope.
- The final answer describes only completed, verified work and clearly reports
  any unresolved blocker.

Any mismatch is a blocking `FAIL`.

## Pull Request Review Gate

Before opening any pull request, agents must run a dedicated review subagent.

The review subagent must:

- Evaluate only. It must not edit files, stage changes, commit, push, or open a
  pull request.
- Review the complete diff against `MISSION.md` and this `AGENTS.md` harness.
- Verify that the final deliverable matches the document type and intent
  required by `MISSION.md`.
- Return exactly one of these statuses: `PASS` or `FAIL`.
- Provide concise reasons for the status.

A `FAIL` blocks the pull request until the issue is corrected and the review
subagent returns `PASS`.

## Final Deliverable Gate

The final deliverable must match the exact document type and intent required by
`MISSION.md`.

Blocking failures include:

- Delivering a template when `MISSION.md` requires an evidence-based report.
- Delivering a checklist, execution plan, or workflow log when the mission
  requires a finished user-facing artifact.
- Omitting any required deliverable.
- Adding final deliverables not specified by `MISSION.md`.
- Leaving placeholders, TODOs, unverifiable claims, or incomplete evidence in a
  final artifact.

## Pull Request Requirements

- Open a pull request only after all validation gates pass.
- The pull request body must explain how the diff satisfies `MISSION.md`.
- Include the validation performed and the review subagent result.
- Do not hide limitations, skipped checks, unresolved ambiguities, or blockers.

## Non-Compliance Rule

If any gate in this harness cannot be satisfied, the correct outcome is to stop
and report the blocking condition. Shipping a weaker interpretation of the
mission is not allowed.
