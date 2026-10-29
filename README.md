# Etymon Tracer — V1

An etymology tracing dashboard built on Webster's Revised Unabridged Dictionary (1913, public domain).

- **Word mode** — definitions, word-form breakdown (prefix · stem · suffix), and the recorded etymology.
- **Root mode** — search an etymological root or stem and list the words built on it.
- **Stem Census** (`stem-census/`) — ranks classical stems by how many Webster's headwords are confirmed to use them. V1 shows the top and bottom five; the full ranked list comes later.

## Files

| Path | Contents |
|---|---|
| `index.html` | Etymon Tracer dashboard |
| `stem-census/index.html` | Stem Census summary page |
| `dict/*.json` | Dictionary entries sharded by first letter |
| `etym.json` | Etymology index |
| `words.json` | Headword list |

## Running it

The page loads its data with `fetch`, so serve the folder rather than opening the file directly:

```
python3 -m http.server 8000
```

Then open http://localhost:8000. It also works on GitHub Pages (Settings → Pages → deploy from `main`).

The optional "trace further with Claude" panel only works inside the claude.ai-hosted version; everywhere else it stays hidden and the rest of the dashboard works normally.

## Source

*Webster's Revised Unabridged Dictionary* (1913), Project Gutenberg eBook #29765. Public domain.

Author: Keith Rawls
