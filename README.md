# End-to-end GeoAI with TorchGeo

Last updated: Dec 18th 2025

Using a segmentation neural network to detect objects in satellite raster data is now a fairly common GeoAI use case, and can be done in a broad-brush sense with no-code or low-code tools. Finer-grained control of the model, data, and processing is often still desirable for real end-to-end analyses, however. The TorchGeo tool builds upon PyTorch and PyTorch Lightning to enable end-to-end GeoAI for a wide range of use cases, and we show how plain PyTorch code is augmented by Lightning’s data and model modules, then in turn by TorchGeo’s geospatial functionality. This lets us run end-to-end building detection and control the details.

## Requirements

- Machine that can run Conda virtualenv and Jupyter notebook, e.g.,
  - Visual Studio code with
    - Python extension
    - Jupyter extension
    - Install iPyKernel

## Setup

- Create virtualenv, e.g., `.venv` in current directory in VSCode
- `pip install torchgeo tensorboard`

## Run

- Run Jupyter notebook `run_inria.ipynb`

## Improvements

- Find why it detects all gray, e.g., roads, and not just buildings
- Run using better data, maybe MMEarth
- If there is a reasonable hyperparameter sweep to try, run it to optimize model performance
- Run on images of Millbrae to improve the OpenStreetMap building outlines in this area
