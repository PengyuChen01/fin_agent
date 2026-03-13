# Fin Agent

A financial intelligence agent that provides market analysis and next-day outlook using free LLM models.

## Overview

Fin Agent is an automated financial analysis tool that runs at key market moments (open, mid-session, close) to deliver actionable market insights. It leverages free LLM models (e.g. DeepSeek) combined with web scraping tools to aggregate analyst opinions and international geopolitical developments.

## Features

- **Scheduled Market Briefings** - Automated reports at market open, mid-session, and close
- **Next-Day Outlook** - Generates predictions and key factors for the next trading day
- **Web Intelligence** - Scrapes and summarizes analyst reports, news, and geopolitical events
- **Free LLM Backend** - Powered by DeepSeek (or other free models) to keep costs at zero
- **Geopolitical Awareness** - Monitors international developments that may impact markets

## Architecture

```
┌─────────────┐     ┌──────────────┐     ┌─────────────┐
│  Scheduler   │────▶│  Fin Agent   │────▶│   Output    │
│ (open/mid/   │     │  (DeepSeek)  │     │ (Terminal/  │
│  close)      │     │              │     │  Notify)    │
└─────────────┘     └──────┬───────┘     └─────────────┘
                           │
                    ┌──────┴───────┐
                    │  Web Tools   │
                    │  - News API  │
                    │  - Analyst   │
                    │    Reports   │
                    │  - Geopolitics│
                    └──────────────┘
```

## Planned Tech Stack

- **LLM**: DeepSeek API (free tier)
- **Language**: Python
- **Scheduler**: APScheduler / cron
- **Web Tools**: requests + BeautifulSoup / Tavily API
- **Data Sources**: Financial news sites, analyst platforms, geopolitical feeds

## Roadmap

- [ ] Project scaffolding & config setup
- [ ] DeepSeek API integration
- [ ] Web scraping tools (news, analyst reports, geopolitical events)
- [ ] Prompt engineering for market analysis
- [ ] Scheduler for open / mid-session / close triggers
- [ ] Output formatting & notification (terminal / messaging)
- [ ] Backtesting & accuracy tracking

## Getting Started

```bash
# Clone
git clone git@github.com:PengyuChen01/fin_agent.git
cd fin_agent

# Install dependencies (coming soon)
pip install -r requirements.txt

# Configure API keys
cp .env.example .env
# Edit .env with your DeepSeek API key

# Run
python main.py
```

## License

MIT
