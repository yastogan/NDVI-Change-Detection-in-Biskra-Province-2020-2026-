
# NDVI Change Detection Analysis (2020–2026)

## Overview

This project evaluates vegetation dynamics across **Biskra Province, Algeria**, by comparing **Normalized Difference Vegetation Index (NDVI)** values derived from Sentinel-2 imagery between **2020** and **2026**.

The objective is to identify areas where vegetation has significantly increased, decreased, or remained relatively stable over the six-year period using Google Earth Engine, GDAL, and QGIS.

---

## Methodology

The workflow consisted of the following steps:

1. Acquisition of cloud-free Sentinel-2 Level-2A imagery for 2020 and 2026.
2. NDVI computation using the standard formula:

[
NDVI = \frac{NIR - Red}{NIR + Red}
]

3. Export of 10 m NDVI rasters from Google Earth Engine.
4. Clipping datasets to the administrative boundary of Biskra Province.
5. Projection to an Equal-Area coordinate system (EPSG:6933) to ensure accurate area calculations.
6. Pixel-wise subtraction:

> NDVI Change = NDVI 2026 − NDVI 2020

7. Classification of change into five categories.

---

## NDVI Change Classification

| Class               | NDVI Difference | Interpretation                 |
| ------------------- | --------------- | ------------------------------ |
| Strong decrease     | < -0.10         | Significant vegetation loss    |
| Moderate decrease   | -0.10 to -0.03  | Slight vegetation decline      |
| Stable / Low change | -0.03 to 0.03   | Little or no detectable change |
| Moderate increase   | 0.03 to 0.10    | Moderate vegetation recovery   |
| Strong increase     | > 0.10          | Significant vegetation gain    |

---

# Results

The spatial analysis indicates that vegetation conditions in Biskra remained largely stable during the study period.

Most pixels fall within the **Stable / Low Change** category, indicating that vegetation patterns experienced only minor fluctuations between 2020 and 2026.

Localized zones of vegetation gain are concentrated primarily in:

* irrigated agricultural areas,
* oasis systems,
* cultivated land,
* seasonal vegetation corridors.

Vegetation decline appears as scattered patches and is generally associated with:

* urban expansion,
* land degradation,
* agricultural abandonment,
* natural seasonal variability.

No extensive province-wide vegetation degradation was detected.

---

# Area Statistics

| Change Class        | Area (km²) |
| ------------------- | ---------: |
| Strong decrease     |      73.41 |
| Moderate decrease   |     275.75 |
| Stable / Low change |   7,689.82 |
| Moderate increase   |     540.51 |
| Strong increase     |     218.45 |

---

# Interpretation

Approximately **87.8%** of the analyzed area remained stable over the six-year period, demonstrating that vegetation conditions across Biskra were generally consistent.

Areas showing vegetation improvement exceed areas experiencing vegetation decline, suggesting localized agricultural expansion and improved vegetation productivity in several irrigated zones.

The strongest vegetation gains are mainly observed around cultivated lands and oasis environments, whereas vegetation losses remain limited in extent and spatially fragmented.

Overall, the results indicate that no major regional-scale vegetation degradation occurred during the study period.

---

# Software & Data

**Satellite Data**

* Sentinel-2 Level-2A
* Google Earth Engine

**Software**

* Google Earth Engine
* QGIS
* GDAL

**Spatial Resolution**

* 10 m

**Projection**

* WGS 84 / UTM Zone 31N (EPSG:32631)
* Equal-Area Projection (EPSG:6933) used for area statistics

---

# Project Outputs

The repository contains:

```
maps/
├── 01_NDVI_Spatial_Distribution_Biskra_2020.png
├── 02_NDVI_Spatial_Distribution_Biskra_2026.png
└── NDVI_Change_Detection_Biskra_2020_2026.png
```

---

# Key Findings

* Six-year NDVI change assessment for Biskra Province.
* Pixel-based change detection at 10 m spatial resolution.
* Equal-area analysis for accurate area estimation.
* More vegetation gain than vegetation loss.
* Stable vegetation dominates the province.
* Workflow developed using Google Earth Engine, GDAL, and QGIS.
* Results can support environmental monitoring, land management, and sustainable agricultural planning.
