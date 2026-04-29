# Givaudan Peer Competitive Intelligence Dashboard

This project builds a local SEC EDGAR-powered dashboard for:

- International Flavors & Fragrances (IFF)
- Sensient Technologies (SXT)
- Estée Lauder (EL)
- Coty (COTY)
- Inter Parfums (IPAR)
- Bath & Body Works (BBWI)

## Run

```bash
python3 scripts/fetch_sec_data.py
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.

## Data

The dataset in `data/sec_company_fundamentals.json` is generated from the SEC EDGAR companyfacts API using latest annual 10-K facts. The subtitle uses `metadata.prepared_by` and `metadata.school`.

## Dashboard Features

- Executive snapshot with peer revenue, average growth, average margin, and fiscal-year coverage
- Sector filters for fragrance, ingredients, prestige beauty, and consumer fragrance peers
- Key takeaways strip for highest margin, fastest growth, largest revenue, and most leveraged company
- Color-coded KPI table and five chart views, including a strategic quadrant scatter plot
- Company deep dives with peer rank, best metric, watch item, SEC EDGAR source link, and radar chart
- CSV export for KPIs and PNG export for the strategic quadrant chart
- Methodology section explaining KPI definitions and SEC source assumptions
- Linked company selection across the table, charts, scatter plot, and deep-dive panel
- 2-3 peer compare tray with KPI deltas, latest-year and 3-year trend modes, sortable/searchable table, URL state, and analyst notes
