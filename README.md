# GeoAI Change Detection

**Leveraging AI and cloud-native geospatial tools to detect land cover changes from Sentinel-2 satellite imagery.**

This project demonstrates an end-to-end GeoAI workflow:
- Querying large-scale satellite data via **STAC** (SpatioTemporal Asset Catalog)
- Efficiently accessing and processing **Cloud Optimized GeoTIFFs (COGs)** without downloading full files
- Automated feature extraction and change detection
- Interactive visualization in a lightweight web map using **Leaflet**

## 🚀 Features

- Public STAC search (Planetary Computer / AWS Earth Search)
- Lazy loading of Sentinel-2 Level-2A COGs with `rasterio` / `rioxarray`
- Simple yet effective change detection (NDVI differencing + optional ML classification)
- Interactive web map that loads specific COG bands directly in the browser
- Zero-cost hosting and execution (Google Colab + GitHub Pages)

## 🛠️ Tech Stack

- **Python**: `pystac-client`, `rasterio`, `rioxarray`, `geopandas`, `scikit-learn`
- **Visualization**: Leaflet.js + georaster-layer-for-leaflet (or Leafmap in notebooks)
- **Data**: Open Sentinel-2 L2A via public STAC catalogs
- **Environment**: Google Colab (recommended) or Binder

## 📁 Project Structuregeoai-change-detection/
├── notebooks/              # Jupyter notebooks (Colab-ready)
│   └── change_detection.ipynb
├── webmap/                 # Static web map files
│   ├── index.html
│   └── assets/
├── README.md
├── requirements.txt
└── .gitignore (optional)


## 📊 How It Works

1. **Data Access** — Search and filter Sentinel-2 scenes using STAC.
2. **Processing** — Compute spectral indices and detect changes between dates.
3. **Output** — Generate GeoJSON of changed areas + ready-to-use COG URLs.
4. **Visualization** — Load selected COGs directly into an interactive Leaflet map (partial loading via HTTP range requests).

## 🖥️ Live Demo

→ **[View Interactive Web Map](https://cazzaster.github.io/geoai-change-detection/)**

## 📓 Run the Notebook

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cazaster/geoai-change-detection/blob/main/notebooks/change_detection.ipynb)

*(The notebook link will work once you create the `notebooks/change_detection.ipynb` file)*

## Getting Started

1. Clone the repo or open directly in Google Colab
2. Install dependencies: `pip install -r requirements.txt`
3. Run the notebook to query STAC and generate change maps
4. View the interactive web map via GitHub Pages

## Future Enhancements

- Deep learning models for semantic segmentation
- Multi-temporal analysis and before/after sliders
- Automated report generation

---

**Built as a professional portfolio project to showcase scalable GeoAI workflows using open data and cloud-optimized tools.**

Made with ❤️ for geospatial innovation.

