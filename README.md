# arcpro-interpol-compare
A Jupyter Notebook intended to reduce the amount of time spent manually comparing results from interpolation tools in ArcGIS Pro.

## General Overview
The Jupyter notebook (“interpol_comp.ipynb”) runs the following interpolation tools available in ArcGIS Pro: Topo To Raster, Natural Neighbor, and the kriging tools in the Geostatistical Wizard (Simple, Ordinary, Universal, and Empirical Bayesian). The results of the methods are compared using cross-validation statistics and by “training” an interpolation surface using some percentage of the data and comparing that surface to the remaining “testing” data. This notebook is intended to reduce the time spent manually comparing the interpolation results and should be used as an initial appraisal of interpolation methods; it is not an exhaustive assessment.

## Input file preparation
Create a new ArcGIS Pro project. The project folder and geodatabase are where you will put all of the input files described below.
### Required input files
- A **point feature class** (to be interpolated) stored **in the project geodatabase**. Make sure this feature class does not have a field called “RASTERVALU”. Rename that field to something else if necessary.
