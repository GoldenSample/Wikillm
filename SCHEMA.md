# Wiki Schema

## Domain
AI, LLMs, machine learning, knowledge synthesis, books and research papers. Building a compounding interlinked knowledge base from 500+ high-signal books.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `transformer-architecture.md`)
- Every wiki page starts with YAML frontmatter
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[raw/...]` at the end of paragraphs

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy]
sources: [raw/...]
confidence: high | medium | low
contested: true
contradictions: [other-page-slug]
---
```

## Tag Taxonomy
- Models: model, architecture, benchmark, training, inference
- People/Orgs: person, company, lab, open-source
- Techniques: optimization, fine-tuning, alignment, data, RAG
- Meta: comparison, timeline, controversy, prediction, book
- Books: book, summary, key-ideas

## Page Thresholds
- Create a page when an entity/concept appears in 2+ sources OR is central to one source
- Add to existing page when a source mentions something already covered
- Split a page when it exceeds ~200 lines
- Archive when fully superseded

## Update Policy
When new information conflicts: note both positions with dates and sources, mark `contradictions`, flag for review.
