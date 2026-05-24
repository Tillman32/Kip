# Contributing to Kip

Kip loves technology. He also loves a clean PR.

---

## Adding a Skill

### 1. Create the skill directory

```
.apm/skills/<your-skill-name>/
├── SKILL.md         ← required
└── AUDIT-LOG.md     ← optional; include if the skill logs executed actions
```

### 2. Write SKILL.md

Start with the required frontmatter:

```yaml
---
name: "your-skill-name"
description: "One sentence. What does this skill do?"
keywords: ["keyword one", "keyword two"]
applyTo: ["trigger phrase one", "trigger phrase two"]
stage: development | operations | analysis | review
domain: infrastructure | frontend | backend | devops | data | security
harnesses:
  - copilot
  - claude
---
```

Then write the skill body. A solid skill includes:

- **Goal** — what the agent is trying to accomplish
- **Assumptions** — what must already be true before the skill runs
- **Required Inputs** — what to collect from the user before acting
- **Decision Flow** — numbered steps for the agent to follow
- **Out of Scope** — what this skill explicitly does NOT handle
- **Example Prompts** — 3–5 trigger phrases that activate this skill

See [ssh-exec](./.apm/skills/ssh-exec/SKILL.md) for a complete reference implementation.

### 3. Open a PR

- One skill per PR
- Include example trigger phrases in the PR description
- If the skill touches destructive or privileged operations, document the confirmation flow in `SKILL.md`

---

## Quality Checklist

Kip has standards. Before submitting, verify:

- [ ] The skill has a single, clear responsibility
- [ ] Trigger phrases are specific enough to avoid accidental activation
- [ ] Risky or destructive actions require explicit user confirmation
- [ ] Out-of-scope cases are documented
- [ ] The skill works with at least one supported harness (Copilot or Claude)

---

## File Naming

Use kebab-case for skill directory names: `my-skill-name`, not `MySkillName` or `my_skill_name`.

---

*"You could be developing skills right now."* — Kip (to you, specifically)
