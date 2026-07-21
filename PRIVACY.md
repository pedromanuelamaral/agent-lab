# Privacy and safe publishing

## What the public site does

Agentic Coding Lab is a static, offline-first HTML application. It does not include analytics, tracking pixels, remote fonts, external JavaScript, cookies, accounts, API calls, or a server-side database.

## Local data

Progress, course notes, drop-in notes, and the local station are stored in browser local storage on the user's device. The public GitHub Pages deployment cannot read this data.

The optional standalone station is a private HTML export. It can contain commands and configuration context, so users should keep it out of repositories, cloud shares, and public issue attachments.

## Never store or publish

- API keys, access tokens, passwords, recovery codes, or private keys
- `.env` files or raw environment dumps
- raw MCP server configuration containing credentials
- private paths, device identifiers, personal logs, or copied terminal history
- downloaded `private-local-station-*.html` files

Use a secret manager or operating-system keychain for credentials. Save only a non-secret reference such as `Keychain: OPENAI_API_KEY` in the station.

## For maintainers

Before pushing, inspect the staged content:

```sh
git diff --cached --check
git diff --cached
```

If sensitive content is accidentally committed, rotate any exposed credential immediately. Removing the file in a later commit does not remove it from Git history.
