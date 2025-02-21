# Crop Classification with Multi-Temporal Satellite Imagery

This repo provides codes for crop classification using multi temporal satellite images. Crop classification is important for understanding the supplies of a crop. The satellite images can be helpful in monitoring crop growth and health in near real-time. Today, high-resolution satellite images are available at a daily frequency. With high-frequency data and multiple bands, it's possible to classify crops using deep learning.

There are many classical machine learning crop classification approaches available which use mono-temporal images and use the spectral and textural properties of a crop which results in relatively low accuracy but we’ll use the method suggested by **Rose M. Rustowicz** author of the [paper](http://cs229.stanford.edu/proj2017/final-reports/5243811.pdf)

![alt text](https://github.com/bhavesh907/Crop-Classification/blob/master/cover1.png "cover")

# Installation

```
conda create --name geo_py37 python=3.7
conda install gdal rasterio
conda install numpy pandas geopandas scikit-learn jupyterlab matplotlib seaborn xarray rasterstats tqdm pytest sqlalchemy scikit-image scipy pysal beautifulsoup4 boto3 cython statsmodels future graphviz pylint line_profiler nodejs sphinx

```

# Dataset
You can download the dataset used in this repo from [Gdrive](https://drive.google.com/drive/folders/1go32yGsEoLkYQi48qVQoG7shDuTgfjf4?usp=sharing)

The dataset consists of 10 RapidEye satellite images provided by the [planet.com](https://www.planet.com/) and 1 USDA Cropland data layer which provides the pixel level crop labels. 

# Usage
1. Run the data-preprocessing.ipynb to prepare the dataset for our models.
2. To classify the crops based on NDVI index, run NDVI_based.ipynb
3. Train the DL model using the script Crop_classification_DL_model.ipynb