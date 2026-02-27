# Claude Skills

A collection of custom skills for Claude — built for personal use, shared in case they're useful to others.

Each skill lives in its own folder and comes with a `.skill` file for easy installation in Claude.ai.

---

## Available Skills

| Skill | Description |
|---|---|
| [adhd-support](./adhd-support/) | Cognitive copilot for ADHD. Detects your state (paralysis, overwhelm, planning, focus, transitions) and adapts its support accordingly. |

---

## Installation

### Claude Code (CLI)

Skills in Claude Code are configured through your `~/.claude/settings.json` file. Each skill is a markdown file (`SKILL.md`) that Claude loads when invoked.

**1. Clone or copy the skill folder into your Claude config directory:**

```bash
# Option A: clone the whole repo
git clone https://github.com/your-username/claude-skills ~/.claude/skills

# Option B: copy just the skill you want
cp -r adhd-support ~/.claude/skills/adhd-support
```

**2. Register the skill in `~/.claude/settings.json`:**

```json
{
  "skills": [
    {
      "name": "adhd-support",
      "description": "Cognitive copilot for ADHD states — paralysis, planning, focus, transitions, and more.",
      "path": "~/.claude/skills/adhd-support/SKILL.md"
    }
  ]
}
```

**3. Use it in any Claude Code session:**

```
/adhd-support
```

---

### Claude.ai (Web)

Each skill comes with a pre-packaged `.skill` file for direct upload to Claude.ai.

**1. Download the `.skill` file** for the skill you want (e.g., `adhd-support.skill`).

**2. In Claude.ai**, go to your profile → **Skills** → **Upload skill** and select the `.skill` file.

**3. The skill will be available** in your conversations automatically, or you can invoke it explicitly.

---

## Skill Structure

Every skill has a folder with at minimum a `SKILL.md` — the main definition file with behavior, rules, and instructions. Beyond that, each skill can include whatever supporting files it needs (templates, reference guides, strategy docs, etc.) and reference them from `SKILL.md`.

```
skill-name/
├── SKILL.md        # Required — main skill definition
├── templates.md    # Optional — whatever the skill needs
└── other-file.md
```

---

## Contributing / Adding Skills

If you want to add a new skill, follow the same structure:

1. Create a folder with the skill name (e.g., `writing-coach/`)
2. Add a `SKILL.md` with the skill's behavior definition
3. Add a `references/` folder for any supporting files
4. Package it as `skill-name.skill` for Claude.ai distribution

---

## License

[MIT](./LICENSE)
