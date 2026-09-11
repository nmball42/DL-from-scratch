# End-to-end GeoAI with TorchGeo

Last updated: Sep 11th 2026

Using a segmentation neural network to detect objects in satellite raster data is now a fairly common GeoAI use case, and can be done in a broad-brush sense with no-code or low-code tools. Finer-grained control of the model, data, and processing is often still desirable for real end-to-end analyses, however. The TorchGeo tool builds upon PyTorch and PyTorch Lightning to enable end-to-end GeoAI for a wide range of use cases. We show how plain PyTorch code is augmented by Lightning’s data and model modules, then in turn by TorchGeo’s geospatial functionality. This lets us run end-to-end building detection as an example, and control the details. ([Blogpost](https://nickballdatascience.com/end-to-end-geoai-with-torchgeo/))

## Disclaimer

This is a personal project built as part of my transition from generalist data scientist to specializing in geospatial data science, GIS, and GeoAI. The aim is for this project to be shareable, but it is not designed for production use.

## Requirements

- Machine that can run Conda virtualenv and Jupyter notebook, e.g.,
  - Visual Studio code with
    - Python extension
    - Jupyter extension
    - Install iPyKernel
- TorchGeo 0.7.1

## Setup

- Create virtualenv, e.g., `.venv` in current directory in VSCode
- `pip install torchgeo==0.7.1 tensorboard`

## Run

- Run Jupyter notebook `run_inria.ipynb` for model training
- Optionally, view data with `view_inria.ipynb`

## Improvements

To existing features

- Upgrade BCE metric to Dice/IoU in TorchGeo 0.11+ (pending https://github.com/torchgeo/torchgeo/issues/4050)
- Get back the missing pixels 4097-5000 in the prediction images resulting from 1024x1024 patch size on 5000x5000 images
- Overlay predictions and ground truth labels for validation set

## Extensions

Add new features

- Output predicted buildings as vectors
- Run on images of Millbrae to improve the OpenStreetMap building outlines in this area
- Run larger models, e.g., `resnet152` backbone on cloud, or geo foundation models, with hyperparameter sweep
- Augment the Inria data with more modern data, e.g., MMEarth
