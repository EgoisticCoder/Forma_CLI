# FORMA CLI

**A visual coding agent for your terminal.** FORMA pairs your coding model with a permissioned Playwright browser and a specialist UI/UX auditor, so you can inspect a page, make a code change, and verify the result in one workflow.

[![npm version](https://img.shields.io/npm/v/@forma-ai/forma)](https://www.npmjs.com/package/@forma-ai/forma) [![License: MIT](https://img.shields.io/badge/License-MIT-8a8c70.svg)](./LICENSE) [![Node.js 20+](https://img.shields.io/badge/Node.js-20%2B-43853d)](https://nodejs.org/)

## Install

```sh
npm install --global @forma-ai/forma
forma
```

On first launch, connect a FORMA vision endpoint and your coding provider. FORMA works with OpenAI-compatible providers and local Ollama models. Credentials are stored in `~/.forma/config.json` with owner-only file permissions.

## The loop

1. Open your page in an isolated Playwright Chromium session at desktop, tablet, or mobile size.
2. Inspect the DOM, console, network, accessibility, layout, and visual hierarchy.
3. Ask the FORMA vision model for a screenshot-based UI/UX audit.
4. Let your chosen coding model make a change, with file and browser actions gated by your approvals.
5. Capture the result and compare the visual change.

## What it can do

- Work with your coding model and FORMA's screenshot-trained UI/UX auditor.
- Inspect and interact with a dedicated browser, including scroll, hover, click, and responsive viewport changes.
- Gather DOM, console, network, accessibility, contrast, spacing, performance, and visual-diff evidence.
- Ask before file edits, shell commands, and browser actions; configure per-tool permissions.
- Stream responses, show progress, suggest slash commands, and switch models, providers, credentials, or themes in the CLI.

## Useful commands

```sh
forma config
forma audit https://example.com
forma audit https://example.com --headed --lighthouse
forma eval ./screenshots
```

Inside the interactive session, use `/help` for the full command list. `/tools` lists browser tools; `/theme` changes the terminal palette; `/model`, `/provider`, and `/credentials` update model settings.

The optional headed mode launches a separate Chromium process. FORMA does not attach to your normal browser profile or read its cookies and saved passwords. Local and private URLs require explicit opt-in.

## Requirements

- Node.js 20 or newer
- A FORMA-compatible vision endpoint for screenshot audits
- A tool-calling coding model (or local Ollama model) for interactive code changes

## Links

- [GitHub repository](https://github.com/EgoisticCoder/Forma_CLI)
- [npm package](https://www.npmjs.com/package/@forma-ai/forma)
- [FORMA MCP server](https://github.com/EgoisticCoder/Forma_MCP)
- [FORMA CLI website](https://forma-cli-website.vercel.app/)
- [FORMA project](https://github.com/EgoisticCoder/Forma)

## License

MIT. See [LICENSE](./LICENSE).
