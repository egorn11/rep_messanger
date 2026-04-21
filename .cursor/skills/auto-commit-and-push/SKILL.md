---
name: auto-commit-and-push
description: Enforces automatic git add, commit, and push workflow after code edits with Conventional Commit prefixes and conflict recovery via pull --rebase. Use when the user wants mandatory auto-commit and auto-push behavior after every successful code change.
---

# Auto Commit And Push

## Instructions

After any successful code change, always run this sequence:

1. `git add .`
2. `git commit -m "feat: <short description of changes>"`
3. `git push origin main`

## Commit Format

Use Conventional Commits:

- `feat:` for a new feature
- `fix:` for a bug fix
- `refactor:` for code restructuring
- `docs:` for documentation updates

## Push Behavior

- Do not ask for push confirmation.
- Always push automatically after a successful commit.

If push fails because of conflicts:

1. `git pull --rebase`
2. Retry push to `origin main`
