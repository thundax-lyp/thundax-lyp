# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a GitHub profile README project. The root contains `README.md`, the primary content rendered on the profile page. Static assets live in `resources/`; for example, `resources/networkx_logo.svg` is available for README or future documentation use. IDE metadata is excluded through `.gitignore`, and `.idea/` should remain untracked.

If the repository grows, keep source files in a clearly named top-level directory such as `src/`, tests in `tests/`, and documentation in `docs/`. Keep profile-only assets under `resources/`.

## Build, Test, and Development Commands

There is no package manager, build system, or test suite configured yet. Useful local checks are:

```sh
git status
```

Shows pending changes before committing.

```sh
find . -maxdepth 3 -type f | sort
```

Reviews the visible repository layout.

```sh
git diff -- README.md AGENTS.md
```

Checks documentation edits before opening a pull request.

## Coding Style & Naming Conventions

Use Markdown for repository documentation. Keep headings short and descriptive, prefer sentence-case prose, and keep HTML blocks in `README.md` consistently indented with four spaces where nested. Use relative paths for local assets, such as `resources/example.svg`, and descriptive lowercase file names with hyphens or underscores for new assets.

Avoid committing generated files, editor metadata, or local workspace settings. Update `.gitignore` when introducing new tools.

## Testing Guidelines

No automated tests are present. For documentation changes, manually preview `README.md` in GitHub or a Markdown viewer and confirm that badges, links, images, and HTML sections render correctly. For SVG or image assets, verify paths are correct and alt text is meaningful when referenced from Markdown.

If code is added later, introduce a matching test command and document it here. Prefer colocated or clearly mirrored test names, such as `tests/test_feature.py` for `src/feature.py`.

## Commit & Pull Request Guidelines

Recent history uses concise `README` commit messages. Continue with short, imperative messages that identify the touched area, for example `Update README badges` or `Add contributor guide`.

Pull requests should include a brief summary, the files changed, and screenshots or rendered previews for visual README changes. Link related issues when applicable, and call out any new tooling, generated assets, or manual verification performed.

## Agent-Specific Instructions

Keep edits scoped and documentation-focused unless the user asks for broader changes. Do not remove profile content or assets without explicit direction. When adding commands or workflows, ensure they work before documenting them.
