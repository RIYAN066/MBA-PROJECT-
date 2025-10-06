[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RIYAN066/MBA-PROJECT-/blob/main/analysis_notebook_colab.ipynb)

# Optimizing Quick Commerce Logistics in Kochi

**Project:** Optimizing Quick Commerce Logistics in Kochi: A Data‑Driven Supply Chain & Facility Location Model  
**Author:** Riyan Reji  
**Based on:** MBA project - Evaluating the efficiency of quick commerce logistics in Kochi and its impact on customer satisfaction.

## What this repo contains
- `notebooks/analysis_notebook.ipynb` - Jupyter notebook with step-by-step analysis (data fetch, demand estimation, facility optimization, VRP, visualizations).
- `scripts/data_fetch.py` - Functions to fetch real-world geospatial and demographic data (using OSMnx, requests) for Kochi.
- `scripts/facility_optimization.py` - MILP model (PuLP) to choose facility locations + transportation flows.
- `scripts/vrp_solver.py` - VRP example using OR-Tools (vehicle routing with time windows and capacities).
- `data/` - placeholder for any saved CSVs (created when you run the notebook).
- `requirements.txt` - Python package list to reproduce results locally.
- `README.md` - This file.

## How to run (local machine)
1. Create a Python virtual environment (Python 3.9+ recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # on mac/linux
   venv\Scripts\activate    # on Windows
   pip install -r requirements.txt
   ```
2. Start Jupyter:
   ```bash
   jupyter notebook notebooks/analysis_notebook.ipynb
   ```
3. Run the notebook cells sequentially. The notebook will fetch real geospatial data for Kochi (OSM), obtain demographic proxies, and run optimization models.
4. Review results and export visualizations. The notebook will save CSVs to the `data/` folder.

## Notes about "real data"
- The notebook uses **OpenStreetMap (OSM)** via `osmnx` to get Kochi's road graph and POIs (potential dark-store locations).
- It demonstrates how to fetch port / trade summaries from public pages (scraping example) but respects site terms — if a site blocks scraping, follow their APIs or download data manually into `data/` and rerun.
- Exact transport cost parameters, fixed opening costs, and demand estimates should be validated against company/market data. The repo uses defensible defaults and shows how to replace them with real inputs.

## Deliverables
- Facility siting recommendations (CSV & map)
- Cost breakdowns & sensitivity analysis
- Example VRP routes (Kochi zones)

## License
MIT License

---
