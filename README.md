# Claude Plugin Builder

> Build complete Claude plugins in 23 guided steps — from raw idea to GitHub push.

**Author:** Santhosh Gandhi · **Version:** 1.0.0

---

## What It Does

Tell it your idea. It interviews you, classifies whether you need a Skill, Agent, or Commands, generates every file you need, and pushes it to your GitHub repo — all in one guided session.

Works on **claude.ai** (generates files as code blocks) and **Claude Code** (writes and pushes automatically).

---

## Install on Claude Code

```bash
claude plugin marketplace add https://github.com/isanthoshgandhi/claude-plugin-builder
claude plugin install claude-plugin-builder
```

Then say:
```
Build a plugin
```
or
```
I want to create a Claude skill
```

---

## The 23-Step Pipeline

| Phase | Steps | What Happens |
|---|---|---|
| Discovery | 1–7 | Vision, audience, goal, input, output, open source search, platform |
| Design | 8–10 | Output template, trigger phrases, name + tagline |
| Classify | 11–13 | Skill / Agent / Commands — auto-classified + SEO generated |
| Generate | 14–19 | SKILL.md, agent file, scripts, plugin.json, marketplace.json, README |
| Review + Push | 20–23 | File tree review, error scenarios, confirm, push |

---

## What You Get

Every run produces a complete, deployable plugin:

```
[plugin-name]/
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── skills/[name]/
│   └── SKILL.md
├── agents/[name].md     ← only if Agent
├── scripts/[name].py    ← only if Agent
└── README.md
```

---

## Built From Experience

Every generated file incorporates lessons from building the foresight-engine plugin:

- `description:` field written as activation trigger, not description
- Explicit I/O file paths in every agent step
- Alias normalization for categorical inputs
- Independent scoring (not forced sum-to-100)
- Windows compatibility (`python` not `python3`)
- Confirm before every push

---

## License

MIT
