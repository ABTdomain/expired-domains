# Expired Domains

[![10M+ expired domains tracked](https://img.shields.io/badge/expired%20domains-10M%2B-0284C7?labelColor=1F2937)](#what-makes-domainkits-different)
[![1,100+ gTLDs](https://img.shields.io/badge/gTLDs-1%2C100%2B-0284C7?labelColor=1F2937)](#what-makes-domainkits-different)
[![Stages: expired, redemption and pending delete](https://img.shields.io/badge/stages-expired%20%C2%B7%20redemption%20%C2%B7%20pending%20delete-0284C7?labelColor=1F2937)](#expired-domain-search)
[![Updated daily](https://img.shields.io/badge/refresh-daily-0284C7?labelColor=1F2937)](#what-makes-domainkits-different)
[![AI native: MCP, CLI and Skills](https://img.shields.io/badge/AI%20native-MCP%20%C2%B7%20CLI%20%C2%B7%20Skills-0284C7?labelColor=1F2937)](#mcp-server)
[![No registrant PII](https://img.shields.io/badge/PII-none-0284C7?labelColor=1F2937)](#what-makes-domainkits-different)

DomainKits tracks more than **10 million expired domains** across 1,100+ gTLDs: names in the registrar grace period, in redemption, or in the final days of pending delete. All of them are still registered, and the ones that are not renewed or restored are released in the coming weeks.

**DomainKits.com** makes finding them before they drop easier.

## What makes DomainKits different

A typical expired domain list is a pending delete file or a single auction feed. DomainKits tracks the whole expiration pipeline:

- **Every stage, not only pending delete.** Expired, Redemption and Pending Delete, each one filter away.
- **Newly Expired.** Names that entered the expired stage within roughly the past 72 hours, weeks before they reach pending delete lists.
- **1,100+ gTLDs.** `.com`, `.net`, `.org`, `.info`, `.xyz` and new gTLDs. ccTLDs are not included because country registries do not publish standardized redemption and pending delete states.
- **Pre-drop signals.** Domain age, current stage, registration date and the number of TLDs sharing the name, to judge value before you bid or backorder.
- **No registrant PII.** Focused on technical domain data, GDPR-friendly.
- **Rich access options.** Four different ways to access expired domains, built for a range of workflows.

## Let DomainKits help you find expired domains

Pick the interface that fits your workflow:

| Way | Best for | Freshness | Coverage |
|---|---|---|---|
| [**Expired domain search**](#expired-domain-search) | A keyword or TLD question you want answered now | Daily | 1,100+ gTLDs |
| [**MCP server**](#mcp-server) | LLM-assisted deep dives into expired domains | Daily | 1,100+ gTLDs |
| [**CLI**](#cli) | Integrating expired domain data into AI agent workflows | Daily | 1,100+ gTLDs |
| [**API**](#api) | Integrating expired domain data into your workflows | Daily | 1,100+ gTLDs |

### [Expired domain search](https://domainkits.com/search/expired?utm_source=github&utm_medium=hub_repo&utm_content=section_search)

Start with **Keyword** (a term across all gTLDs), **Browse by TLD** (one TLD, no keyword needed) or **Browse all** (the full pipeline), then narrow down with **10 filters** and export the results.

<p align="center">
<a href="https://www.youtube.com/watch?v=vEqW-aqvpbQ"><img src="https://img.youtube.com/vi/vEqW-aqvpbQ/maxresdefault.jpg" alt="Video: How to search expired domains with DomainKits" width="640"></a><br>
<a href="https://www.youtube.com/watch?v=vEqW-aqvpbQ">▶ Watch on YouTube: How to Search Expired Domains</a>
</p>

| Dimension | Filters |
|---|---|
| **Keyword and TLD** | **TLD** · **Position** (start, middle or end) · **Exclude keywords** |
| **Structure** | **Length** (up to 5, 5 to 20, or over 20 characters) · **Type** (letters only, numbers only, no numbers, no hyphens) |
| **Stage and age** | **Status** (expired, redemption or pending delete) · **Fresh** (newly expired) · **Age** (0 to 5, 5 to 10, 10 to 20, or 20+ years) |
| **Signals** | **TLD count** (TLDs sharing the same name) · **Registrar** |

### [MCP server](https://domainkits.com/mcp?utm_source=github&utm_medium=hub_repo&utm_content=section_mcp)

Lets AI find expired domains with [ABTdomain/domainkits-mcp](https://github.com/ABTdomain/domainkits-mcp): Claude, ChatGPT, Gemini, Cursor and other MCP clients search the same expiration pipeline as web search, by keyword or gTLD, then dig deeper in the same conversation.

- **Judge the value**: registration history, backlink profile, and search volume and CPC for the keyword
- **Map the name**: the same name across TLDs, and secondary market prices for similar names
- **Read the status**: what each EPP status code means and what the holder can still do
- **Automate the workflow**: build these steps into your own skills, or try [ABTdomain/domainkits-skills](https://github.com/ABTdomain/domainkits-skills)

### [CLI](https://github.com/ABTdomain/domainkits-cli)

Uses the DomainKits API from the command line: `dk` is one binary with no dependencies, takes `key=value` parameters, prints the API response as returned, and returns exit codes that AI agents and scripts can branch on (`0` success, `1` API error, `2` usage or network error).

```bash
export DOMAINKITS_API_KEY=dk_...
dk search expired query=shop status=pending_delete age_min=10   # pending delete names with 10+ years of history
dk search expired tld=app status=redemption export=csv          # one TLD's redemption stage as a CSV file
```

- **Install**: [ABTdomain/domainkits-cli](https://github.com/ABTdomain/domainkits-cli), or `go install github.com/ABTdomain/domainkits-cli/cmd/dk@latest`
- **Orchestrate your own AI workflow**: pick the commands you need and chain them together

### [API](https://domainkits.com/dev/api-docs?utm_source=github&utm_medium=hub_repo&utm_content=section_api)

Integrates expired domain data into your workflows: the same search with the full filter set (stage, age, TLD count, registrar, auction and found dates) as JSON, or CSV and TXT exports of up to 50,000 results, for your scripts, dashboards and drop-catching tools.

- **Python SDK**: [ABTdomain/domainkits-sdk-py](https://github.com/ABTdomain/domainkits-sdk-py)
- **Go SDK**: [ABTdomain/domainkits-sdk-go](https://github.com/ABTdomain/domainkits-sdk-go)
- **TypeScript SDK**: [ABTdomain/domainkits-sdk-js](https://github.com/ABTdomain/domainkits-sdk-js)
- **n8n node**: [ABTdomain/domainkits-n8n](https://github.com/ABTdomain/domainkits-n8n), with a ready-made template that [finds high-value expired domains and emails a CSV report](https://n8n.io/workflows/18101-find-high-value-expired-domains-with-domainkits-and-moz-and-email-a-csv-report/)
- **Node-RED nodes**: [ABTdomain/node-red-contrib-domainkits](https://github.com/ABTdomain/node-red-contrib-domainkits)

## Contact us

- Email: [info@domainkits.com](mailto:info@domainkits.com)
- Website: [domainkits.com](https://domainkits.com/?utm_source=github&utm_medium=hub_repo&utm_content=contact)
