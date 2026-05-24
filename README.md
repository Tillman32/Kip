# Kip ✨

> *"I love technology, but not as much as you, you see."*  
> — **Kip Dynamite**

**A curated collection of AI agent skills, packaged with [APM](https://github.com/microsoft/apm).**

Napoleon once said: *"You know, like nunchuck skills, bow-hunting skills, computer hacking skills. Girls only want boyfriends who have great skills."*

Kip heard that. Kip built this repo.

---

## Get Started

Install the full package into your AI assistant:

```bash
apm install tillman/kip
```

Or grab a single skill:

```bash
apm install tillman/kip --skill ssh-exec
```

> **New to APM?** It's `npm` for AI agent skills. → [Quick Start](https://microsoft.github.io/apm/getting-started/quick-start/)

---

## Skills

| Name | Description | Domain | Works With |
|------|-------------|--------|------------|
| [ssh-exec](./.apm/skills/ssh-exec/SKILL.md) | Run non-interactive commands on remote Linux hosts over SSH. Risk confirmation and audit logging built in. | Infrastructure | Copilot, Claude |

> More skills incoming. LaFawnduh is very supportive of this project.

---

## How It Works

Every skill lives in `.apm/skills/<name>/SKILL.md`. `apm install` injects the relevant instructions directly into your AI assistant — Copilot, Claude, Cursor, Codex, and more. No copy-pasting prompts. No manual setup.

```
kip/
└── .apm/
    └── skills/
        └── ssh-exec/
            ├── SKILL.md       ← the skill definition
            └── AUDIT-LOG.md   ← auto-generated audit trail
```

→ [APM Docs](https://microsoft.github.io/apm/) · [Package Types](https://microsoft.github.io/apm/reference/package-types/)

---

## Contributing

Got a skill Kip would approve of? Check [CONTRIBUTING.md](./CONTRIBUTING.md) for the directory structure, frontmatter spec, and PR checklist.

*"It's pretty much my favorite repo."* — Kip (probably)

---

<sub>Made by [Brandon Tillman](https://tillmanbuildstech.com) · Powered by [APM](https://github.com/microsoft/apm)</sub>

