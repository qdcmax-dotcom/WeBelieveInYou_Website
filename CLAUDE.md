# CLAUDE.md

Instructions for Claude when working in this repository.

## Branch naming
- Never use randomly generated or session-ID branch names.
- Before making any changes, create a branch named `type/short-description` in lowercase kebab-case.
- Allowed types:
  - `feature/` — new functionality (e.g. `feature/scene-export`)
  - `fix/` — bug fixes (e.g. `fix/login-crash`)
  - `docs/` — README or documentation changes (e.g. `docs/setup-guide`)
  - `refactor/` — code cleanup with no behavior change
  - `test/` — adding or updating tests
  - `chore/` — config, dependencies, tooling
- If the environment requires a `claude/` prefix to push, use `claude/type-short-description` (e.g. `claude/fix-login-crash`) with no random suffix.
- If you can't control the branch name, say so at the start and tell me the name you ended up with.

## Never work directly on main
- `main` must always work. All changes go through a branch and a pull request.

## Commits
- Small, focused commits with clear messages in present tense: "Add login form", "Fix upload timeout".
- No vague messages like "update" or "changes".

## Pull requests
- Title: short summary of the change.
- Description: what changed, why, and how to test it.
- Explain changes in plain language — I'm still learning Git and GitHub.

## Tests
- Run existing tests before opening a PR and report the results.
- Add or update tests in `tests/` for any new feature or bug fix.
- Don't open a PR with failing tests without clearly saying which ones fail and why.

## Repo structure
Keep this layout unless the project already uses a different standard:
```
README.md          what the project is and how to run it
.gitignore         files Git should skip
src/               source code
tests/             automated tests
docs/              extra documentation
.github/workflows/ automated test (CI) setup
```

## Safety
- Never commit secrets, API keys, passwords, or `.env` files.
- Ask before deleting files, rewriting Git history, or force-pushing.
