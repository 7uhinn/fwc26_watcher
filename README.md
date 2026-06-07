# FIFA World Cup 2026 — Live Dashboard

A single-file HTML dashboard for following the 2026 FIFA World Cup, built for a Bengaluru viewer (IST, UTC+5:30).

## Features

- **All 104 matches** — group stage through the final, with approximate kickoff times
- **Live scores** — fetched from the ESPN public API every 60 seconds during live matches
- **12 group tables** — real-time standings with W/D/L/GD/Pts, color-coded by qualification status
- **Third-place leaderboard** — all 12 third-place teams ranked; top 8 advance
- **Dynamic knockout bracket** — R32 through Final; slots fill from current group standings even before matches are played
- **Match schedule** — all matches sorted by date, with full-card highlights for recommended watches
- **IST watchability** — every match rated by time window (Prime / Late / Graveyard / Morning / Afternoon)
- **Importance scoring** — 1–5 stars based on team quality, match stakes, rivalry, and upset potential, with bonus weight for preferred teams
- **Country flags** — via flagcdn.com

## Viewing

Open `worldcup2026.html` directly in any modern browser. No server, build step, or dependencies needed.

Designed for a **1920×1080** display. The layout scales down to fit smaller viewports automatically.

## Preferred teams

**Must watch:** Portugal · Brazil · Germany · Spain · France · Argentina · England

**Good watch:** Morocco · Japan · Netherlands · Norway · Belgium · Uruguay · Croatia

## Data

Match schedule and bracket structure are hardcoded from the official FIFA 2026 fixture list. Live scores are pulled from the ESPN free API (`site.api.espn.com`) — no API key required.

## Constraints

- Single file, no build tools, no npm, no frameworks
- No localStorage or sessionStorage
- External resources: country flags from [flagcdn.com](https://flagcdn.com) only
