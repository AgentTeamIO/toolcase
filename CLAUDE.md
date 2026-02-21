# ToolCase — MCP Server Collection

## What This Is
Curated collection of open-source MCP servers. Published to MCP official Registry.

## Structure
- `servers/{name}/` — each MCP server
  - `src/` — server implementation
  - `server.json` — MCP official format metadata
  - `README.md` — documentation
  - `package.json` or `Cargo.toml` — dependencies

## Adding a Server
1. Create `servers/{name}/` directory
2. Implement the MCP server
3. Create `server.json` in MCP official format
4. PR -> review -> merge -> auto-publish to MCP Registry

## MCP Official Format (server.json)
```json
{
  "name": "server-name",
  "description": "What it does",
  "version": "1.0.0",
  "tools": [],
  "resources": [],
  "prompts": []
}
```

## Integration
- `agentteam tools add {name}` installs from ToolCase
- `list_tools` MCP tool shows available ToolCase servers
