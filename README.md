# agentic-utils Claude Plugins

Custom Claude Code plugin marketplace with additional LSP servers.

## Available Plugins

| Plugin | Description | Install |
|--------|-------------|---------|
| `ty-lsp` | Python language server via [ty](https://github.com/astral-sh/ty) | `uv tool install ty@latest` |
| `svelte-lsp` | Svelte language server | `npm install -g svelte-language-server` |

## Installation

Add this marketplace to Claude Code:

```bash
/plugin marketplace add https://github.com/agentic-utils/claude-plugins
```

Then install plugins:

```bash
/plugin install ty-lsp@agentic-utils
/plugin install svelte-lsp@agentic-utils
```

## Local Development

For local development, add to `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "agentic-utils": {
      "source": {
        "source": "directory",
        "path": "/path/to/claude-plugins"
      }
    }
  }
}
```
