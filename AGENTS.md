# Repository Guidelines

## Project Structure & Module Organization
This repository is currently a lightweight scaffold with minimal checked-in files. Keep contributor-facing docs at the root (for example, `AGENTS.md`, `README.md`) and place implementation work under clearly named top-level folders as the project grows.

Recommended layout:
- `skills/<skill-name>/` for reusable skill definitions and instructions.
- `scripts/` for automation helpers (setup, validation, release tasks).
- `tests/` for automated checks that mirror `skills/` or `scripts/` structure.

## Build, Test, and Development Commands
No build system is enforced yet. Prefer adding a `Makefile` or `package.json` scripts when tooling is introduced.

Common local commands used in this repo today:
- `rg --files` lists tracked files quickly.
- `find . -maxdepth 3 -type f` inspects current workspace contents.
- `git status` reviews local changes before commits.

If you introduce new tooling, document canonical commands in `README.md` (for example, `make test`, `pnpm test`, or `pytest`).

## Coding Style & Naming Conventions
Use Markdown-first, automation-friendly conventions:
- Indentation: 2 spaces for YAML/JSON, 4 spaces for Python, and no tabs.
- File names: kebab-case for docs and assets (example: `skill-checklist.md`).
- Directories: lowercase, descriptive, and singular where practical (example: `scripts`, `tests`).

## Commit & Pull Request Guidelines
Follow clear, scoped commits:
- Commit format: `type(scope): summary` (example: `docs(agents): add contributor guide`).
- Keep commits focused; avoid mixing refactors with behavior changes.

PRs should include:
- What changed and why.
- Linked issue/task when applicable.

## Security & Configuration Tips
Do not commit secrets, tokens, or machine-specific config. Use `.env.example` for new environment variables and keep real credentials in local, untracked files.
