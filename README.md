# Manhattan Project Portfolio · INOVUES

Interactive Mapbox visualization of INOVUES' active NYC-metro deal portfolio.

## What it shows

- **13 active deals** across the NYC metro area, geocoded to lat/lng
- **Sized by deal value** — flagship ($5M+), major ($1M+), mid ($100K+), early
- **Pipeline stage progress** for each deal (8-stage funnel)
- **Mockup status** flagged on relevant deals
- **433K ft² total glass area · $14.6M pipeline value**

## Stack

- Mapbox GL JS v3.6.0 (dark style, 3D buildings)
- Plain HTML/CSS/JS — no build step
- GeoJSON data layer (`deals.geojson`)
- Inter + JetBrains Mono typography
- Pentagram annual-report visual language (inherited from `viz-steel.vercel.app`)

## Files

| File | Purpose |
|------|---------|
| `index.html` | Full app (UI + map + popup logic) |
| `deals.geojson` | Deal data — edit to add/remove projects |
| `stats.json` | Aggregate portfolio metrics |

## Updating deals

Edit `deals.geojson`. Each feature has `coordinates: [lng, lat]` and `properties` with `name`, `stage`, `sf`, `amount`, etc.

To regenerate from the HubSpot CSV export, see the geocoding pipeline in the original build conversation.

## Deploy

Pushes to `main` auto-deploy via Vercel.
