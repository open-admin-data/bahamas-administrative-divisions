# Bahamas Administrative Divisions / The Bahamas



## Overview

| Item | Details |
|------|---------|
| District | 32 |
| Locality | 349 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-07-07 |
| Website | [openadmindata.org/bs](https://openadmindata.org/bs/) |
| API | [openadmindata.org/api/bs](https://openadmindata.org/api/bs/) |

## Browse by District

| # | District | Localitys | Link |
|---|----|----|------|
| 1 | Acklins | 17 | [Browse](divisions/acklins-bs-ak/) |
| 2 | Berry Islands | 2 | [Browse](divisions/berry-islands-bs-br/) |
| 3 | Biminis | 7 | [Browse](divisions/biminis-bs-bi/) |
| 4 | Black Point | 2 | [Browse](divisions/black-point-bs-bp/) |
| 5 | Cat Island | 33 | [Browse](divisions/cat-island-bs-ci/) |
| 6 | Central Abaco | 6 | [Browse](divisions/central-abaco-bs-cb/) |
| 7 | Central Andros | 6 | [Browse](divisions/central-andros-bs-cn/) |
| 8 | Central Eleuthera | 9 | [Browse](divisions/central-eleuthera-bs-ce/) |
| 9 | City of Freeport | 14 | [Browse](divisions/city-of-freeport-bs-fp/) |
| 10 | Crooked Island | 13 | [Browse](divisions/crooked-island-bs-ck/) |
| 11 | East Grand Bahama | 5 | [Browse](divisions/east-grand-bahama-bs-eb/) |
| 12 | Exuma | 27 | [Browse](divisions/exuma-bs-em/) |
| 13 | Grand Cay | 0 | [Browse](divisions/grand-cay-bs-gc/) |
| 14 | Harbour Island | 1 | [Browse](divisions/harbour-island-bs-hb/) |
| 15 | Hope Town | 6 | [Browse](divisions/hope-town-bs-ht/) |
| 16 | Inagua | 1 | [Browse](divisions/inagua-bs-in/) |
| 17 | Long Island | 46 | [Browse](divisions/long-island-bs-li/) |
| 18 | Mangrove Cay | 5 | [Browse](divisions/mangrove-cay-bs-mc/) |
| 19 | Mayaguana | 3 | [Browse](divisions/mayaguana-bs-mg/) |
| 20 | Moore&#39;s Island | 2 | [Browse](divisions/moore-s-island-bs-mi/) |
| 21 | New Providence | 31 | [Browse](divisions/new-providence-bs-nw/) |
| 22 | North Abaco | 12 | [Browse](divisions/north-abaco-bs-nb/) |
| 23 | North Andros | 22 | [Browse](divisions/north-andros-bs-nn/) |
| 24 | North Eleuthera | 9 | [Browse](divisions/north-eleuthera-bs-ne/) |
| 25 | Ragged Island | 1 | [Browse](divisions/ragged-island-bs-ri/) |
| 26 | Rum Cay | 4 | [Browse](divisions/rum-cay-bs-rc/) |
| 27 | San Salvador | 24 | [Browse](divisions/san-salvador-bs-ss/) |
| 28 | South Abaco | 4 | [Browse](divisions/south-abaco-bs-sb/) |
| 29 | South Andros | 10 | [Browse](divisions/south-andros-bs-sn/) |
| 30 | South Eleuthera | 14 | [Browse](divisions/south-eleuthera-bs-se/) |
| 31 | Spanish Wells | 1 | [Browse](divisions/spanish-wells-bs-sw/) |
| 32 | West Grand Bahama | 12 | [Browse](divisions/west-grand-bahama-bs-wb/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-district.json](data/all-district.json) | JSON | All 32 district records |
| [all-locality.json](data/all-locality.json) | JSON | All 349 locality records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-district.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['locality']} localitys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-district.json", "utf-8"));
console.log(`Total: ${data.length} districts`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=district, 2=locality |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{district-slug}/
```

Localitys are listed inline in each district's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-district links
- [Per-district data](docs/llms-full/) — Full data by district

## Citation

```
Bahamas Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/bahamas-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
