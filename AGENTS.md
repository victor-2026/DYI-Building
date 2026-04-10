# DYI Building Schema

## Overview
Personal knowledge base for DIY building project. Pattern from karpathy/llm-wiki.

## Directory Structure
```
/
├── raw/              # Immutable source documents
│   └── sources/      # Articles, papers, notes
├── wiki/              # LLM-generated markdown files
│   ├── index.md      # Catalog of all wiki pages
│   ├── log.md        # Chronological activity log
│   └── pages        # Entity, concept, summary pages
└── AGENTS.md         # This schema
```

## Conventions
- Source documents are NEVER modified by LLM
- LLM owns wiki layer entirely
- Index updated on every ingest
- Log entries use format: `## [YYYY-MM-DD] type | Title`

## Operations

### Ingest
1. Drop source into `raw/sources/`
2. LLM reads source, extracts key info
3. LLM creates/updates wiki pages
4. LLM updates `index.md` and `log.md`

### Query
1. LLM reads `index.md` for relevant pages
2. LLM drills into relevant pages
3. LLM synthesizes answer with citations
4. Valuable answers filed back into wiki

### Lint
Periodically check for:
- Contradictions between pages
- Stale claims superseded by new sources
- Orphan pages with no inbound links
- Missing cross-references
- Data gaps fillable with web search

## Page Types
- **Summary**: Overview of a source or topic
- **Entity**: Person, place, concept
- **Comparison**: Side-by-side analysis
- **Synthesis**: Multi-source synthesis