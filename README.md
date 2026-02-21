# 🔍 Ask Microsoft Docs

Ask Microsoft's official documentation anything - powered by GitHub Copilot and the Microsoft Learn MCP Server.

**Free. No API keys. Five-minute setup.**

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/<OWNER>/ask-microsoft-docs?quickstart=1)

Replace `<OWNER>` in the badge URL with your GitHub username or organization name.

## What is this?

This is a starter template that lets GitHub Copilot answer your questions using Microsoft's official documentation. You open it in GitHub Codespaces, switch Copilot Chat to Agent mode, and ask about products like Excel, Azure, Outlook, .NET, and Power Automate. Copilot searches Microsoft Learn and replies with source links you can click and verify. In short: less guessing, more trusted answers.

## What do I need?

- A free GitHub account
- GitHub Copilot (Copilot Free is fine, with monthly usage limits)
- Nothing else: no API keys, no Azure subscription, no local setup required

## Quick start

1. Click **Use this template** at the top of this repo, or use the **Open in GitHub Codespaces** badge above.
2. Wait for your Codespace to finish loading. Then open Copilot Chat:
   Windows/Linux: `Ctrl+Alt+I`
   macOS: `Cmd+Alt+I`
3. In Copilot Chat, change the mode to **Agent** (important).
4. Click the tools icon (`🔧`) in chat and confirm you can see `microsoft-learn` with tools like `microsoft_docs_search` and `microsoft_docs_fetch`.
5. Ask your first question, for example:
   `How do I freeze panes in Excel? search Microsoft Learn`

If you do not see Microsoft Learn tools, reload the window:
`Ctrl+Shift+P` -> `Developer: Reload Window`

## Example prompts

See [example-prompts.md](example-prompts.md) for a full list across Office, Azure, and developer topics.

Quick examples:
- `search Microsoft Learn for all ways Copilot in Outlook can help me prep for a meeting`
- `How do I use XLOOKUP instead of VLOOKUP? search Microsoft Learn`
- `Give me Azure CLI commands to create an Azure Container App with managed identity. search Microsoft Learn`
- `What are the current Azure OpenAI quotas and limits? fetch full doc`

## How it works

This repo contains a small config file that VS Code reads automatically. That file tells Copilot how to connect to Microsoft's free documentation server through MCP (Model Context Protocol). MCP is simply a standard way for AI tools to safely pull outside information. In Agent mode, Copilot can search Microsoft docs and pull full pages while it answers. The result is practical answers with direct links back to the original docs.

## Tips for best results

- Use **Agent** mode (not Ask or Edit mode)
- Add `search Microsoft Learn` to prompts to make sure docs tools are used
- Add `fetch full doc` when you want the complete page content
- Ask follow-up questions; Copilot keeps tool context
- If an answer feels generic, make your prompt more specific

## Codespace hours

GitHub Free currently includes **120 core-hours/month** for Codespaces. A typical 2-core Codespace gives about **60 hours** of usage. Stop your Codespace when done (auto-stop is usually 30 minutes of inactivity by default).

Learn more: https://docs.github.com/en/billing/managing-billing-for-your-products/managing-billing-for-github-codespaces/about-billing-for-github-codespaces

## Using locally (without Codespaces)

1. Create a repo from this template (or clone your own copy).
2. Open it in VS Code 1.99 or later.
3. VS Code will automatically detect `.vscode/mcp.json`.
4. Open Copilot Chat, switch to Agent mode, and start asking questions.

## Credits & related

- Microsoft Learn MCP Server: https://github.com/MicrosoftDocs/mcp
- MCP specification: https://modelcontextprotocol.io
- GitHub Copilot docs: https://docs.github.com/en/copilot
- Inspired by the approach described in connecting ChatGPT to the Microsoft Learn MCP server

## License

MIT.
