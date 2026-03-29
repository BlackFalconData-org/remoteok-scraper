# RemoteOK Scraper

Scrape RemoteOK — the world's largest remote job board. Filter by skill, location restriction, or company. Includes salary range, full description, and direct apply URL.

**[Run on Apify →](https://apify.com/blackfalcondata/remoteok-scraper)**

---

## Key features

⚡ **Compact output for AI agents**

Core-fields-only mode optimized for MCP and AI agent workflows. Description truncation to control output size.

📊 **Structured data**

Clean JSON output with consistent field naming. All fields always present — null when unavailable, never omitted.

---

## Use cases

**Data pipeline automation**
Integrate with your ETL pipeline to collect structured listings from the source on a schedule. Export to CSV, JSON, or directly to your database.

**Market research**
Monitor listings, track trends, and analyze market dynamics with structured, deduplicated data from the source.

**AI and LLM workflows**
Use compact mode and description truncation to feed data into AI agents, MCP servers, and LLM pipelines without exceeding token budgets.

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

---

## Related products by Black Falcon Data

| Product | Description |
|:--------|:------------|
| [StepStone Jobs API](https://github.com/BlackFalconData-org/stepstone-jobs-api) | Job listings from 18 European portals |
| [Company Jobs Tracker](https://github.com/BlackFalconData-org/company-jobs-tracker-api) | Track new/removed jobs per company |
| [Indeed Jobs Feed](https://github.com/BlackFalconData-org/indeed-jobs-feed) | Indeed job listings with salary data |
| [Glassdoor Jobs Feed](https://github.com/BlackFalconData-org/glassdoor-jobs-feed) | Glassdoor listings with company ratings |
| [Arbeitsagentur Jobs Feed](https://github.com/BlackFalconData-org/arbeitsagentur-jobs-feed) | Germany's federal job portal (1M+ listings) |
| [Naukri Jobs Feed](https://github.com/BlackFalconData-org/naukri-jobs-feed) | India's largest job portal |
| [Bilbasen Scraper](https://github.com/BlackFalconData-org/bilbasen-scraper) | Denmark's largest car marketplace |

---

*Last updated: 2026 03*
