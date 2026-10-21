---
name: ingest
description: Sync new or edited documents from the Crawling Fortunes Google Drive folder into the knowledge base right now, instead of waiting for the hourly sync. Use when the user asks to ingest, sync or refresh the library, or says they just added or changed a document, book or doc in the Drive folder. Do not run it otherwise.
---

# Ingest new documents

1. Call the cf-kb `ingest_library` tool. It waits up to about 40 seconds.
2. If it says the ingest is still running, call `ingest_status` about every 20 seconds until it finishes. A batch of new books takes about a minute each.
3. Tell the user in plain words which documents were added, updated or removed, and mention any failures or skipped files. Say so if nothing changed.
4. If the cf-kb tools are unavailable or return an error, say the library could not be reached. Do not guess what was ingested.
