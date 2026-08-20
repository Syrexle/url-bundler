# Ledger Line

Bundle several block-explorer transaction links into one shareable link.

Built for reconciling payouts that span multiple swaps — epoch rewards, incentive claims, batches of transactions — into a single row in a spreadsheet. Instead of pasting six links into one cell, generate one link that expands into the full list when opened.

**Live:** https://url-bundler.vercel.app

## How it works

- Add a line per transaction (optional label + URL), or paste a block of URLs at once.
- Click **Generate bundle link** to get one URL.
- Opening that link decodes the list client-side and shows every transaction, individually clickable, with an **Open all in new tabs** button.

There is no backend and no accounts. The data is base64-encoded directly into the URL fragment (`#...`), so nothing is stored on a server — the link itself is the database.

## Stack

Single static `index.html`. No build step, no dependencies. Deployed to Vercel.

## Development

```bash
vercel deploy --prod
```
