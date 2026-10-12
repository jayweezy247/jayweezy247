# Jordan White

**AI marketing engineer.** Twelve years running paid search and marketing for lead-generation businesses, starting inside Google's agency program, then Chief Revenue Officer and Chief Data & Technology Officer at a lead-gen agency. Now I build the AI software marketing teams need, mostly by directing Claude Code and checking what it ships against the live system.

Portland, OR · [didm.ai](https://didm.ai) · [LinkedIn](https://www.linkedin.com/in/jordan-white-pdx)

## What I build

Most of this lives in private client and company repos. Here is what's in them.

**A CRM for service businesses, with AI built in** (pre-launch, 360+ merged pull requests in its first 20 days)
- Multi-tenant on Cloudflare Workers and Postgres, with row-level security and a test that proves one client can never read another's data.
- A Claude assistant that answers questions about contacts, deals and leads, and drafts changes that a person approves before anything is written.
- Claude lead scoring on call and form transcripts; consent, opt-out and quiet hours stored as data, not checkboxes.
- Voice AI for inbound calls. I ran a bake-off of four voice providers and put them behind one provider-neutral layer, so when a vendor shut down, switching was a config change.
- Industry packs: law practices (matters, conflict checks, engagement agreements signed from a link), pool construction and service, and more.

**A marketing data stack**
- Google Ads, GA4 and call-tracking leads unified in BigQuery and ClickHouse, with spend reconciled against the live Google Ads API.
- Scheduled pipelines on Google Cloud Run for court dockets, Census and labor data, property records, permits, weather and search trends.
- An agent that audits GA4 setups and fixes them behind human approval, then checks weekly for drift.

**Agent systems**
- A 23-agent system for a school, running around the clock on Google Cloud, with one identity per agent, approval gates and a spend cap.
- MCP servers that let AI agents work inside Google Ads, GA4, Tag Manager and call tracking: dry-run by default, every write logged. One is public below.
- A Claude Code plugin of specialist agents (implementer, verifier, security, data) with hooks that block unsafe commits and require evidence before a fix is delegated.

## Public work

- [**tracking-stack-mcp**](https://github.com/jayweezy247/tracking-stack-mcp): an MCP server for setting up GA4, Google Tag Manager and WhatConverts, behind a create-only, dry-run-by-default write contract with an append-only action log.

## How I work

- Every write an agent makes is previewed first and logged. Nothing risky runs without a person saying yes.
- Decisions get written down where the next session will read them, and every failure becomes a test or a guard.
- I measure the live system, not what the code says it does.

**Tools I use daily:** Claude Code, the Anthropic API, MCP, TypeScript, Python, SQL, Cloudflare Workers, Postgres, BigQuery, ClickHouse, Google Cloud Run, GA4, Google Tag Manager, Google Ads API, Zapier.
