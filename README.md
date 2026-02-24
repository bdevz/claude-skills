# Claude Code Skills

Custom skills for [Claude Code](https://docs.anthropic.com/en/docs/claude-code/skills) that extend Claude's capabilities with domain-specific knowledge and workflows.

## Skills

### live-sales-coach

Real-time sales coaching for live customer calls. Paste transcript chunks from a live discovery, demo, or pricing call and get immediate tactical advice.

- Identifies call phase (opening, discovery, demo, pricing, objection, closing)
- Reads prospect signals and provides word-for-word talking points
- Grounded in proven frameworks: Gap Selling, Challenger, 30MPC
- Tuned for selling AI solutions at $500-$1,500/month with land-and-expand strategy

**Usage in Claude Code:**
```
/live-sales-coach <paste transcript>
```

Or just paste a call transcript — Claude will auto-detect and activate the skill.

## Installation

Clone into your Claude Code personal skills directory:

```bash
git clone https://github.com/bdevz/claude-skills.git ~/.claude/skills
```

> **Note:** If you already have skills in `~/.claude/skills/`, clone elsewhere and copy the skill folders you want.

## Adding New Skills

1. Create a folder: `~/.claude/skills/my-skill/`
2. Add a `SKILL.md` with frontmatter and instructions
3. Allowlist it in `.gitignore`:
   ```
   !my-skill/
   !my-skill/**
   ```
4. Commit and push

## Structure

```
my-skill/
├── SKILL.md           # Instructions + frontmatter (required)
├── references/        # Detailed docs loaded on-demand
└── scripts/           # Scripts Claude can execute
```

## License

MIT
