# OFMAPI MCP server

The OFMAPI Model Context Protocol server is **hosted**. There is nothing to
install and no npm package: point your AI client at one URL.

```
https://api.ofmapi.com/mcp/v1/
```

- Transport: Streamable HTTP (keep the trailing slash)
- Tools: 174, covering the REST API plus computed operations such as top
  spenders, churn risk, and a creator overview
- Auth: OAuth 2.1 for Claude and ChatGPT; a scope-limited Bearer API key for
  Cursor, VS Code, and other config-based hosts
- Accounts can be referenced by creator name or @handle
- Public Beta: free, no card, 100 tool calls per calendar month

## Config files

- [`clients/cursor.mcp.json`](clients/cursor.mcp.json): Cursor `mcpServers` shape with a Bearer key
- [`clients/vscode.mcp.json`](clients/vscode.mcp.json): VS Code `.vscode/mcp.json` with a password input for the key

Claude and ChatGPT do not use a config file: add the URL as a custom
connector or app and complete OAuth.

## Setup guides

- Overview and example prompts: https://ofmapi.com/integrations/mcp
- Step-by-step for Claude, ChatGPT, Cursor, and VS Code:
  https://ofmapi.com/docs/integrations/mcp
- Rate limits and the Beta quota: https://ofmapi.com/docs/rate-limits

## Try asking

- "Top 5 spenders for Camila this week, with handles and totals."
- "Who is about to churn across all my creators? Rank by lifetime spend."
- "Draft a re-engagement DM for @ogkanug fans who have not replied in 14 days."

## What this repository is for

Issues and discussion about the hosted server. If a local stdio bridge is
published later, its source will live here.

## License

MIT. See [LICENSE](LICENSE).

---

OFMAPI is an independent organisation, not affiliated with OnlyFans.com or
Fenix International Limited. "OnlyFans" is a registered trademark of Fenix
International Limited.
