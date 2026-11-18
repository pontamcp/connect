# Install notes for AI agents

These notes are for an AI agent, such as Cline, that adds Ponta for a person. Read README.md too.

Ponta is a hosted remote MCP server. There is nothing to download, build or run. Do not use npx, a local command or an API key.

## The server

- Name: `ponta`
- Address: `https://mcp.ponta.ai/mcp`
- Transport: Streamable HTTP
- Sign-in: OAuth 2.1. The app registers itself and opens Ponta's sign-in page in the browser. The person signs in with Google. Never ask for a password or a token.

## Cline

Add this entry under `mcpServers` in Cline's MCP settings file, `cline_mcp_settings.json`. Keep any servers already there.

```json
{
  "mcpServers": {
    "ponta": {
      "type": "streamableHttp",
      "url": "https://mcp.ponta.ai/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

In Cline 4, the file is at `~/.cline/data/settings/cline_mcp_settings.json`. On Windows that is `%USERPROFILE%\.cline\data\settings\cline_mcp_settings.json`. Create the folder and the file if they are missing.

After you save the file, Cline connects to the server. The server asks for sign-in, so Cline shows an Authenticate button beside Ponta in its MCP servers list. Ask the person to press it, then sign in with Google on the Ponta page. Once signed in, Ponta's tools appear in the list.

## Other apps

Use the same address as a remote server. Key names differ from app to app. The README has a typical entry.

## Before it works

The person needs a Ponta account and a 64-bit Windows 10 or 11 PC with Ponta's agent on it. Ponta is in private beta. If the person has no account, point them to https://ponta.ai to join the beta, and to https://ponta.ai/help/set-up for the PC.
