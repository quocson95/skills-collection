# Skills Collection

Claude Code skills.

| Skill | What it does |
|---|---|
| [`motion-director`](motion-director/SKILL.md) | Designs, animates, scores and QAs a finished motion-graphics film in code (showreel, product, launch-story, explainer), with an independent critic loop and a measured quality bar. |

## Install

A skill is a folder containing a `SKILL.md`. Claude Code loads skills from two places:

- **Personal (all projects):** `~/.claude/skills/<skill-name>/`
- **Project (one repo, shareable via git):** `<repo>/.claude/skills/<skill-name>/`

### Option 1 — symlink (recommended, stays in sync with this repo)

```bash
mkdir -p ~/.claude/skills
ln -s "$(pwd)/motion-director" ~/.claude/skills/motion-director
```

### Option 2 — copy

```bash
mkdir -p ~/.claude/skills
cp -R motion-director ~/.claude/skills/
```

### Option 3 — into a single project

```bash
mkdir -p /path/to/project/.claude/skills
cp -R motion-director /path/to/project/.claude/skills/
```

Restart Claude Code (or start a new session), then check it's listed by asking *"what skills do you have?"*.

## Use

- Type `/motion-director`, or just ask for a showreel / product video / explainer animation and Claude picks it up.
- Fill in the brief first: copy `motion-director/templates/brief.md` into your video project. Blank lines are decided by Claude and logged with a reason.

### Requirements on the machine

- `ffmpeg` / `ffprobe` (render, loudness, freeze detection)
- Node.js, plus your chosen toolchain (Remotion, or a headless-browser HTML + GSAP renderer)
- Any API keys for voice/music generation set as environment variables, never in files

## Uninstall

Run the one that matches how you installed:

```bash
rm ~/.claude/skills/motion-director       # if symlinked
rm -rf ~/.claude/skills/motion-director   # if copied
```
