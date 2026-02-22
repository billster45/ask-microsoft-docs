# 🔍 Ask Microsoft Docs

Ask Microsoft's official documentation anything - powered by GitHub Copilot and the Microsoft Learn MCP Server.

**Free. No API keys. Five-minute setup.**

## What is this?

This is a starter template that lets GitHub Copilot answer your questions using Microsoft's official documentation. You open it in GitHub Codespaces, switch Copilot Chat to Agent mode, and ask about products like Excel, Azure, Outlook, .NET, and Power Automate. Copilot searches Microsoft Learn and replies with source links you can click and verify. In short: less guessing, more trusted answers.

## What do I need?

- A free GitHub account: https://github.com/signup
- GitHub Copilot is included with every GitHub account, with a default free allowance (Copilot Free).
- Copilot Free currently includes:
  - 50 agent mode or chat requests per month
  - 2,000 completions per month
  - Access to Haiku 4.5, GPT-5 mini, and more
- For paid upgrades and current pricing, see: https://github.com/features/copilot/plans
- Nothing else: no API keys, no Azure subscription, no local setup required

## Quick start

1. Create your own repo from this template.
   Recommended (private by default):
   `https://github.com/new?template_owner=billster45&template_name=ask-microsoft-docs&visibility=private`
   Or click **Use this template** at the top of this repo.

   ![Use this template button](docs/images/template-sm.png)

2. In your new repo, click **Code** -> **Codespaces** -> **Create codespace on main**.

   ![Create codespace on main](docs/images/codespace-sm.png)

3. Wait for your Codespace to finish loading. Then open Copilot Chat:
   Windows/Linux: `Ctrl+Alt+I`
   macOS: `Cmd+Alt+I`
4. Agent mode is usually on by default. If it is not, switch the mode dropdown to **Agent**.
5. Click the config tools icon in chat.

   ![Open Copilot tools configuration](docs/images/config-sm.png)

6. Check the `microsoft-learn` box, then click **Update tools**.

   ![Select microsoft-learn and click Update tools](docs/images/tick-sm.png)

7. You should now see the Microsoft Learn tools loaded.

   ![Microsoft Learn tools loaded in Copilot](docs/images/loaded-sm.png)

8. Ask your first question:
   `How do I freeze panes in Excel? search Microsoft Learn`

   ![Example query in Copilot chat](docs/images/query-sm.png)

If you do not see Microsoft Learn tools, reload the window:
`Ctrl+Shift+P` -> `Developer: Reload Window`

## Privacy note

Your Copilot chat is not automatically published to the internet. What can become public is content you save to a public repository.

- If you want private work by default, create your repo as **Private**.
- Do not commit sensitive prompts, internal notes, or secrets.
- Codespaces are tied to your account, but forwarded ports can be shared if you set them to public.
- Use private ports unless you intentionally want to share a running app.

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

- Agent mode is usually default, but double-check if tools do not run
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
