# Boring News MCP Server
[![smithery badge](https://smithery.ai/badge/@Oliviergg/boring-news-mcp)](https://smithery.ai/server/@Oliviergg/boring-news-mcp)

A Python server library for interacting with the Boring News API from a MCP (Model Context Protocol) server like Claude Desktop


## Features
four actions : 
- Fetch articles by date, category, or tags
- Get articles mentioning specific people
- Find similar articles based on text content
- Get article groups and categories

- Predefined Prompts
  - Daily news (tech and culture focused)
  - Comprehensive daily summaries
  - News highlights
  - Cultural news focus

## Quick Start

### Installing via Smithery

To install boring-news-mcp for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@Oliviergg/boring-news-mcp):

```bash
npx -y @smithery/cli install @Oliviergg/boring-news-mcp --client claude
```

### Manual Installation
```bash
pip install boring-news-mcp
```

### Exemple of claude Desktop Configuration
```json
{
  "mcpServers": {
    ...      
    "boringnews": {
          "command": "python",
          "args": [
                "-m", 
                "boring_news_mcp"
          ]
      },
    ...
    }
}
```

## API Reference

### Articles

- `get_articles_by_date(date: Optional[str], category: Optional[str], tags: Optional[str]) -> str`
- `get_articles_by_person(person: str) -> str`
- `get_similar_articles(text: str) -> str`
- `get_article_groups(date: Optional[str]) -> str`
- `get_categories(date: Optional[str]) -> str`

### News Summaries Prompt

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
