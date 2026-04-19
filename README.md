# paircode-gemini

Gemini CLI extension that registers `/paircode` as a slash command.

**This repo contains only the slash-command manifest.** The actual Python tool lives at [`starshipagentic/paircode`](https://github.com/starshipagentic/paircode) and must be installed separately.

## Install

```bash
# 1. Install the paircode Python CLI (once)
pipx install paircode

# 2. Register /paircode with Gemini (this repo)
gemini extensions install https://github.com/starshipagentic/paircode-gemini --consent
```

Inside gemini, run `/commands reload` (or restart your session), then type `/paircode` — the slash command is listed.

## Alternative: let paircode's installer do it for you

```bash
pipx install paircode
paircode install      # registers /paircode in Gemini, Claude, Codex all at once
```

## What's in here

```
gemini-extension.json     extension manifest
commands/
  paircode.toml           the /paircode slash-command prompt
```

Versions here track the main paircode release via `scripts/release.py` in the paircode repo.

## License

MIT. See `LICENSE`.
