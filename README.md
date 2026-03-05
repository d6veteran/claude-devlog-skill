# Devlog Skill for Claude

A custom Claude skill that maintains a structured development changelog (`DEVLOG.md`) in your GitHub repository. It captures architectural decisions, progress milestones, key conversation takeaways, and strategic decisions — so critical context from your development conversations doesn't evaporate between sessions.

## What It Does

- **Proactively suggests** devlog entries when significant decisions, milestones, or insights come up in conversation
- **Accepts ad-hoc entries** when you say "log this" or "add to devlog"
- **Writes detailed entries** with category tags, summaries, full context, and rationale
- **Auto-pushes to GitHub** after you approve each entry
- **Works with any project** — not tied to a specific repo or product

## Entry Categories

| Category | What It Captures |
|---|---|
| `architecture` | Technical design decisions, data model changes, stack choices |
| `milestone` | Completed work, version releases, phase transitions |
| `takeaway` | Key insights, lessons learned, important context |
| `strategy` | Business decisions, market positioning, go-to-market pivots |

## Installation

1. Download the `devlog.skill` file from this repo
2. In Claude.ai, open your Project
3. Go to Project Settings → Skills
4. Upload the `devlog.skill` file

## Usage

Once installed, the skill activates automatically. You can:

- **Let Claude suggest entries** — it will offer to log significant decisions at natural pause points
- **Request entries directly** — say "log this", "devlog", or "add this to the devlog"
- **Review before pushing** — Claude always shows you the draft entry before committing to GitHub

On first use each session, Claude will ask for your GitHub repo URL and Personal Access Token (the environment resets between sessions).

## DEVLOG.md Format

Entries are reverse-chronological (newest first) and follow this structure:

```markdown
## [2025-03-04] Brief descriptive title

**Category:** `architecture`
**Tags:** `relevant`, `topic`, `tags`

### Summary
A 1-2 sentence overview of what happened or was decided.

### Detail
Full context including what was decided, why, what alternatives
were considered, and implications for future work.

### Related
- Links to related entries or documents
```

## Repository Contents

| File | Purpose |
|---|---|
| `SKILL.md` | The skill source file — Claude's instructions for how the devlog works |
| `devlog.skill` | Installable package — upload this to Claude.ai to install the skill |
| `README.md` | This file — repo documentation |
| `LICENSE` | License terms |

## License

See [LICENSE](LICENSE) for details.
