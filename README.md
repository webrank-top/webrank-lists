# webrank lists

The downloadable lists of [**webrank**](https://webrank.top) — the open domain popularity +
authority rank, a free alternative to Tranco. No key, no signup, CC-BY 4.0.

## Files

| file | what | cadence |
|---|---|---|
| `webrank-latest.csv.gz` | top 1M domains, rolling | updated daily |
| `webrank-YYYY-MM.csv.gz` | frozen monthly snapshot (15th) | permanent, citable |

Columns: `rank, domain, webrank_score, pagerank`
- **`rank`** — popularity rank, 1 = most popular (driven by real user traffic).
- **`webrank_score`** — the same popularity on a friendly 0–10 log scale.
- **`pagerank`** — 0–10 link authority (PageRank-style): how much the web links to it.

Git history of `webrank-latest.csv.gz` gives you every daily version for free;
the monthly snapshots never change once frozen — cite those.

## Direct downloads (no GitHub needed)

```bash
curl -O https://api.webrank.top/list/webrank-latest.csv.gz
curl -O https://api.webrank.top/list/webrank-2026-07.csv.gz   # a citable snapshot
```

Per-domain lookups (JSON, batch, history): https://api.webrank.top — e.g.
`curl https://api.webrank.top/rank/google.com`. Python: `pip install webrank`
([webrank-python](https://github.com/webrank-top/webrank-python)).

## Method

The rank is a data-driven composite of eight public sources (Tranco, Chrome/CrUX,
Cisco Umbrella, Cloudflare Radar, Majestic, Open PageRank, host.io, Common Crawl),
with source weights **derived from agreement with real-traffic data** — not guessed,
not equal. It predicts real user traffic ~46% better than an equal-weighted list.
Full method + validation numbers: <https://webrank.top/methodology>.

## License & citation

Data: [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free for any use,
attribute "webrank.top". Suggested citation:

> webrank list webrank-YYYY-MM, https://webrank.top (retrieved YYYY-MM-DD).

Contact: peter@webrank.top
