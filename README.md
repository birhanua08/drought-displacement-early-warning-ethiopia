# Climate Stress and Drought-Attributed Internal Displacement in Ethiopia

Python and geospatial analysis workflow examining the geographic concentration of
drought-attributed internal displacement in Ethiopia and its relationship with
rainfall stress, pastoral livelihood systems, livestock mobility corridors, and
conflict exposure.

## Related Manuscript
**Climate Stress and Drought-Attributed Internal Displacement in Ethiopia:  
Woreda-Scale Rainfall Anomalies, Zone-Level Patterns, and an Early-Warning Framework**  
Author: Birhanu A. Teka

## Purpose
This repository supports:
- Processing CHIRPS rainfall data into seasonal totals, anomalies, and drought indicators.
- Aggregating IOM DTM displacement records to woreda and zone levels.
- Examining the spatial concentration of drought-attributed displacement.
- Overlaying rainfall stress with pastoral livelihood zones, livestock corridors,
  and conflict-event context.
- Generating maps and monitoring products for anticipatory action and
  conflict-sensitive early warning.

## Data Sources
- **Displacement:** IOM Displacement Tracking Matrix (DTM) Site Assessment Round 35.
- **Climate:** CHIRPS v2.0 monthly rainfall data.
- **Conflict context:** ACLED event-level data.
- **Livelihood exposure:** FEWS NET Ethiopia livelihood zones.
- **Mobility corridors:** SPARC/ILRI livestock-route mapping and participatory mapping.

## Analytical Workflow
1. Download and preprocess CHIRPS monthly rainfall tiles.
2. Calculate Kiremt seasonal rainfall totals and long-term averages.
3. Compute rainfall anomalies in millimetres, percent of normal, and standardized forms.
4. Calculate SPI-3 and SPI-6 indicators where applicable.
5. Aggregate drought-attributed IDP counts to woreda and zone levels.
6. Spatially join climate, displacement, conflict, livelihood, and corridor layers.
7. Produce maps of rainfall anomalies, displacement burden, and high-priority zones.
8. Generate descriptive outputs for anticipatory action and peace-responsive early warning.

## Key Output
The analysis identifies high-burden pastoral and agro-pastoral zones where drought stress,
constrained livestock mobility, resource competition, and conflict risk intersect. It does
not estimate causal effects; it provides a geographic and associative evidence base for
anticipatory action and conflict-sensitive programming.

## Technologies
- Python
- Pandas
- GeoPandas
- Rasterio
- xarray
- Matplotlib
- Folium / Leaflet
- PostGIS
- Jupyter Notebook

## Repository Structure
```text
├── README.md
├── requirements.txt
├── data/
│   ├── raw/                  # Not included if restricted or very large
│   └── sample/
├── notebooks/
│   └── 01_drought_displacement_analysis.ipynb
├── src/
│   ├── 01_download_chirps.py
│   ├── 02_process_rainfall.py
│   ├── 03_calculate_anomalies.py
│   ├── 04_aggregate_displacement.py
│   ├── 05_spatial_joins.py
│   ├── 06_maps_and_figures.py
│   └── 07_early_warning_indicators.py
├── outputs/
│   ├── figures/
│   └── tables/
└── .gitignore
```

## How to Run
```bash
pip install -r requirements.txt
```

Run the Jupyter notebook or execute the scripts in the `src/` folder.

## Ethical and Data Notes
This repository uses open data sources. Displacement data reflect accessible sites assessed
by IOM DTM and are not a full census. The analysis is associative and cross-sectional; it
does not claim that climate alone causes displacement.# drought-displacement-early-warning-ethiopia
