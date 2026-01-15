# Repository Guidelines

## Project Structure & Module Organization
This repository is currently empty aside from Git metadata. When adding code, keep a clean top-level layout and document any new directories here. Suggested conventions:
- `src/` for production code
- `tests/` for automated tests
- `docs/` for design or usage notes
- `scripts/` for developer tooling

If you introduce assets (images, fixtures), place them under `assets/` or a clearly named subfolder (e.g., `tests/fixtures/`).

## Build, Test, and Development Commands
No build or test tooling is configured yet. Once added, list canonical commands here, for example:
- `npm run build` for production builds
- `npm test` for unit tests
- `make lint` for style checks

Keep commands runnable from the repository root and keep output deterministic.

## Coding Style & Naming Conventions
No formatting or linting tools are defined. If you add one, document it and prefer automatic formatting on save or in CI. Keep naming consistent within a language:
- Use `snake_case` for file names in scripts, `kebab-case` for configs, and `PascalCase` for types/classes.
- Use 2 spaces for indentation in JSON/YAML and follow the language community standard elsewhere.

## Testing Guidelines
Testing frameworks are not yet selected. When adding tests, keep names descriptive and co-locate with `tests/` or use `*.test.*` patterns. Document coverage expectations and the fastest test command.

## Commit & Pull Request Guidelines
There is no commit history yet, so no existing convention. Use concise, imperative commit messages (e.g., "Add initial scaffolding"). Pull requests should include a clear description, steps to verify, and link any related issues.

## Security & Configuration
Do not commit secrets. If configuration is required, provide a template like `.env.example` and document required variables.

## Agent-Specific Instructions
Follow `AGENTS.md` for repository guidance and keep changes minimal, explicit, and well-scoped.
