# claude-mood

`/mood` is a custom slash command for Claude Code. Given a theme or mood
in plain language, it rewrites the CLI's spinner verbs (the little phrases
shown next to the spinner while it's working) and saves each generated
theme here so it can be reused across machines.

## Layout

- `commands/mood.md` — the slash command itself.
- `moods/<slug>.json` — saved presets (`theme`, `mode`, `verbs`, `createdAt`).
- `bin/mood-lib` — small helper script the command uses to list, save,
  and sync presets.

## Setup on a new machine

```sh
git clone https://github.com/WhiteAnthrax/claude-mood.git ~/.claude/mood-library
mkdir -p ~/.claude/commands
ln -sf ~/.claude/mood-library/commands/mood.md ~/.claude/commands/mood.md
```

Then just run `/mood <theme>` inside Claude Code.

## Usage

```
/mood ジブリ
/mood ジョジョの名言 長めで
/mood 一覧
```
