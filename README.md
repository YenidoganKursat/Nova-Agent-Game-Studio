# Nova Agent Game Studio

> **Codex-native agentic game dev studio template** for solo devs & small teams.

## TL;DR
- Opinionated workflow + docs to treat Codex like a disciplined studio (design, engineering, art, audio, QA, production)
- Heavy documentation index (you start from `docs/00-TABLE-OF-CONTENTS.md`)
- Ready to scale from “prototype” to “ship”: ADRs, playbooks, engine presets (Godot / Unity / Unreal), release checklists

## Why this exists
Most "agent" setups become chaotic: threads diverge, decisions aren’t recorded, and you lose auditability. Nova Agent Game Studio enforces structure:

- **Studio hierarchy:** director → leads → specialists
- **Explicit output contracts:** design doc → task breakdown → implementation → validation
- **Decision trails:** ADRs & specs required for risky changes
- **Minimal ceremony at prototype time**, increasing rigor as the project matures

## What’s included
- `.codex/agents/` — custom agents organized by department
- `.agents/skills/` — reusable skills/workflows (review, testing, validation, etc.)
- `docs/` — dense documentation set (see TOC)
- `studio/` — living project state (planning, status, risks)

## Getting started
### Requirements
- Node.js + npm
- `@openai/codex` CLI

### Install
```bash
npm install -g @openai/codex
``` 

### Initialize project
```bash
codex
```

### Trust project (first run)
When Codex prompts you to trust the project, accept. This enables project-scoped config.

### Run
Use the scripts in `scripts/` to bootstrap and validate project state.

## Script index
- `scripts/bootstrap.sh` — initial setup
- `scripts/install_git_hooks.sh` — installs repo hooks
- `scripts/validate_repo_layout.py` — verifies required folders
- `scripts/validate_docs.py` — lint docs
- `scripts/validate_assets.py` — validate asset manifest

## Documentation (high detail)
All docs are indexed under `docs/`.

- `00-TABLE-OF-CONTENTS.md` — master index
- `01-INTENT.md` — goals, constraints, scope
- `02-ARCHITECTURE.md` — system/agent topology
- `03-WORKFLOW.md` — how to work daily
- `04-CODING-STANDARDS.md` — style, reviews, test policy
- `05-DESIGN.md` — game design docs (GDD, combat, quests)
- `06-ENGINE-PRESETS.md` — Godot/Unity/Unreal presets
- `07-QA.md` — test cases, regression checklists
- `08-RISK-REGISTER.md` — risk log
- `09-ADR/` — architecture decision records

> ⚠️ Note: GitHub web only lets me create files one by one. I’m prioritizing the critical docs and the high-level index; you can expand `docs/` as you execute the studio playbooks.

## Contributing
- Open an issue with your objective
- Create a draft spec (design + acceptance criteria)
- Implement
- Run validation scripts
- Submit

## License
MIT
