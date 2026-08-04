# mcp-podatki-si

Slovenia Open Data (podatki.gov.si) CKAN MCP.

Part of [Pipeworx](https://pipeworx.io) — an MCP gateway connecting AI agents to 1394+ live data sources.

## Tools

| Tool | Description |
|------|-------------|
| `search_datasets` | Search Slovenia Open Data (Slovenia) for datasets by keyword. Returns each dataset's id/name, title, organization, and its resources (each with a resource_id for query_resource). |
| `dataset` | Show full metadata for one Slovenia Open Data dataset by id or name (from search_datasets), including all resources and their resource_ids. |
| `query_resource` | Pull rows from a tabular Slovenia Open Data resource (CKAN DataStore) by resource_id (from a dataset's resources). Optional full-text q, limit, offset. Note: only resources with the DataStore enabled are queryable. |

## Quick Start

Add to your MCP client (Claude Desktop, Cursor, Windsurf, etc.):

```json
{
  "mcpServers": {
    "podatki-si": {
      "url": "https://gateway.pipeworx.io/podatki-si/mcp"
    }
  }
}
```

Or connect to the full Pipeworx gateway for access to all 1394+ data sources:

```json
{
  "mcpServers": {
    "pipeworx": {
      "url": "https://gateway.pipeworx.io/mcp"
    }
  }
}
```

## Using with ask_pipeworx

Instead of calling tools directly, you can ask questions in plain English:

```
ask_pipeworx({ question: "your question about Podatki Si data" })
```

The gateway picks the right tool and fills the arguments automatically.

## More

- [Docs and guides](https://pipeworx.io/docs)
- [pipeworx.io](https://pipeworx.io)

## License

MIT
