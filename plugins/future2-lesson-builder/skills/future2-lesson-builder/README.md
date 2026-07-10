# future2-lesson-builder

Internal Alpha × HISD skill. The locked operational rulebook + styled doc
template for authoring Future 2 Experiences lesson plans (grades 3-8) as Google
Docs that match HISD's Scope & Sequence.

**Audience:** the Alpha team on the HISD partnership. Keeps org specifics on
purpose (the locked S&S sheet ID, staff-internalized titles, Google Drive tooling).

## What it enforces
Fixed-vs-alterable S&S columns · Lesson Type = S&S Design Type (Skills Lab =
scored checkpoint only) · scalable/low-cost materials · a real hands-on core with
a binary win test · per-indicator through-line moves, escalated by band · the
3-stage AI arc · a required, forward-written Connection · the exact styled HTML
lesson-plan template · a pre-ship checklist.

## Single source of truth
All lessons align to the **LOCKED HISD Scope & Sequence**:
`17UFR-Lzd4Lupz6lgsJ_d7_bJcnbA_D23_ZV8tLCaCwo` ("Cycle 1 Scope & Sequence",
tabs `34` / `56` / `78`). Match the six fixed columns exactly; only
EO / Activity / Materials / Est. Cost reflect the build.

## Contents
- `SKILL.md` — the rulebook (authoritative source + 11 rules + locked format + tooling + pre-ship checklist)
- `assets/lesson-plan-template.html` — the exact styled template with `{{PLACEHOLDER}}`s

## Companion skills (recommended, not bundled)
- `future2-lesson-generation` — governing philosophy (canonical-first, fidelity gate). Wins on conflict.
- `lesson-injection` — lesson-writing clarity/quality bar.

The rulebook stands alone, but install these alongside it for full coverage.

## Install

**Claude Code / Agent SDK**
- Personal: copy the `future2-lesson-builder/` folder into `~/.claude/skills/`.
- Project: copy it into `<repo>/.claude/skills/`.
- Verify it loads, then invoke with `/future2-lesson-builder`.

**Claude.ai & Claude Desktop**
- Settings → Capabilities → **Skills** (must be enabled) → **Upload skill** →
  select `future2-lesson-builder.zip`.

**Claude Developer Platform (API)**
- Upload the folder via the Skills API and attach it to the code-execution container.

## Team rollout (one source, auto-updates)
Put this folder in a shared git repo as a Claude Code **plugin** in a
**marketplace** so teammates install and update with one command; distribute the
same `.zip` for anyone on claude.ai / Desktop.

## Versioning
Update the `## Authoritative source` block in `SKILL.md` if HISD locks a new S&S
sheet ID, and re-zip. Keep `name:` = folder name (`future2-lesson-builder`).
