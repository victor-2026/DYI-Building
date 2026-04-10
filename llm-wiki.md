# LLM Wiki

A pattern for building personal knowledge bases using LLMs.

## The core idea

Instead of just retrieving from raw documents at query time, the LLM **incrementally builds and maintains a persistent wiki** — a structured, interlinked collection of markdown files that sits between you and the raw sources.

## Architecture

- **Raw sources** — immutable source documents
- **The wiki** — LLM-generated markdown files
- **The schema** (AGENTS.md) — conventions and workflows

## Operations

- **Ingest** — process new sources into wiki
- **Query** — search wiki and synthesize answers
- **Lint** — health-check for contradictions, orphans, gaps