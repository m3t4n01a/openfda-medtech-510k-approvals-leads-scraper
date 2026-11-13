# OpenFDA MedTech 510(k) Approvals Leads Scraper

[![Run on Apify Store](https://img.shields.io/badge/Apify_Store-Run_Actor-00C853?style=for-the-badge&logo=apify)](https://apify.com/willowy_catamaran_fco/openfda-medtech-510k-approvals-scraper)

Extract newly FDA 510(k) cleared medical device companies with executive/regulatory contacts, clearance dates, verified domains, and B2B emails.

---

## 1-Click n8n Workflow Template (Ready to Import)
Import directly into **n8n** (`Workflows -> Import from URL`) using:
`https://raw.githubusercontent.com/m3t4n01a/openfda-medtech-510k-approvals-leads-scraper/main/n8n-workflow.json`

Or download [`n8n-workflow.json`](./n8n-workflow.json) from this repository.

## Claude Desktop / Cursor MCP Server Integration
Use this B2B intelligence engine directly inside Claude Desktop, Cursor, or Windsurf:
```json
{
  "mcpServers": {
    "openfda-medtech-510k-approvals-scraper": {
      "command": "npx",
      "args": [
        "-y",
        "@apify/actors-mcp-server",
        "--actors",
        "willowy_catamaran_fco/openfda-medtech-510k-approvals-scraper"
      ],
      "env": {
        "APIFY_TOKEN": "YOUR_APIFY_API_TOKEN"
      }
    }
  }
}
```

## Direct Synchronous REST API (cURL / Clay / Make)
```bash
curl -X POST "https://api.apify.com/v2/acts/willowy_catamaran_fco~openfda-medtech-510k-approvals-scraper/run-sync-get-dataset-items?token=YOUR_APIFY_API_TOKEN" \
  -H 'Content-Type: application/json' \
  -d '{"medicalSpecialty": "", "countryCode": "US", "maxItems": 25}'
```