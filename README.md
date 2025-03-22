MCP server for threat info colletion

[![smithery badge](https://smithery.ai/badge/@xue20010808/threatnews)](https://smithery.ai/server/@xue20010808/threatnews)

Usage :
TOOL: collect_threat_info
arguments": {
      "start_year": "2024",
      "start_month": "3",
      "start_day": "1",
      "end_year": "2024",
      "end_month": "3",
      "end_day": "10"
    }

Cursor settins->Add mcp server[stdio]:
mcp.json:


{
  "mcpServers": {
    "Threat_news": {
      "command": "uv",
      "args": ["--directory", "/Users/sheldon/Desktop/mcp_test/threatmcp","run", "collect.py"],
      "env": {
        "API_KEY": "value"
      }
    },
// if u want to create a neo4j knowledge graph. Thanks to alanse!!!
    "neo4j": {
      "command": "npx",
      "args": ["@alanse/mcp-neo4j-server"],
      "env": {
        "NEO4J_URI": "bolt://localhost:7687",
        "NEO4J_USERNAME": "neo4j",
        "NEO4J_PASSWORD": "123456"
      }
    }

### Installing via Smithery

To install threatnews for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@xue20010808/threatnews):

```bash
npx -y @smithery/cli install @xue20010808/threatnews --client claude
```

