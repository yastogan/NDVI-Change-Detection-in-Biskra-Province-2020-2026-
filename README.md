# NDVI-Change-Detection-in-Biskra-Province-2020-2026-
Project Overview

This project analyzes vegetation dynamics in Biskra Province, Algeria, by comparing Normalized Difference Vegetation Index (NDVI) values between 2020 and 2026 using Sentinel-2 imagery. The objective is to identify areas that experienced vegetation improvement, degradation, or remained stable over the six-year period.

The analysis was performed using Google Earth Engine for image preprocessing and NDVI calculation, followed by QGIS and GDAL for spatial analysis, raster processing, visualization, and cartographic production.

Objectives
Generate NDVI maps for 2020 and 2026.
Detect vegetation changes between both years.
Classify NDVI change into five meaningful categories.
Quantify vegetation change across the province.
Produce professional cartographic outputs suitable for environmental monitoring.
Data Sources
Dataset	Source
Sentinel-2 MSI Level-2A	Copernicus Programme
Administrative Boundary	GADM / Open GIS Data
Software
Google Earth Engine
QGIS
GDAL
Methodology
1. Image Preparation

Sentinel-2 cloud-free composites were generated for both study years using Google Earth Engine.

2. NDVI Calculation

NDVI was calculated using the standard equation:

NDVI = (NIR − Red) / (NIR + Red)

where:

NIR = Band 8
Red = Band 4
3. Change Detection

Vegetation change was calculated by subtracting the 2020 NDVI from the 2026 NDVI:

NDVI Change = NDVI₍₂₀₂₆₎ − NDVI₍₂₀₂₀₎

Positive values indicate vegetation improvement, while negative values indicate vegetation loss.

4. Classification

The change raster was classified into five categories:

Class	Description
1	Strong decrease
2	Moderate decrease
3	Stable / Low change
4	Moderate increase
5	Strong increase
5. Area Calculation

The classified raster was reprojected to an Equal Area projection (EPSG:6933) to ensure accurate area estimation before calculating the spatial extent of each class.

Results

The analysis shows that vegetation remained largely stable across Biskra Province between 2020 and 2026.

Approximately 76.90 km² (about 89.5% of the valid study area) experienced little or no detectable change in vegetation condition.

Vegetation improvement was identified over approximately 7.59 km², representing areas where agricultural expansion, irrigation, or natural vegetation recovery may have occurred.

Conversely, approximately 3.49 km² showed vegetation decline, suggesting localized degradation that may be associated with land-use changes, drought stress, or reduced vegetation cover.

The spatial distribution of change indicates that vegetation dynamics are concentrated mainly within agricultural zones and oasis systems, while large desert areas remained relatively unchanged throughout the study period.

Overall, the results indicate that vegetation conditions in Biskra Province remained generally stable during the 2020–2026 period, with localized areas of both improvement and degradation.

Area Statistics
Change Category	Area (km²)
Strong decrease	0.73
Moderate decrease	2.76
Stable / Low change	76.90
Moderate increase	5.41
Strong increase	2.18
Maps Produced
01_NDVI_Spatial_Distribution_Biskra_2020.png
02_NDVI_Spatial_Distribution_Biskra_2026.png
NDVI_Change_2020_2026.png
Skills Demonstrated
Remote Sensing
Vegetation Monitoring
NDVI Analysis
Change Detection
Raster Processing
Spatial Analysis
Google Earth Engine
QGIS
GDAL
Cartographic Design
GIS Data Visualization
