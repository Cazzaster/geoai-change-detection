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

## 📁 Project Structure
geoai-change-detection/

├── notebooks/              # Jupyter notebooks (Colab-ready)

│   └── change_detection.ipynb

├── webmap/                 # Static web map files

│   ├── index.html

│   └── assets/

├── README.md

└── requirements.txt

