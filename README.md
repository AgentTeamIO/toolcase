# ToolCase — Curated MCP Server Collection

Open-source MCP servers for AI agents. Curated by [AgentTeam](https://agentteam.app), published to the official [MCP Registry](https://registry.modelcontextprotocol.io).

## What is ToolCase

ToolCase is a curated collection of production-ready MCP (Model Context Protocol) servers that give AI agents real-world capabilities. Each server is open-source, tested, and published to the official MCP Registry so any MCP-compatible client can use them.

## Install

```bash
agentteam tools add {server-name}
```

This installs the server locally and configures it for your agents.

## Server Structure

Each server lives in its own directory under `servers/`:

```
servers/{name}/
├── src/           # Server implementation
├── server.json    # MCP official format metadata
├── README.md      # Documentation
└── package.json   # or Cargo.toml — dependencies
```

## Available Servers

See [registry.json](./registry.json) for the full list, or browse the `servers/` directory.

## Contributing

We welcome contributions via pull requests. Each server must include:

1. **`server.json`** in MCP official format (name, description, version, tools/resources/prompts)
2. **`README.md`** with usage instructions and examples
3. **`src/`** with a working implementation
4. **Tests** covering core functionality

### Steps

1. Fork this repo
2. Create `servers/{your-server-name}/`
3. Implement the MCP server with `server.json` metadata
4. Open a PR — we'll review and merge
5. On merge, the server is auto-published to the MCP Registry

## Relationship to MCP Registry

ToolCase is a **source** for the official MCP Registry at [registry.modelcontextprotocol.io](https://registry.modelcontextprotocol.io). We publish there — we don't compete with or replace it. Any MCP client can discover ToolCase servers through the official registry.

## License

[Apache 2.0](./LICENSE)
