# SpringBrand MCP Guide: GTM Tools for Claude Code, Codex and Cursor

A short guide to connecting your AI agent to [SpringBrand](https://springbrand.ai/), an MCP capability layer that gives agents like Claude Code, Codex and Cursor access to 10,000+ APIs and plugins for go-to-market work: SEO, ads, social media, lead generation, e-commerce and customer support.

Keep the agent you already use. SpringBrand adds the tools it is missing.

## What is SpringBrand?

SpringBrand is a shared layer of APIs and plugins for AI agents. You describe a task, and your agent searches the SpringBrand catalog, picks the operations that fit, runs them and reads the results in the same conversation.

- **One account, 10,000+ APIs and plugins.** No separate keys or integrations for each provider.
- **500+ GTM scenarios** across ads and SEO, social media, creative content, e-commerce, sales and CRM, and customer support.
- **Pay per call.** One shared credit balance and one bill, with calls starting at $0.03.
- **Works through MCP**, so any MCP-capable agent host can use it.

## Install the SpringBrand MCP server

The SpringBrand MCP server ships inside the SpringBrand plugin. Paste this into your agent to install or update it:

```
Install or update SpringBrand: https://plugin.springbrand.ai/INSTALL.md
```

Then sign in. Command-line hosts use:

```bash
# Claude Code CLI
claude mcp login plugin:springbrand:springbrand

# Codex CLI
codex mcp login springbrand
```

Desktop hosts show the sign-in prompt in their plugin settings. Step-by-step guides for each host are in the [SpringBrand installation guide](https://springbrand.ai/developers/docs/installation).

## SpringBrand MCP tools

The server follows a discover-then-run pattern. Discovery and schema lookups never execute anything, so an agent can explore safely before it runs a task.

| Tool | What it does |
|---|---|
| `search_tools` | Find operations that match a task description |
| `get_tool_schemas` | Read an operation's input and output contract |
| `execute_tools` | Run one or more operations |
| `get_execution` | Read the status and saved result of a run |
| `manage_connections` | List and connect the third-party accounts an operation needs |

Full reference: [SpringBrand MCP server docs](https://springbrand.ai/developers/mcp).

## What you can ask your agent

Once SpringBrand is connected, plain-language requests like these work in Claude Code, Codex or Cursor.

**SEO and ads**
- Find competitor keywords my site misses
- Compare cost per lead across Google and Meta
- Pause keywords that spent over $100 with no leads

**Social media and creators**
- Find beauty creators with 20K–100K followers
- Show my best-performing posts from the last 30 days

**Creative content**
- Create five UGC video ad concepts for my product launch
- Turn a product photo into a 15-second video ad

**E-commerce**
- Compare my pricing against three competitors
- Draft product descriptions for a new SKU launch

**Sales and CRM**
- Find deals that haven't moved forward in two weeks
- Add new leads from my inbox to the CRM

**Customer support**
- Summarize customer complaints from the last 7 days

More ready-made agents by job: [competitor analysis](https://springbrand.ai/agents/competitor-analysis), [lead generation](https://springbrand.ai/automate/lead-generation), [Shopify stores](https://springbrand.ai/agents/shopify) and the full [AI agents directory](https://springbrand.ai/agents).

## APIs your agent can reach

Google, Google Maps, TikTok, Instagram, YouTube, X, Reddit, RedNote, Facebook, Semrush, Ahrefs, Firecrawl, Apify, Apollo, Lusha, HubSpot, Salesforce, Shopify, Amazon, Stripe, ElevenLabs and thousands more. Browse them in the [SpringBrand marketplace](https://springbrand.ai/integrations).

## Skills vs MCP

An agent skill is a folder with a `SKILL.md` file: instructions the agent reads. An MCP server is a running program that gives the agent tools to call. They work best together: a skill tells the agent how to approach a task, and the SpringBrand MCP server gives it the tools to finish it. See [agent skills for Claude Code and OpenClaw](https://springbrand.ai/skills).

## FAQ

**Which agents work with SpringBrand?**
Any agent host that supports MCP. Guides are maintained for Claude Code, Codex, Cursor and WorkBuddy.

**Do I need an API key?**
No. The MCP server signs in with OAuth in your browser. Some operations ask you to connect a third-party account the first time you use them.

**Do I need to code?**
Not with SpringBrand Agent, where you describe tasks in everyday language. Connecting your own agent takes a small amount of MCP setup.

**How is it priced?**
A credit balance covers API and plugin usage. Plans include monthly credits, and you can start with free credits. See [SpringBrand pricing](https://springbrand.ai/pricing).

**How do I update it?**
Paste the install prompt again. The plugin and its bundled MCP server update together.

## Links

- Website: https://springbrand.ai/
- Docs: https://springbrand.ai/developers/docs
- X: https://x.com/Springbrand_ai
- Discord: https://discord.gg/cBSexyn4P
