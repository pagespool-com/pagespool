---
name: "pagespool"
description: "Seven open-source document engines behind one API key: Docling, MarkItDown, WeasyPrint, veraPDF, Gotenberg, OCRmyPDF, EPUBCheck. Use it through the pagespool MCP servers under https://api.pagespool.com/mcp/."
license: "MIT"
compatibility: "Needs network access to https://api.pagespool.com; a tool that needs an account asks for an API key or a sign-in."
---

# pagespool

pagespool hosts seven open-source document engines under their own names: Docling, MarkItDown, WeasyPrint, veraPDF, Gotenberg, OCRmyPDF and EPUBCheck. Each engine has its own REST API, MCP server and free tool, and one API key and one credit balance pay for all seven. Docling, veraPDF and Gotenberg answer on their own routes, so their clients work with a new base URL. The servers are in Germany. The free plan has 100 credits a month and needs no card.

## Connect

- MCP endpoints (streamable HTTP), one per server:
  - Docling by pagespool: https://api.pagespool.com/mcp/docling/
  - MarkItDown by pagespool: https://api.pagespool.com/mcp/markitdown/
  - WeasyPrint by pagespool: https://api.pagespool.com/mcp/weasyprint/
  - veraPDF by pagespool: https://api.pagespool.com/mcp/verapdf/
  - Gotenberg by pagespool: https://api.pagespool.com/mcp/gotenberg/
  - OCRmyPDF by pagespool: https://api.pagespool.com/mcp/ocrmypdf/
  - EPUBCheck by pagespool: https://api.pagespool.com/mcp/epubcheck/
- A tool that needs an account asks you to sign in; an API key in the `X-API-Key` header works instead. The Claude Code plugin reads it from `PAGESPOOL_API_KEY`.
- API reference: https://api.pagespool.com/docs

Maintained by the pagespool team.
