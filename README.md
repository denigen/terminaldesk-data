# terminaldesk-data

Public JSON store for [NY Desk](https://github.com/denigen/terminaldesk).

The SPA fetches these at runtime (no redeploy for morning updates):

```
https://raw.githubusercontent.com/denigen/terminaldesk-data/main/latest.json
```

## Files

- `latest.json` — today’s package (preferred)
- `YYYY-MM-DD.json` — archive days
- `index.json` — `{ "latest": "latest.json", "days": [...] }`
- `SAMPLE-*.json` — demo packages

## Writers

After each weekday BTC/FX brief, publish a `DeskDay` package here (`schemaVersion: 1`). Never invent levels. Prefer `chartUrl` as a data URL or absolute https link.
