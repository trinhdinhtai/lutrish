# AGENTS.md

## Agent skills

### Issue tracker

Issues are tracked in GitHub Issues on `trinhdinhtai/lutrish` (via the `gh` CLI). See `docs/agents/issue-tracker.md`.

### Triage labels

Default vocabulary: `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: one `GLOSSARY.md` and `docs/adr/` at the repo root. See `docs/agents/domain.md`.

### Branch per ticket

Before starting work on any ticket, create a new branch from an up-to-date `main`. Never commit ticket work directly on `main`. Name it `<type>/<issue#>-<short-slug>`; drop the number when there is no issue. Work lands on `main` through a pull request.

### Small commits

Commit ticket work as several small commits, one per logical step, so each can be reviewed on its own. Never put a whole ticket in one commit. Put new dependencies in their own `build:` commit. Every commit must stand alone: typecheck, lint and its tests pass. Fold review fixes into the commit they fix while the branch is unpushed; after that, add a small `fix:` commit.
