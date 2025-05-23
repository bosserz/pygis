# pygis
Compilation of Pythonic alternatives for GIS tasks.

# Core Geospatial Data Handling
## Vector Data
### Reading/Writing:
- Reading various vector formats (Shapefile, GeoJSON, KML, GPKG, etc.)
- Writing to various vector formats
### Attribute Table Operations:
- Selecting/filtering rows (by attribute, by location)
- Adding/deleting/modifying columns
- Calculating new attribute values (e.g., area, perimeter, length)
- Joining tables (one-to-one, one-to-many, spatial joins)
### Geometric Operations:
- Creation: Creating points, lines, polygons from coordinates or WKT/WKB
### Manipulation:
- Buffering (fixed distance, variable distance)
- Dissolving (by attribute, all features)
- Intersecting
- Unioning
- Clipping/Masking
- Symmetric Difference
- Difference
- Convex Hull
- Simplification (e.g., Ramer-Douglas-Peucker)
- Centroids, points on surface
- Bounding boxes/envelopes
### Measurements:
- Area, Perimeter, Length
- Distance between geometries
### Coordinate System Transformations:
- Reprojecting vector layers
## Raster Data
### Reading/Writing:
- Reading various raster formats (GeoTIFF, NetCDF, HDF, etc.)
- Writing to GeoTIFF
### Basic Raster Operations:
- Clipping/Masking rasters
- Resampling (nearest neighbor, bilinear, cubic)
- Reclassifying raster values
- Mosaic/Merging rasters
- Calculating basic statistics (min, max, mean, std dev)
- Converting raster to vector (polygonizing)
- Converting vector to raster (rasterizing)
### Raster Algebra/Map Algebra:
- Performing arithmetic operations (+, -, *, /) on rasters
- Conditional statements (e.g., where operations)
### Coordinate System Transformations:
- Reprojecting raster layers

# Geospatial Analysis & Processing
## Proximity Analysis
- Buffer Analysis: Creating buffers around points, lines, and polygons.
- Distance Analysis: Calculating distance to nearest features.
- Cost Path/Least Cost Path: (More advanced, often involving scipy or networkx)
- Thiessen Polygons/Voronoi Diagrams: Creating areas of influence.
## Overlay Analysis
- Intersects, Union, Difference, Symmetric Difference: For vector layers.
- Clip, Erase: For vector layers.
## Spatial Joins
- Point in Polygon: Assigning attributes from polygons to points.
- Intersection Join: Joining attributes based on overlapping geometries.
- Nearest Neighbor Join: Joining attributes based on proximity.
## Zonal Statistics
- Calculating statistics (mean, sum, min, max, count, etc.) of a raster within defined zones (polygons).
## Surface Analysis (DEMs)
- Hillshade: Generating hillshade from DEM.
- Slope: Calculating slope from DEM (degrees or percent).
- Aspect: Calculating aspect from DEM.
- Contour Generation: Creating contour lines from DEM.
- Viewshed Analysis: (More complex, often requires custom implementation or specific libraries)
## Network Analysis (More advanced, often with networkx or dedicated libraries)
- Shortest Path
- Service Area (Isocrone)
- Closest Facility
## Geocoding & Reverse Geocoding
- Using APIs (e.g., OpenStreetMap Nominatim, Google Geocoding API) to convert addresses to coordinates and vice-versa.
## Interpolation
- IDW (Inverse Distance Weighting): Simple interpolation.
- Kriging: More advanced geostatistical interpolation (requires scipy or pykrige).
## Remote Sensing
- Spectral Indices: Calculating NDVI, NDWI, EVI, etc., from multi-band imagery.
- Image Classification (Unsupervised/Supervised): (Often involves scikit-learn, scikit-image, spectral)
  - K-Means clustering for unsupervised.
  - Random Forest, SVM for supervised.
- Change Detection: Comparing multi-temporal images.

# Data Visualization
## Static Maps:
- Using matplotlib and geopandas for basic mapping.
- Adding basemaps (e.g., contextily).
- Thematic mapping (choropleth, proportional symbols).
## Interactive Maps:
- Using folium for web-based interactive maps (Leaflet).
- Using ipyleaflet or pydeck for Jupyter-integrated interactive maps.
- Basic layer toggling, popups, tooltips.

# Utilities & Helper Functions
## Coordinate Conversion: Lat/Lon to UTM, etc.
- CRS Handling: Detecting, defining, and transforming Coordinate Reference Systems.
- Data Validation: Checking geometry validity.
- Data Cleaning: Handling null geometries, repairing invalid geometries.
- Batch Processing: Examples of iterating through multiple files or features.
Command Line Interface (CLI) tools: Simple scripts that can be run from the terminal.
Project Structure & Best Practices
README.md: Clear explanation of the repo's purpose, how to use it, and dependencies.
Jupyter Notebooks: For each use case, have a clear, runnable Jupyter notebook demonstrating the code.
Python Scripts: Convert notebooks into reusable Python scripts where appropriate.
requirements.txt: List all necessary Python packages.
Data Folder: A small data folder with sample datasets (or links to larger datasets) to make examples runnable.
Docstrings and Comments: Explain your code clearly.
Testing (Optional but Recommended): Basic unit tests for critical functions.
