# Susceptible landslide areas detection

##Description
The Susceptible landslide area model was developed to obtain an information layer that contributes to AI Climate Platform, a land management instrument and decision-making tool geared to Global South secondary/tertiary cities that lack local data and whose objective is to cut the time and expense involved in climate hazard mapping, assessment, and prediction, freeing up city resources for community resilience (adaptation) building.

As inputs, the model uses: (I) a raster dataset from optical satellites that represent conditioning factors (topographic and environmental) that can facilitate landslide occurrence, (II)georeferenced information (ground truth) of landslides past events.

DEM, slope, topographic wet index (TWI), land use and land cover (LULC), NDVI (impervious surface) map, distance to rivers and roads, lithological map, and a soil map are the conditioning factors used in the input dataset. The selection of these factors has depended on the area of interest characteristics and the availability of the data.

## Requirements 

The tools **GDAL** y [Orfeo Toolbox](https://www.orfeo-toolbox.org/) are used in the first stage, the pre-processing of the data. In the following stages, our packages [satproc](https://github.com/dymaxionlabs/satproc) and [unetseg](https://github.com/dymaxionlabs/satproc) are used for dataset generation and for training and prediction process.

## Notebooks

This repository has a Jupyter Notebooks set, which describes the necessary steps:

1. [Training](notebooks/1_Entrenamiento.ipynb): Satellite imagery and ground truth are processed to generate the training dataset. Then, the model is trained and evaluated.
2. [Prediction](notebooks/2_Prediccion.ipynb): Prediction over the area of interest and prediction results processing.

## :handshake: Contributions

Bugs reports y *pull requests* could be done in the [issues page](https://github.com/dymaxionlabs/adefinir) of this repository. 

## :page_facing_up: License

The code is licensed under Apache 2.0. Refer to [LICENSE.txt](LICENSE.txt).
