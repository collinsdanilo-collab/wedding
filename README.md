# Wedding Venue Comparison Tracker

A running system for comparing wedding venues by cost and unique offerings as we collect PDFs, quotes, and email responses from each location.

## How this works

1. **Drop source material in `venues/`.** Save each venue's PDF/quote/email thread as its own file (or folder) under `venues/`, named for the venue, e.g. `venues/oak-hill-farm.md` or `venues/oak-hill-farm-quote.pdf`. Raw text pasted from an email is fine too — just save it as a `.md` or `.txt` file so it's in the repo.
2. **Ask Claude to process it.** Point Claude at the new file (or paste the content directly) and it will:
   - Confirm the venue name and source document
   - Extract all pricing data, flagging anything missing or unclear
   - Note standout offerings vs. venues already logged
   - Update `COMPARISON.md`
3. **`COMPARISON.md` is the single source of truth** — master cost table, venue-by-venue highlights, and the running list of open questions to send back to venues.

## Status

No venue documents have been processed yet. See the "Setup questions" section at the top of `COMPARISON.md` — a few answers there will let cost comparisons be normalized consistently (per-person vs. flat totals, guest count, etc.) as venues are added.
