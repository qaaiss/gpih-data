# Market data feed

Daily raw-material market snapshot in JSON, published once a day.

- `payloads/latest.json` — the most recent snapshot
- `payloads/archive/YYYY-MM-DD.json` — one file per day

## Format (schema_version 1.0)

| Key | Content |
|---|---|
| `prices` | Market price observations — each with `source`, `source_url` and `observed_on` |
| `drivers` | Futures / feedstock / energy values — each with source and date |
| `fx` | Exchange rates with source and date |
| `events` | Market events (price announcements, outages, duties, capacity) with source and date |
| `analyses` | AI interpretation — not market data; each lists its evidence URLs |
| `forecasts` | Low / base / high price ranges with target date, confidence and method |

All facts come from public sources and link back to them.
