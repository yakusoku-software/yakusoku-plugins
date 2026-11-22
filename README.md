# Yakusoku plugins

Connect an AI assistant to [Yakusoku](https://yakusoku.com.au) and plan a wedding in conversation: guests and RSVPs, seating, menu, budget, tasks, calendar, vendors, photos, the gift registry and messages. Vendors manage their listings, bookings, invoices and questionnaires.

Every plugin here connects to Yakusoku's remote MCP server, `https://yakusoku.com.au/api/mcp`. You sign in to Yakusoku and choose what the assistant can do. Requires a Yakusoku account; disconnect at any time from Settings → AI assistants in Yakusoku.

| Assistant | Install |
| --- | --- |
| Claude Code | `/plugin marketplace add yakusoku-software/yakusoku-plugins`, then `/plugin install yakusoku@yakusoku`, then `/mcp` to sign in |
| Cursor | The Cursor marketplace, or **Add to Cursor** in Yakusoku's Settings → AI assistants |
| Gemini CLI | `gemini extensions install https://github.com/yakusoku-software/yakusoku-plugins` |
| Antigravity | `agy plugin install https://github.com/yakusoku-software/yakusoku-plugins` |
| Any MCP client | Add `https://yakusoku.com.au/api/mcp` as a remote (streamable HTTP) server |

Guide: https://yakusoku.com.au/guides/connect-ai-assistant-to-yakusoku

The files are MIT licensed (`LICENSE`). The Yakusoku name and logo are trademarks of Yakusoku Software and are not covered by that license.

This repository is generated from Yakusoku's main repository; changes made here are overwritten. Report problems at https://yakusoku.com.au/contact.
