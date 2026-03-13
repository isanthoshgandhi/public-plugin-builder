# Claude Plugin Builder

> Build a complete Claude plugin in 23 guided steps — from raw idea to GitHub push.

A Claude skill by [Santhosh Gandhi](https://github.com/isanthoshgandhi) that interviews you, classifies your plugin type, generates all necessary files, and pushes them to your GitHub repo — with a single confirmation.

Works on **claude.ai** (generates files as code blocks) and **Claude Code** (writes files + pushes automatically).

---

## Install

```bash
claude plugin marketplace add https://github.com/isanthoshgandhi/claude-plugin-builder
claude plugin install claude-plugin-builder
```

---

## What It Does

Building a Claude plugin means knowing SKILL.md format, agent architecture, `plugin.json`, `marketplace.json`, GitHub structure, SEO topics, and trigger phrase engineering — all at once, all correct on the first try.

Claude Plugin Builder collapses that into a conversation.

### 23-Step Pipeline

| Phase | Steps | What Happens |
|---|---|---|
| Discovery | 1–7 | Vision, audience, goal, input, output, open source search, platform target |
| Design | 8–10 | Output template, trigger phrases, plugin name + tagline |
| Classify | 11–13 | Auto-classify type, dependency check, auto-generate SEO |
| Generate | 14–19 | SKILL.md, agent file, scripts, plugin.json, marketplace.json, README |
| Push | 20–23 | File review, error scenarios, confirm, push to GitHub |

### Auto-Classification

```
SKILL        → Pure reasoning, works on claude.ai + Claude Code
AGENT        → Requires Python/Bash/file system, Claude Code only
SKILL+AGENT  → Skill for claude.ai, Agent extends it on Claude Code
COMMANDS     → 3+ distinct named operations
```

### Auto-Generated SEO

From your description alone, the skill generates:
- GitHub topics (8–10 kebab tags)
- Repo description
- marketplace.json description
- README headline

---

## Example Output

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLAUDE PLUGIN BUILDER
Build a stock analysis skill
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
CLASSIFICATION
Type:       SKILL + AGENT
Compatible: claude.ai (Skill) + Claude Code (Agent)
Reason:     Requires yfinance + file output

OPEN SOURCE FOUND:
① yfinance — Yahoo Finance data via Python
② pandas — data manipulation and tabular output

FILES TO BE GENERATED:
├── .claude-plugin/plugin.json
├── .claude-plugin/marketplace.json
├── skills/stock-analyzer/SKILL.md
├── agents/stock-analyzer.md
├── scripts/fetch_data.py
└── README.md
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Confirm push? (yes/no)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
✓ PUSHED
Install: claude plugin marketplace add https://github.com/you/stock-analyzer
         claude plugin install stock-analyzer
Topics to add: claude-plugin, stock-analysis, finance, yfinance, claude-code
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

---

## Trigger Phrases

- *"Build me a Claude plugin that..."*
- *"I want to create a Claude skill for..."*
- *"Help me make a new agent"*
- *"How do I structure a Claude plugin?"*
- *"New plugin"*
- *"Plugin builder"*
- *"Create a skill"*

---

## Platform Behaviour

| Feature | claude.ai | Claude Code |
|---|---|---|
| 23-step interview | ✓ | ✓ |
| File generation | As code blocks | Written to disk |
| Auto push to GitHub | ✗ | ✓ |
| Agent + script generation | ✓ | ✓ |
| Open source search | ✓ | ✓ |

---

## Built From Experience

Built from direct experience developing production Claude plugins — learning what actually works in the real plugin ecosystem.

Key principles applied throughout:
- `description:` frontmatter = activation trigger, not a label
- Output template design matters more than pipeline complexity
- Platform detection must be handled explicitly, not assumed
- Confirmation gates before every irreversible action
- Windows-compatible paths throughout

---

## Author

**Santhosh Gandhi** · [github.com/isanthoshgandhi](https://github.com/isanthoshgandhi)
