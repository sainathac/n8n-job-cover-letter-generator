# n8n-job-cover-letter-generator

n8n workflow that reads job postings from RSS feeds, extracts skills, and generates personalized cover letters using Gemini AI.

## What It Does

Monitors job RSS feeds daily, uses Gemini AI to extract required technical skills from each posting, generates a tailored cover letter, and appends everything to a Google Sheet for easy review.

## Workflow

```
Schedule Trigger -> RSS Read -> Basic LLM Chain -> Append row in sheet
```

## Prerequisites

- **n8n** instance (self-hosted or cloud)
- **Google account** with OAuth2 configured in n8n
- **Google Gemini API** access (via AI Gateway in n8n)
- A Google Sheet named 'N8N Linkedin auto' with columns: Title, Link, Published Date, Skill, CV, About Company & Job Description

## Setup

1. **Import the workflow:** Open your n8n instance, go to **Workflows > Import from File**, and select `workflow.json`
2. **Configure credentials:**
   - Set up Google Sheets OAuth2
   - Set up Gmail OAuth2
   - Set up Google Gemini (Palm) API credentials
   - Link your target Google Sheet for appending results
3. **Update placeholders:**
   - Replace any hardcoded email addresses with your own
   - Replace any Google Sheet IDs with your own sheets
   - Update the RSS feed URL if you want different job sources
- Update the Google Sheet document ID
4. **Activate the workflow** and let it run!

## Author

**sainathac** — [GitHub](https://github.com/sainathac)

## License

MIT
