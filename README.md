# agents-config

Personal Claude Code / agent configuration for [@yfuks](https://github.com/yfuks).

This repo holds the configuration that shapes how AI coding agents behave across all of my projects: global rules and reusable skills.

## Contents

- **[`AGENTS.md`](./AGENTS.md)**: Global rules applied in every scenario, regardless of the project. These are the baseline standards (quality over development cost, engineering excellence, best practices) that individual projects layer their own instructions on top of.
- **[`skills/`](./skills)**: Reusable agent skills. Each skill is a directory with a `SKILL.md` (and optional `references/`).

## Skills

| Skill | Source | What it does |
| --- | --- | --- |
| [`react-doctor`](./skills/react-doctor) | Vendored from [react.doctor](https://www.react.doctor/) | Runs automatically when finishing React work: scans the codebase for security, performance, correctness, and architecture issues, checks the health score did not regress, and drives a full local triage/fix loop on `/doctor`. |

### Regenerating `react-doctor`

The `react-doctor` skill is produced by its official CLI, not hand-written. Treat it as vendored and regenerate it rather than editing in place:

```bash
# In a throwaway dir containing a React package.json:
npx react-doctor@latest install --yes
# then copy .claude/skills/react-doctor/ over skills/react-doctor/
```

## Usage

These files are meant to be picked up by agent tooling (e.g. Claude Code) as global config. Symlink or copy them into the relevant location: `AGENTS.md` into your global instructions, and `skills/` into `~/.claude/skills/`.

On this machine, `~/.claude/skills` is a symlink to this repo's `skills/`, so any skill added here becomes available to Claude Code automatically.
