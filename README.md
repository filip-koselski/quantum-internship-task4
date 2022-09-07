# Quantum Internship Task 4 - Soil Erosion Detection on Sentinel2 Tile

* The main goal of this task is to train model for erosion detection

Input files:
* Sentinel2 tile (T36UXV_20200406T083559_TCI_10m.jp2);
* Masks with soil erosion for this tile (masks directory);

Report:
* Read input Sentinel2 tile and masks with usage of rasterio and geopandas
* Convert CRS(Coordinate Reference System) of masks with soil erosion for this tile by finding EPSG correct for area on input tile
* Create binary mask (soil_erosion/ not_soil_erosion) for whole input tile
* Image and mask split into small segments 256x256 pixels
* 
