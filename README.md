# Claude Skills

Shared development skills for AI coding assistants. Install these globally to make them available across all projects.

## Installation

Clone this repo to your local skills directory:

```bash
git clone https://github.com/15MariamS/claude-skills.git ~/.claude/skills/claude
```

That's it! Skills are now available in all your projects.

## Available Skills

### `/handover` - Session Handover Generator
Generates comprehensive handover documents for development sessions.

**Usage**: Type `/handover` in any conversation to create a `HANDOVER.md` file documenting:
- What you worked on
- What got done / didn't work
- Key decisions made
- Lessons learned & gotchas
- Next steps
- Important files
- Open questions

**When to use**: End of coding sessions, before handing off work, or when context switching between features.

---

### `vercel-react-best-practices` - React Performance Optimization
59 performance optimization rules from Vercel Engineering covering:
- Eliminating async waterfalls (CRITICAL)
- Bundle size optimization (CRITICAL)
- Server-side performance (HIGH)
- Client-side data fetching
- Re-render optimization
- Rendering performance
- JavaScript performance
- Advanced patterns

**Usage**: Automatically applied when writing React/Next.js code. Reference specific rules in `~/.claude/skills/claude/vercel-react-best-practices/rules/`

---

## Updating Skills

To get the latest skill updates:

```bash
cd ~/.claude/skills/claude
git pull
```

## Contributing

To add or improve skills:
1. Fork this repo
2. Add/modify skills in their respective directories
3. Create a PR for review
4. After merge, update your local installation with `git pull`

---

## Structure

```
claude/
├── handover/
│   └── SKILL.md
└── vercel-react-best-practices/
    ├── SKILL.md
    ├── metadata.json
    ├── README.md
    └── rules/ (59 optimization rules)
```
