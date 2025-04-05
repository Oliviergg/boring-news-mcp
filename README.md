# Boring News MCP Client

A Python client library for interacting with the Boring News API using Mission Control Protocol (MCP).

## Installation

```bash
pip install boring-news-mcp
```

## Features

- Fetch articles by date, category, or tags
- Get articles mentioning specific people
- Find similar articles based on text content
- Get article groups and categories
- Generate various types of news summaries:
  - Daily news (tech and culture focused)
  - Comprehensive daily summaries
  - News highlights
  - Cultural news focus

## Quick Start

```python
from boring_news_mcp import get_articles_by_date, daily_news_summary

# Get today's articles
articles = await get_articles_by_date()
print(articles)

# Get a comprehensive news summary for a specific date
summary = await daily_news_summary("2024-04-05")
print(summary)
```

## API Reference

### Articles

- `get_articles_by_date(date: Optional[str], category: Optional[str], tags: Optional[str]) -> str`
- `get_articles_by_person(person: str) -> str`
- `get_similar_articles(text: str) -> str`
- `get_article_groups(date: Optional[str]) -> str`
- `get_categories(date: Optional[str]) -> str`

### News Summaries

- `daily_news(target_date: str) -> str`
- `daily_news_summary(target_date: str) -> str`
- `daily_news_highlights(target_date: str) -> str`
- `daily_cultural_news(target_date: str) -> str`

## Requirements

- Python >= 3.8
- httpx >= 0.25.0
- fastmcp >= 0.1.0

## License

MIT License
