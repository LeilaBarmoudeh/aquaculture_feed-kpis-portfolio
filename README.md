# aquaculture_feed-kpis-portfolio
Aquaculture Feeding Optimization Dashboard – using Python and power point(Synthetic Demo).

*Goal* Turn aquaculture data into clear KPIs and a one-page slide:
*FCR (7-day avg)*, *Feed waste (7d, t)*, *Biomass growth (7d, t)*,
plus key charts (FCR trend, waste vs. current, forecast vs. actual biomass).

 **Data are synthetic** for portfolio purposes. No real farm or confidential data.

# What’s in the repository
- *Python scripts* to generate data, compute KPIs, and export charts.
- *PowerPoint one-pager* (`ppt/Aquafeed_KPIs_OnePager.pptx`) assembled from the charts.
- *Images* folder with standalone PNG charts for quick viewing.
## Quick start
```bash
git clone https://github.com/<user>/aquafeed-kpis-portfolio.git
cd aquafeed-kpis-portfolio
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 1) (Re)generate synthetic data
python src/generate_data.py --out data/synthetic_feed_sample.csv --seed 42

# 2) Compute KPIs and save to console/CSV
python src/compute_kpis.py --data data/synthetic_feed_sample.csv

# 3) Export charts (PNGs) used in the slide
python src/make_charts.py --data data/synthetic_feed_sample.csv --out images/

