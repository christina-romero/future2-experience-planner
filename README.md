# Alpha × HISD — Future 2 Skills

Internal Claude Code **plugin marketplace** for the Alpha team on the HISD
partnership. Ships the skills we use to build Future 2 Experiences curriculum.

> **Internal / proprietary.** Contains HISD-specific curriculum rules, the locked
> Scope & Sequence sheet ID, and staff-internalized conventions. Keep this repo
> **private**.

## Plugins

| Plugin | What it does |
| --- | --- |
| **future2-lesson-builder** | Locked operational build spec + styled HTML template for authoring Future 2 Experiences lesson plans (grades 3-8) as Google Docs matched to the locked HISD Scope & Sequence. Enforces fixed-vs-alterable S&S columns, design-type discipline (Skills Lab = scored checkpoint only), scalable materials, the hands-on testable-stake core, per-indicator through-line moves, the 3-stage AI arc, a required forward-written Connection, and a pre-ship checklist. |

## Install (Claude Code / Agent SDK) — recommended, auto-updates

```
/plugin marketplace add <owner>/alpha-hisd-future2-skills
/plugin install future2-lesson-builder@alpha-hisd-future2
```

Then invoke the skill with `/future2-lesson-builder`. `git pull` (or re-run
`/plugin marketplace update`) to get new versions.

## Install (claude.ai / Claude Desktop)

Those surfaces don't read marketplaces. Download
`dist/future2-lesson-builder.zip` and upload it under
**Settings → Capabilities → Skills → Upload skill**.

## Companion skills (recommended, not bundled)

- `future2-lesson-generation` — governing philosophy (canonical-first, fidelity gate). Wins on conflict.
- `lesson-injection` — lesson-writing clarity/quality bar.

## Layout

```
.claude-plugin/marketplace.json          # marketplace manifest
plugins/future2-lesson-builder/
  .claude-plugin/plugin.json             # plugin manifest
  skills/future2-lesson-builder/         # the skill (SKILL.md + assets)
dist/future2-lesson-builder.zip          # same skill, zipped for app upload
```

## Maintaining

- The single source of truth for all lessons is the **locked HISD Scope &
  Sequence**: `17UFR-Lzd4Lupz6lgsJ_d7_bJcnbA_D23_ZV8tLCaCwo`. If HISD locks a new
  sheet, update the `## Authoritative source` block in the skill's `SKILL.md`,
  bump the versions in the two manifests, re-zip into `dist/`, and push.
