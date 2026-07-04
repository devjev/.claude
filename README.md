# .claude

Global [Claude Code](https://claude.com/claude-code) configuration, versioned with git.

This is the actual `~/.claude` directory. It contains a lot of runtime state
(session history, caches, credentials) that must not be committed, so the
`.gitignore` works as a whitelist: everything is ignored by default, and each
tracked file is explicitly un-ignored with a `!` rule.

## Tracked files

- `CLAUDE.md` — global instructions applied to all projects
- `.gitignore` — the whitelist itself
- `LICENSE`

## Adding a file to tracking

1. Add a `!<filename>` line to `.gitignore`
2. `git add` and commit as usual

Never track `.credentials.json` or anything under `sessions/`, `history.jsonl`,
or the cache directories — they contain secrets and machine-local state.

## License

[MIT](LICENSE)
