# Yakusoku for Claude Code

Plan a wedding in [Yakusoku](https://yakusoku.com.au) from Claude Code: guests and RSVPs, seating, menu, budget, tasks, calendar, vendors, photos, the gift registry and messages. Vendors manage their listings, bookings, invoices and questionnaires.

The plugin connects Claude Code to Yakusoku's remote MCP server, `https://yakusoku.com.au/api/mcp`, and adds a `wedding-planning` skill that tells Claude how to use its tools: find the wedding first, preview bulk changes before committing them, and ask before anything that contacts people or deletes.

## Install

```
/plugin marketplace add yakusoku-software/yakusoku-plugins
/plugin install yakusoku@yakusoku
```

Then run `/mcp`, choose **yakusoku**, sign in to Yakusoku and choose what Claude can do. Without the plugin, `claude mcp add --transport http yakusoku https://yakusoku.com.au/api/mcp` adds the server alone.

Requires a Yakusoku account. Disconnect at any time from Settings → AI assistants in Yakusoku. Guide: https://yakusoku.com.au/guides/connect-ai-assistant-to-yakusoku
