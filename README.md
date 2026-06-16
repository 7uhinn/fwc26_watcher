# FIFA World Cup 2026 — Live Dashboard

A single-file HTML dashboard for following the 2026 FIFA World Cup, built for an Indian viewer (IST, UTC+5:30).

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
- **Match popup** — click any match card for a detailed view with three tabs:
  - **Lineups** — pitch-view formation with jersey chips, player ratings (position-aware), MOTM star, manager name, team average rating
  - **Incidents** — timeline of goals, assists, cards, and substitutions
  - **Match Facts** — split-bar team stats using each team's kit colours (home kit for home, away kit for away)
- **Player stats popup** — click any player chip (starter or sub) for a full breakdown: jersey, position, rating, and every ESPN stat grouped into Attacking / Defence / Discipline / General
- **Player ratings** — computed from ESPN stats weighted by position (GK/Def/Mid/Fwd), with result-context bonus/penalty
- **Man of the Match** — single best-rated player across both teams, shown only after full time

## Viewing

Open `index.html` directly in any modern browser. No server, build step, or dependencies needed.

Designed for a **1920×1080** display. The layout scales down to fit smaller viewports automatically.

## Preferred teams

**Must watch:** Portugal · Brazil · Germany · Spain · France · Argentina · England

**Good watch:** Morocco · Japan · Netherlands · Norway · Belgium · Uruguay · Croatia

## Data

Match schedule and bracket structure are hardcoded from the official FIFA 2026 fixture list. Live scores are pulled from the ESPN free API (`site.api.espn.com`) — no API key required. Lineups, stats, and incidents are fetched from the ESPN match summary endpoint on demand.

All 48 team managers are hardcoded from official FIFA sources.

Team codes follow ESPN's abbreviations throughout (e.g. Saudi Arabia is `KSA`, matching ESPN rather than the FIFA code `SAU`), so live data maps directly without a translation layer.

## Constraints

- Single file, no build tools, no npm, no frameworks
- No localStorage or sessionStorage
- File size under 200 KB
- External resources: country flags from [flagcdn.com](https://flagcdn.com) only
