# RemoteOK Scraper

Scrape RemoteOK — the world's largest remote job board. Filter by skill, location restriction, or company. Includes salary range, full description, and direct apply URL.

**[RemoteOK Scraper - Remote Job Listings on Apify →](https://apify.com/blackfalcondata/remoteok-scraper?fpr=1h3gvi)**

---

## Key features





**Incremental mode** — Only get new or changed listings since your last run. Content hash per listing — no duplicates, no re-processing.

**Compact output** — Emit core fields only (AI-agent / MCP-friendly). Keeps response size small for LLM workflows.

**Description truncation** — Cap description length per listing to control output size and cost.

**Result cap** — Stop after N listings (up to 200). Set to 0 for the full catalog.

**Export anywhere** — Download as JSON, CSV, or Excel. Stream via Apify API, webhooks, or integrations with Make, Zapier, Airbyte, Keboola.

**Structured data** — Every listing returns the same schema with consistent field naming. All fields always present — `null` when unavailable, never omitted.

---

## Use cases





**Data pipeline automation**
Integrate with your ETL pipeline to collect structured listings from remoteok.com on a schedule. Export to CSV, JSON, or directly to your database. Use compact mode to control output size.

**Market research**
Monitor listings, track trends, and analyze market dynamics with structured, deduplicated data from remoteok.com.

**Change monitoring**
Run daily or hourly in incremental mode to capture only new, updated, or expired listings. Perfect for price-tracking, churn analysis, and alerting pipelines.

**Compensation benchmarking**
Aggregate salary ranges across roles, industries, and locations on remoteok.com to inform pricing decisions, hiring plans, or candidate negotiations.

**AI / LLM training data**
Structured JSON per listing is ready for RAG pipelines, embeddings, and agent workflows. Compact mode trims tokens for LLM context windows.

---

## Quick start

```json
{
  "tag": "javascript",
  "maxResults": 10
}
```

---

## Input parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `tag` | string | — | Filter by skill or technology tag, e.g. "javascript", "python", "devops", "react". Leave blank for all recent remote jobs. |
| `location` | string | — | Filter jobs by geographic restriction, e.g. "usa", "europe", "worldwide". Note: many remote jobs have no location restriction. |
| `company` | string | — | Filter jobs by company name, e.g. "github", "stripe". Leave blank for all companies. |
| `maxResults` | integer | `25` | Maximum number of jobs to return (0 = all available, up to ~96 most recent). |
| `descriptionMaxLength` | integer | `0` | Truncate job description HTML to N characters. 0 = no truncation. |
| `compact` | boolean | `false` | Return core fields only (jobId, title, company, location, tags, salaryText, applyUrl, url, postedDate). Ideal for AI-agent and MCP workflows. |

---

## FAQ

<!-- WRITE: 4-6 Q&A pairs relevant to this product -->

**How does incremental mode work?**
Each listing gets a content hash. On subsequent runs, only new or changed listings are emitted — saving time, compute, and storage.

---

## Known limitations

<!-- WRITE: 4-6 honest limitations -->

- <!-- WRITE: limitation 1 -->
- <!-- WRITE: limitation 2 -->


## Output fields

Every listing returns the same 17-field schema. Missing values are `null` — never omitted.

- `jobId`
- `title`
- `company`
- `location`
- `tags`
- `salaryMin`
- `salaryMax`
- `salaryText`
- `description`
- `applyUrl`
- `url`
- `logoUrl`
- `postedDate`
- `isVerified`
- `portalUrl`
- `scrapedAt`
- `source`


## Sample output

One object per listing. Here is a real example from a production run:

```json
{
  "jobId": "4274f4404f33f186012fc73e4638177227a39c6390eed0785f56d1b3530d3bf5",
  "title": "Clinician Experience Specialist",
  "company": "Nabla",
  "location": "New York City",
  "tags": [
    "support",
    "software",
    "travel",
    "assistant",
    "financial",
    "video",
    "senior",
    "operations",
    "excel",
    "health",
    "healthcare",
    "engineering",
    "recruitment",
    "educational"
  ],
  "salaryMin": 75000,
  "salaryMax": 100000,
  "salaryText": "$75,000 – 

**[Try RemoteOK Scraper - Remote Job Listings now — $5 free credit, no credit card →](https://apify.com/blackfalcondata/remoteok-scraper?fpr=1h3gvi)**


## Pricing

Pay only for what you extract. No subscription required — Apify's free $5 credit covers thousands of results.

| Event | Price (USD) |
| --- | --- |
| Actor Start | $0.005 |
| Result | $0.001 |

See the [actor on Apify](https://apify.com/blackfalcondata/remoteok-scraper?fpr=1h3gvi) for current pricing.

---

## Related products by Black Falcon Data





00,000",
  "description": "<h2><strong>About Nabla</strong></h2><p style=\"min-height:1.5em\">We are a team of entrepreneurs, clinicians and engineers committed to bringing back joy to the practice of medicine…",
  "applyUrl": "https://remoteOK.com/remote-jobs/remote-clinician-experience-specialist-nabla-1130917",
  "url": "https://remoteOK.com/remote-jobs/remote-clinician-experience-specialist-nabla-1130917",
  "logoUrl": null
}
```

*Truncated — full records contain 17 fields. See Output fields for the complete schema.*

---

## Related products by Black Falcon Data





- [StepStone Scraper](https://apify.com/blackfalcondata/stepstone-scraper?fpr=1h3gvi) — Job listings from 18 European portals
- [Indeed Job Scraper](https://apify.com/blackfalcondata/indeed-job-scraper?fpr=1h3gvi) — Indeed job listings with salary data
- [Glassdoor Job Scraper](https://apify.com/blackfalcondata/glassdoor-job-scraper?fpr=1h3gvi) — Glassdoor listings with company ratings
- [Arbeitsagentur Scraper](https://apify.com/blackfalcondata/arbeitsagentur-scraper?fpr=1h3gvi) — Germany's official job portal (1M+ listings)
- [SEEK Scraper](https://apify.com/blackfalcondata/seek-scraper?fpr=1h3gvi) — Australia & NZ's largest job board
- [Naukri Scraper](https://apify.com/blackfalcondata/naukri-scraper?fpr=1h3gvi) — India's largest job portal


## Getting started with Apify

New to Apify? [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=1h3gvi) — no credit card required.

1. [Sign up free](https://console.apify.com/sign-up?fpr=1h3gvi) — $5 credit included
2. Open the actor and paste your input
3. Click Start — results download as JSON, CSV, or Excel

Need more volume? [See pricing](https://apify.com/pricing?fpr=1h3gvi).

---


## About Black Falcon Data

Black Falcon Data builds production-grade web scrapers for job boards and marketplace data. Browse our full actor catalog at [www.blackfalcondata.com](https://www.blackfalcondata.com).

---
---

*Last updated: 2026 03*
