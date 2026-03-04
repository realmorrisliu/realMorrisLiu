# Repository Guidelines

## Source of Truth
For all future profile/content updates, use `https://github.com/realmorrisliu/realmorrisliu.com` as the canonical reference.  
When content differs between repositories, prefer the `realmorrisliu.com` version and align this profile repo to it.

## Project Structure & Module Organization
This repository is a GitHub Profile project. The primary content lives in [`README.md`](README.md), which renders on the profile page (`github.com/realmorrisliu`).

- `README.md`: Profile content (intro, projects, contact, image links).
- `.git/`: Version history and metadata.
- Optional future assets: place local images in `assets/` and reference with relative paths (for example, `![Banner](assets/banner.png)`).

Keep the repository lightweight: avoid adding app scaffolding unless the repo purpose changes.

## Build, Test, and Development Commands
There is no compile/build pipeline for this repo. Use lightweight validation commands:

- `git status` - check pending changes.
- `git diff -- README.md AGENTS.md` - review Markdown edits before commit.
- `markdownlint README.md AGENTS.md` - lint Markdown formatting (if `markdownlint` is installed).
- `lychee README.md` - validate external links (if `lychee` is installed).

## Coding Style & Naming Conventions
Use clean, readable Markdown with consistent structure.

- Use ATX headings (`#`, `##`) and keep a single H1 per file.
- Prefer short sections and bullet lists over long paragraphs.
- Keep line breaks intentional; avoid trailing whitespace.
- Use descriptive link text instead of raw URLs when possible.
- For new files/folders, use lowercase kebab-case names (example: `assets/profile-banner.png`).

## Testing Guidelines
No automated test framework is configured. Validation is content-focused:

- Preview rendered Markdown locally or in GitHub’s file preview.
- Verify all links and image references resolve correctly.
- Confirm profile sections remain scannable on desktop and mobile widths.

## Commit & Pull Request Guidelines
Current history is mostly `Update README.md`; keep commits focused and explicit.

- Prefer imperative messages: `docs: refine profile intro`, `docs: update project links`.
- Keep one logical content change per commit.
- PRs should include: what changed, why it changed, and a quick render check summary.
- For visual/format-heavy updates, include a screenshot of rendered output.

## Security & Configuration Tips
Do not commit secrets, personal tokens, or private email aliases you do not want publicly indexed. Assume all profile content is public and searchable.
