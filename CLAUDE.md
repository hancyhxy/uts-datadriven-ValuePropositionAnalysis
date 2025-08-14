# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Bitcoin Value Proposition Analysis** academic research project that uses data-driven narrative mapping to analyze Bitcoin's value proposition through six structured segments. The project creates interactive web-based visualizations to present comprehensive research on Bitcoin's emergence, adoption, and future potential.

## Architecture & Data Structure

### Core Data Schema
The project centers around `bitcoin_narrative_data_mapping.json`, which contains a structured narrative with:

- **6 narrative segments**: Introduction → Mystery → Maintainers → Price Journey → Winners → Future
- **Each segment contains**:
  - `key_questions`: Research questions driving the narrative
  - `required_data`: Specific data types and metrics needed
  - `data_sources`: APIs and data sources with access methods
  - `visualization_suggestions`: Recommended chart types and visual presentations

### Cross-Segment Requirements
- **Time Series Alignment**: All time-based data must use consistent timestamps for narrative flow
- **Data Quality Metrics**: Source credibility and reliability scoring system
- **Technical Requirements**: JSON/CSV/API format support with daily price updates, weekly metric updates

### Web Interface Architecture
- **Self-contained HTML files**: No build process required - all CSS and JavaScript embedded
- **Bilingual support**: Built-in Chinese/English switching using `data-en` and `data-zh` attributes
- **Interactive components**: Expandable table rows, smooth scrolling navigation, responsive design
- **No external dependencies**: Pure HTML/CSS/JavaScript implementation

## Key Operations

### Viewing the Project
```bash
# Open main project page
open index.html

# Open specific language versions
open bitcoin_narrative_table_en.html  # English only
open bitcoin_narrative_table.html     # Chinese only
```

### Data Structure Updates
When modifying `bitcoin_narrative_data_mapping.json`:
- Maintain the 6-segment structure with consistent `segment_id` numbering
- Ensure each segment has all required fields: `title`, `narrative_text`, `key_questions`, `required_data`, `data_sources`, `visualization_suggestions`
- Keep data source URLs accessible and verify access methods
- Update corresponding HTML table content to reflect JSON changes

### HTML Modifications
- Language content uses dual attributes: `data-en="English text" data-zh="中文文本"`
- Interactive table rows use `data-segment` attributes for JavaScript targeting
- CSS classes follow BEM-like naming: `.segment-row`, `.details-row`, `.sub-table`
- Badge styling indicates counts: `.badge`, `.badge.success`, `.badge.warning`, `.badge.danger`

### Language Support
- Language switching preserves user preference in localStorage
- All user-facing text should have both `data-en` and `data-zh` attributes
- Navigation and interactive elements are fully bilingual
- Default language is English (`lang="en"`)

## File Relationships

- **`index.html`**: Main project homepage with full feature integration, navigation, and project context
- **`bitcoin_narrative_data_mapping.json`**: Core data structure - source of truth for all narrative content
- **`bitcoin_narrative_table_en.html`**: English-only table version (legacy)
- **`bitcoin_narrative_table.html`**: Chinese-only table version (legacy)
- **Academic support files**: `How to Create an Effective Value Proposition.md`, `narrotive.md` provide research context

## Data Integrity Requirements

### JSON Schema Consistency
- Each narrative segment must include all required fields
- Data source URLs should be functional and current
- Visualization suggestions should be implementable with standard charting libraries
- Cross-segment data needs must address temporal alignment and quality metrics

### Ethical Considerations
The project incorporates specific ethical guidelines:
- Privacy protection for individual Bitcoin addresses
- Balanced representation of risks and benefits
- Transparent disclosure of data sources and limitations

## Academic Context

This project applies Clayton Christensen's "jobs to be done" theory to Bitcoin value proposition analysis, using structured narrative mapping to understand how Bitcoin addresses specific user needs and market opportunities. The data-driven approach ensures research conclusions are supported by verifiable metrics and credible sources.