# Candid calculators (MCP server)

Free UK personal finance calculators from [Candid](https://www.candid-finance.co.uk/), served as a remote MCP server so an AI assistant can run them.

**Server URL:** `https://www.candid-finance.co.uk/mcp` (Streamable HTTP, no sign-in)

Listed in the official MCP Registry as `uk.co.candid-finance/calculators`.

## Tools

| Tool | What it works out |
| --- | --- |
| `tax_trap_100k` | Whether income falls in the Personal Allowance taper (£100,000 to £125,140), what it costs including lost Tax-Free Childcare and funded hours, and the pension salary sacrifice that would bring income back to £100,000 |
| `student_loan_overpay` | Whether overpaying a UK student loan (Plan 1, 2, 4, 5 or Postgraduate) reduces total repayments, or only hands over money that would otherwise be written off |
| `mortgage_overpay_vs_savings` | Over the time left on a fixed-rate mortgage, overpaying compared with saving the same monthly amount, after tax and the Personal Savings Allowance |

Each tool uses UK rules for the current tax year. It returns a one-sentence summary, the figures, the assumptions used, and a link to the same result on Candid's site. All tools are read-only. Answers aren't stored.

## Connecting

Add the server URL as a remote (custom) connector in your MCP client. For example, in Claude Code:

```bash
claude mcp add --transport http candid https://www.candid-finance.co.uk/mcp
```

## About

Candid is a calculator, not an adviser. Results are guidance, not regulated financial advice, and Candid doesn't recommend products or courses of action.

The server runs on Candid's own calculation engine, which isn't open source. This repository holds the registry listing (`server.json`) and this documentation. Report problems as an issue here.
