# METAR Archive Cookbook

<img src="thumbnails/thumbnail.png" alt="thumbnail" width="300"/>

[![nightly-build](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/METAR_archive-cookbook/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/475509405.svg)](https://zenodo.org/badge/latestdoi/475509405)

This Project Pythia Cookbook accesses, analyzes, and visualizes real-time and archived surface meteorological observations from a worldwide network of (mostly) airport locations, originally encoded in [METAR](https://www.weather.gov/asos/METAR.html) format.

## Motivation

While a number of Pythia cookbooks have focused on raster-based datasets (e.g., NWP and reanalysis output in NetCDF and Zarr), there is a need for similar examples which use direct observational data at actual physical locations. These inherently tabular datasets are well-suited for not only Python tools such as Pandas but also those that provide database-like query-based services (e.g. DuckDB).

## Structure

We will work with a cloud-served, continually-updating archive of METAR observations that are in GeoParquet format. We will use DuckDB to query them, create a simple method to visualize world-wide surface weather observations at a given hour, perform a variety of time-series analyses, and statically and/or interactively visualize our results with Matplotlib, Geopandas and Lonboard.

### Section 1 (Introduction)

We will describe the file format of the METAR archive (Parquet) and give an overview of DuckDB, which we will use to perform SQL-like queries on the archive.


### Section 2 ( Examples )

1. Create a synoptic station model plot from METAR observations at a current or user-specified hour.
2. Perform an interactive visualization of METAR data using GeoPandas.
3. Perform an interactive visualization of METAR data using Lonboard.
4. Time-series analysis
5. Compare METAR observations to gridded reanalyses
6. Demonstrate an AI agent that translates METAR observations into plain-language text.

## Running the Notebooks

You can either run the notebooks in the Cookbook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables "one click"
execution in the cloud. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon (see screenshots [here](https://foundations.projectpythia.org/preamble/how-to-use/#running-pythia-foundations-examples)),
and a text box will appear. Type or paste the Pythia Binder link
(`https://binder.projectpythia.org`) and click "Launch".
After a few moments you should be presented with a
notebook that you can interact with. You’ll be able to execute code
and even change the example programs. At first the code cells
have no output, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in the Pythia Foundations chapter [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter).

Note, not all Cookbook chapters are executable. If you do not see
the rocket ship icon, such as on this page, you are not viewing an
executable book chapter.


### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

1. Clone the `https://github.com/ProjectPythia/METAR_archive-cookbook` repository:

   ```bash
    git clone https://github.com/ProjectPythia/METAR_archive-cookbook.git
   ```

1. Move into the `METAR_archive-cookbook` directory
   ```bash
   cd METAR_archive-cookbook
   ```
1. Create and activate your conda environment from the `environment.yml` file
   ```bash
   conda env create -f environment.yml
   conda activate METAR-archive-cookbook
   ```
1. Move into the `notebooks` directory and start up Jupyterlab
   ```bash
   cd notebooks/
   jupyter lab
   ```
