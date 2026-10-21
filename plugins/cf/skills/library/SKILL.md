---
name: library
description: Answer questions from the Crawling Fortunes knowledge base (the cf-kb connector), which holds the company's own docs about Pivvy (product rules, numbers, decisions, user journeys, brand, roadmap) plus the founders' startup, product and marketing books (traction, cold start, growth, marketing, product-market fit). Use whenever the user asks anything about Pivvy or Crawling Fortunes, a product decision or rule, or what the books say about a startup, product or marketing topic. Search the library before answering from memory, past chats or project files.
---

# Crawling Fortunes library

The cf-kb connector is the source of truth for Pivvy and Crawling Fortunes, and for the founders' books. Memory, past chats and project files can be stale or incomplete, so search the library first.

## Steps

1. Call `search_library` before answering. Use `collection: "company"` for Pivvy and Crawling Fortunes questions, `"books"` for advice and "what do the books say" questions, and `"all"` when both apply.
2. For broad or synthesis questions, search several times with different phrasings. Use `list_documents` and `doc_ids` to target specific documents. Use `get_passage` when a hit is cut off.
3. Answer from the results. Where the library and memory or past chats disagree, the library wins, and say that you are using the library's version.
4. Cite company docs with their Drive link, and books as (Title, chapter, pages).
5. Never call something undecided or unknown until the library has been searched. If the library has nothing relevant, say so plainly and label anything else as general knowledge.
6. If the cf-kb tools are unavailable or return an error, tell the user the library could not be reached instead of answering from memory as if it had been checked.
