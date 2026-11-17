# Carrier MCP

Programmable eSIM and mobile connectivity for your agent. Carrier is the control plane for mobile connectivity, like Stripe for telecom: manage eSIM fleets, create and sell connectivity plans, and simulate an order with a free test eSIM before going live.

Works with Claude, Cursor, VS Code and any MCP client. 144 tools (72 read, 52 write, 20 admin) and 5 prompts.

MCP registry name: `llc.carrier/mcp` · npm: [`@carrierllc/mcp`](https://www.npmjs.com/package/@carrierllc/mcp) · site: https://carrier.llc

## Install

Local (stdio):

```bash
npx -y -p @carrierllc/mcp carrier-mcp
```

Claude Desktop / Cursor config:

```json
{
  "mcpServers": {
    "carrier": {
      "command": "npx",
      "args": ["-y", "-p", "@carrierllc/mcp", "carrier-mcp"],
      "env": { "CARRIER_API_KEY": "your-key" }
    }
  }
}
```

Hosted (streamable HTTP, sign in with Google, GitHub or email):

```
https://mcp.carrier.llc/mcp
```

## Environment variables

Set at least one. With none, the server exits.

| Variable | Enables |
| --- | --- |
| `CARRIER_API_KEY` | Starts the server and enables the storefront management tools. |
| `CARRIER_API_TOKEN` | Durable inventory tools such as `assign_package`. |
| `CARRIER_OCS_API_TOKEN` | The explicit OCS tools. |

## First run

> Install the Carrier MCP, then order the free test eSIM (test_global_1gb) and show me the order status.

## License

MIT. See [LICENSE](LICENSE).
