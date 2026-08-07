# Accessing the Datasets from ESA Open Science Catalogue
 
## Overview
 
The ESA Open Science Catalogue hosts a growing number of Earth observation and scientific datasets distributed in **cloud-optimized formats** — very often in `.zarr` or `.parquet` format (for vector data). These formats allow efficient access to large N-dimensional datasets, easy creation of subsets, selection of variables of interest, and straightforward visualisation.
 
While `.zarr` is well-suited for scalable, parallel, and remote access, it is less familiar to many users than traditional formats like NetCDF or GeoTIFF. New users frequently encounter friction when trying to:
 
- Locate the correct `.zarr` asset URL for a given dataset in the catalogue
- Open remote Zarr stores correctly
- Understand the lazy-loading model and avoid accidentally downloading entire datasets
- Inspect metadata, dimensions, and variables before committing to a full read
- Subset and visualize data efficiently
A template Jupyter Notebook (`0_templates/data_access_template.ipynb`) provides a minimal, reusable example that covers loading an example dataset, inspecting and reading the metadata of the product, creating a subset, and visualising the selected variable.
The goal of this repository is to lower the entry barrier and provide a starting point for external users to discover a broad number of datasets in a consistent manner, and for data providers to see an example of how such a data access notebook can be prepared and adapted to any dataset published in the catalogue.
 
## Repository structure
 
This repository is organized with **one folder per product**. Each product folder may contain one or more notebooks, e.g.:
 
- a **data access notebook**, showing how to locate and open the `.zarr` file or any other file stored in the object storage
- a **data visualisation notebook**, showing how to plot the main variables of the dataset, providing ideally a short interpretation if needed

## Adding a new data access notebook
 
A generic **data access notebook tutorial** is provided in the first folder (`0_templates/data_access_tutorial`). To add a new notebook to the collection:
 
1. Fork/copy the tutorial notebook into a new folder named after the project name.
2. Update the description of the datasets and links to point to the new products.
3. Adjust the area-of-interest, time range, and variable names as needed.
4. Optionally add a companion visualisation notebook following the same pattern.

## Open also to external users
 
If you are not an EarthCODE user, you can still use the notebooks to access the products. All dependencies are open and free to use — the only requirement is a working Python environment and internet access. To use these notebooks:
 
1. Clone/download this repository (or just the notebook file).
2. Install dependencies.
3. Launch a Python interpreter, e.g. Jupyter Notebook.
4. Edit the placeholders if needed (e.g. collection URL).
5. Run cells sequentially.
If you encounter any problems or have any issues to address, please leave us feedback on the **EarthCODE Discourse Forum**: [https://discourse-earthcode.eox.at/](https://discourse-earthcode.eox.at/)
 
