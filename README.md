# Quantum Internship Task 4 - Soil Erosion Detection on Sentinel2 Tile

* The main goal of this task is to train model for erosion detection

## Solution Report


According to [1], soil erosion is a very serious environmental problem. Studies (for example [1], [2]) have shown that the utility of the remote sensing method has great potential for detecting eroded areas and monitoring erosion processes in a regional area.
Satellite image processing (such as Sentinel2 [3]) can give a lot of useful information. Of course, with the development of deep learning methods came the possibility of effective segmentation of such images using convolutional neural networks [3].


Input files:
* Sentinel2 tile (T36UXV_20200406T083559_TCI_10m.jp2);
* Masks with soil erosion for this tile (masks directory);

Steps taken in ```Task4_Data_Analysis.ipynb```:

* Read input Sentinel2 tile and masks with usage of rasterio and geopandas
* Convert CRS(Coordinate Reference System) of masks with soil erosion for this tile by finding EPSG correct for area on input tile
* Create binary mask (soil_erosion/ not_soil_erosion) for whole input tile
* Image and mask split into small segments 256x256 pixels


Inspiring by [4] it was decided to try to detect erosion places on input file with the usage of U-Net Convolutional Neural Network taken from [5].






[1] Lukyanchuk, K. A., I. P. Kovalchuk, and O. M. Pidkova. "Application of a remote sensing in monitoring of erosion processes." Geoinformatics: Theoretical and Applied Aspects 2020. Vol. 2020. No. 1. European Association of Geoscientists & Engineers, 2020.

[2] Lu, D., et al. "Mapping and monitoring land degradation risks in the Western Brazilian Amazon using multitemporal Landsat TM/ETM+ images." Land Degradation & Development 18.1 (2007): 41-54.

[3] Fazzini, Paolo, et al. "Sentinel-2 Remote Sensed Image Classification with Patchwise Trained ConvNets for Grassland Habitat Discrimination." Remote Sensing 13.12 (2021): 2276.

[4] Samarin, Maxim, et al. "Identifying soil erosion processes in alpine grasslands on aerial imagery with a u-net convolutional neural network." Remote Sensing 12.24 (2020): 4149.

[5] https://www.depends-on-the-definition.com/unet-keras-segmenting-images/

[6] Fang, W. A. N. G., et al. "Aerial-BiSeNet: A real-time semantic segmentation network for high resolution aerial imagery." Chinese Journal of Aeronautics 34.9 (2021): 47-59.
