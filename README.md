# Connect to Ponta

Ponta gives your AI app the tools to do real work on your own Windows PC. Your AI app can sort files, run commands, use desktop apps, work in a web browser and read or draft email. Anything risky waits for your yes.

This repository holds no code. It shows how to add Ponta to an AI app. Ponta's server is hosted, so there is nothing to install from here.

## Before you start

- You need a 64-bit Windows 10 or 11 PC with Ponta's agent on it. The set up guide shows how: https://ponta.ai/help/set-up
- You need a Ponta account. Ponta is in private beta. Join the beta at https://ponta.ai with your Google account. If Ponta is full, you get a place on the waitlist.

## The address

```
https://mcp.ponta.ai/mcp
```

This is a remote MCP server over Streamable HTTP. Your AI app signs in with OAuth 2.1, using your Google account.

## Add it to your AI app

1. In your AI app's settings, find where you add a custom connector or a remote MCP server.
2. Paste the address `https://mcp.ponta.ai/mcp`.
3. When the Ponta page opens, check which app is asking. Then choose Continue with Google.
4. Sign in with the same Google account you use for Ponta.

We have tested Ponta with Claude, ChatGPT and Grok. Ponta is independent and is not endorsed by the makers of these apps. The steps for each app are at https://ponta.ai/help/connect-your-ai-app

### Apps with a settings file

Some apps keep their MCP servers in a JSON settings file. Add Ponta there as a remote server by its address. Key names differ from app to app, so check your app's help. A typical entry looks like this:

```json
{
  "mcpServers": {
    "ponta": {
      "url": "https://mcp.ponta.ai/mcp"
    }
  }
}
```

Your app must support sign-in for remote servers. It opens the Ponta page the first time it connects.

## What your AI app gets

One address gives your AI app every set of tools your PCs have. That can be files and commands, browser, mail, screen and My Chrome. Each tool's name starts with its set, such as `files_` or `mail_`.

## You stay in charge

When a step needs your yes, your phone tells you. If you do not answer, nothing runs. Read how Ponta keeps your PCs and data safe: https://ponta.ai/security

## Help and privacy

Help: https://ponta.ai/help. Privacy notice: https://ponta.ai/privacy. Questions go to support@ponta.ai.

Ponta is made by Roadmap Consulting Ltd, a UK company, trading as Ponta.

## Licence

This README is released under the MIT licence. See LICENSE.
