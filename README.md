# Geospatial Data Science with Python

Notebooks for the YouTube course — from reading a spatial file to building and
honestly validating a spatial machine learning model.

Every notebook runs in **Google Colab** with no installation: click the badge,
run the first cell, and the data downloads itself.

---

## Series 1 — Spatial Data in Python

| # | Notebook | Video | Run it |
|---|---|---|---|
| 01 | **Introduction to GeoPandas** — the geometry column, CRS, projecting to metres, file formats, your first map | [watch](https://youtu.be/FvdJasgymRE) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/reza-geospatial/geospatial-data-science-python/blob/main/01_SpatialData/S1_01_GeoPandas.ipynb) |
| 02 | **Coordinate reference systems** — reading a CRS, `set_crs` vs `to_crs`, mismatched joins, why Web Mercator lies, buffering in degrees | [watch](https://youtu.be/VIDEO_ID) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/reza-geospatial/geospatial-data-science-python/blob/main/02_CRS/S1_02_CRS.ipynb) |
| 03 | **Spatial joins, buffers and overlays** — `sjoin` and its predicates, buffer, overlay, dissolve, and counting the rows every join loses | [watch](https://youtu.be/VIDEO_ID) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/reza-geospatial/geospatial-data-science-python/blob/main/03_SpatialJoins/S1_03_SpatialJoins.ipynb) |

More episodes are published here as each video goes live.

**Coming next**

- Series 1 — nearest neighbour and geocoding · classification and basemaps · getting real data from OSM, WFS and PostGIS
- Series 2 — Spatial Statistics That Actually Matter
- Series 3 — Spatial Machine Learning Done Right

▶ [Course playlist](https://www.youtube.com/playlist?list=PLAYLIST_ID)

---

## The dataset

One dataset runs through the whole course, so each episode builds on the last:
**Unfallatlas 2018** — 13,652 georeferenced road accidents in Berlin, plus 7,413
street segments and the city's administrative boundaries.

See [`data/SOURCES.md`](data/SOURCES.md) for the full attribution and licences.

---

## Running locally

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Each notebook finds `data/` on its own.

## Licence

Code: [MIT](LICENSE). Data: see [`data/SOURCES.md`](data/SOURCES.md) — the
accident data is published under *Datenlizenz Deutschland – Namensnennung 2.0*
and must be attributed wherever it is reused.
