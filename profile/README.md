# Anseta Labs

Open source tooling for the [Anseta](https://anseta.com) staking platform — a multi-chain
staking API covering Ethereum, Solana, Cosmos networks, Cardano, and more.

Everything here is a client for that API. None of it holds keys, and none of it broadcasts
transactions: the write endpoints return **unsigned** transactions for a user to review and
sign in their own wallet.

## Projects

| Repository | What it is |
|---|---|
| [**mcp**](https://github.com/anseta-labs/mcp) | An MCP server exposing the staking API to AI agents as 12 curated tools. Runs locally over stdio; works with Claude Code, Claude Desktop, and Cursor. |
| [**typescript-sdk**](https://github.com/anseta-labs/typescript-sdk) | Type-safe TypeScript client generated from the OpenAPI specification. |

## Getting started

Both projects need an Anseta API key. Request one through your Anseta account contact.

**AI agents** — add the MCP server to your client:

```bash
claude mcp add anseta --env ANSETA_API_KEY=your-key -- npx -y @anseta/mcp
```

**Applications** — install the SDK:

```bash
npm install @anseta/typescript-sdk
```

## A note on amounts

Every token amount in these APIs is a **string in the token's base denomination**, never a
decimal token value. 1 SOL at 9 decimals is `"1000000000"`. Both clients document this
prominently, because it is the single easiest thing to get wrong when a program — or a
language model — constructs a staking transaction.

## Contributing

Issues and pull requests are welcome on any repository.
