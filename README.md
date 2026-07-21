# Agentic Coding Lab

An offline-first field guide for learning terminal habits, safe agentic coding, Git review, debugging, and evidence-based workflows.

Open `index.html` directly in a browser, or publish it as a static GitHub Pages site. No build step, package manager, account, analytics, or network dependency is required.

## What is included

- Eight short, practical coding and terminal missions.
- An ADHD-friendly drop-in mode for returning through one small next move.
- A deliberately curated external-learning map.
- A private local station for commands, MCP references, local-model notes, and long-form non-secret setup knowledge.
- A downloadable, editable standalone station that persists its own changes locally in the browser.

## Privacy model

This repository contains only the application source. It does **not** contain a user's local station entries, progress, notes, API keys, tokens, model settings, MCP configurations, or downloaded station snapshots.

The lab stores learner-created content in the browser's local storage. That data never becomes part of `index.html` unless the user deliberately downloads an updated private station file. Treat those downloaded station files as private and do not commit or upload them.

Read [PRIVACY.md](PRIVACY.md) before hosting a fork or contributing.

## Run locally

Double-click `index.html`, or serve this directory with any static server. The application is deliberately self-contained and has no external assets.

## Publish with GitHub Pages

1. Create a public GitHub repository named `agent-lab`.
2. Push this repository's `main` branch.
3. In the repository: **Settings → Pages → Source**, select **GitHub Actions**.
4. The included workflow publishes `index.html` after every push to `main`, and can also be run manually from the Actions tab.

GitHub Pages supports custom GitHub Actions workflows using `configure-pages`, `upload-pages-artifact`, and `deploy-pages`; the included workflow follows the current documented pattern. [GitHub Pages documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)

## Before publishing a fork

- Do not add `.env` files, API keys, access tokens, logs, raw MCP configuration files, or model paths.
- Do not commit a downloaded `private-local-station-*.html` file.
- Use Keychain or a dedicated secret manager for credentials; save only human-readable references in the local station.
- Review `git status` and the staged diff before every push.

## License

[MIT](LICENSE)
