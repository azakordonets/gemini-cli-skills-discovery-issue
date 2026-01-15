This repository contains an example of an issue with Gemini CLI discovering skills via symlinks.

## Project Structure
- `.gemini/` holds Gemini CLI configuration for the repo.
- `.gemini/skills` is a symlink to `../.skills`.
- `.skills/` stores local skill definitions (e.g., `make-magic-number/`, `explaining-code/`).
- `devl/python/.gemini/` is a nested Gemini CLI config used for the Python sub-area.
- `screenshots/` contains reproduction images (`from_the_root.png`, `from_internal_folder.png`).
- `AGENTS.md` documents contributor guidance for this repository.
- `README.md` provides the high-level overview and structure summary.

## Symlinks
- Symlinked: `.gemini/skills` -> `../.skills`, `devl/python/.gemini/skills` -> `../../../.skills`
- Not symlinked: `.gemini/`, `.skills/`, `devl/`, `devl/python/`, `devl/python/.gemini/`, `screenshots/`, `AGENTS.md`, `README.md`.

If we run `gemini` from the root of the repository and will ask `What skills do you have?`, we will get the correct list of skills - it will even recognize the `.skills` directory.
Here's the screenshot:

![from_the_root](screenshots/from_the_root.png)

Now, I would expect that when I go to the `devl/python` directory and run `gemini`, it should also discover the skills correctly. However, that's not the case. When running `gemini` from the `devl/python` directory, it fails to discover the skills.
Here's the screenshot:

![from_internal_folder](screenshots/from_internal_folder.png)

| About Gemini CLI | |
| --- | --- |
| CLI Version | 0.24.0 |
| Git Commit | 48ee9bb30 |
| Model | auto-gemini-2.5 |
| Sandbox | no sandbox |
| OS | darwin |
| Auth Method | OAuth |