# Pagespool

**Seven open-source document engines behind one API key: Docling, MarkItDown, WeasyPrint, veraPDF, Gotenberg, OCRmyPDF, EPUBCheck.**

Pagespool hosts seven open-source document engines under their own names: Docling, MarkItDown, WeasyPrint, veraPDF, Gotenberg, OCRmyPDF and EPUBCheck. Each engine has its own REST API, MCP server and free tool, and one API key and one credit balance pay for all seven. Docling, veraPDF and Gotenberg answer on their own routes, so their clients work with a new base URL. The servers are in Germany. The free plan has 100 credits a month and needs no card.

## Use it from

### MCP servers

One streamable-HTTP endpoint per server. A tool that needs an account
asks you to sign in; an API key in the `X-API-Key` header works instead.

| Server | Endpoint |
|---|---|
| Docling by Pagespool | `https://api.pagespool.com/mcp/docling/` |
| MarkItDown by Pagespool | `https://api.pagespool.com/mcp/markitdown/` |
| WeasyPrint by Pagespool | `https://api.pagespool.com/mcp/weasyprint/` |
| veraPDF by Pagespool | `https://api.pagespool.com/mcp/verapdf/` |
| Gotenberg by Pagespool | `https://api.pagespool.com/mcp/gotenberg/` |
| OCRmyPDF by Pagespool | `https://api.pagespool.com/mcp/ocrmypdf/` |
| EPUBCheck by Pagespool | `https://api.pagespool.com/mcp/epubcheck/` |

Claude Code, one server:

```sh
claude mcp add --transport http pagespool-docling https://api.pagespool.com/mcp/docling/
```

Claude Code, every server: `/plugin marketplace add pagespool-com/pagespool` then `/plugin install pagespool@pagespool` (set `PAGESPOOL_API_KEY` for your key).

Cursor / Windsurf / Cline / Claude Desktop:

```json
{
  "mcpServers": {
    "pagespool-docling": {
      "url": "https://api.pagespool.com/mcp/docling/"
    }
  }
}
```

One-click installs for every client: https://pagespool.com/connect

**Integrations** (Dify, Python SDK and templates): https://github.com/pagespool-com/pagespool-integrations

## Links

- **Website:** https://pagespool.com/go/github
- **API docs:** https://api.pagespool.com/docs · [OpenAPI](https://api.pagespool.com/openapi.json)
- **Pricing:** https://pagespool.com/pricing
- **Convert HTML to PDF free:** https://pagespool.com/tools/html-to-pdf
- **llms.txt:** https://pagespool.com/llms.txt
- **Privacy policy:** https://pagespool.com/privacy
- **Support:** https://pagespool.com/support

## API

Base URL `https://api.pagespool.com/` — authenticate with an `X-API-Key` header;
anonymous calls work at a lower rate limit.

## About the files here

- `.claude-plugin/` — Claude Code plugin, with this repo as its own marketplace.
- `.mcp.json` — the MCP servers the Claude Code plugin connects to.
- `gemini-extension.json` — Gemini CLI extension manifest.
- `glama.json` — Glama server claim (names the maintainer).
- `mcp.json` — Agent Plugins 1.0 MCP server config.
- `plugin.json` — Agent Plugins 1.0 plugin manifest.
- `skills/` — an Agent Skill (agentskills.io SKILL.md) for skill galleries.
