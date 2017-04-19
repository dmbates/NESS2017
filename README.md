# NESS2017
Materials for workshop, "Mixed-effects Models with Julia" at the 2017 New England Statistics Symposium, Friday, April 21, 2017

### Installing Julia

- It will help if participants install [`Julia`](https://julialang.org) (version 0.5.1), before the workshop.  An alternative is to use the online service at https://juliabox.com, as described below.

- Julia can be installed from https://julialang.org/downloads/ or as the no-cost version of `JuliaPro` from https://juliacomputing.com.

- `JuliaPro` is a "batteries included" version of Julia with several of the more widely-used packages.  Those using Windows or Mac OSX may find it more convenient than downloading the base release and adding packages.

### Jupyter notebooks

- We will use [Jupyter notebooks](https://jupyter.org) throughout the course.
- The interface to Jupyter notebooks is included with `JuliaPro`.
- Those who install Julia from the download site will need to add the `IJulia` package.  See below for instructions on adding Julia packages.

### Julia packages

- Julia packages are added with, e.g.
```
Pkg.add("MixedModels")
```

- It is a good practice to run
```
Pkg.update()
```
weekly or more frequently to ensure you have the latest package versions.

- To check which version of a package is installed, use, e.g.
```
Pkg.status("MixedModels")
```

- To see all of the directly and indirectly installed packages, use
```
versioninfo(true)
```

- In addition to [`MixedModels`](https://github.com/dmbates/MixedModels.jl), you should install `DataFramesMeta`, `FreqTables`, `Gadfly`, `IJulia`, `Rcall`, and `RData`.  Other packages we will use, (e.g. DataFrames, GLM) will be installed as requirements of these packages.  Ensure that you have v0.8.0 or later of the `MixedModels` package.

### Julia packages in general

- Julia packages are `git` repositories.  At present registered packages must be available on https://github.com

- Registered packages are listed on https://pkg.julialang.org

- Documentation for packages is usually linked in the github repository.  Search for the package name on https://pkg.julialang.org then click on the name to get to the github repository.

- In the package listing you will see that several packages are owned by github groups, such as [`JuliaStats`](https://github.com/JuliaStats/), `JuliaIO`, `JuliaOpt`, `JuliaDiffEQ`, ...  These packages can be expected to be well-maintained.

### Notebooks in this repository

The notebooks (files ending in `.ipynb`) whose names start with numbers are intended to be read in the sequence.

### JuliaBox

- [`juliabox.com`](https://juliabox.com) provides a browser interface to `Julia` through [`Jupyter`](https://jupyter.org) notebooks.
    - login using one of the methods shown there
    - the `Sync` tab allows access to [`github.com`](https://github.com) repositories or `Google Drive` directories.
    - the `Files` tab provides uploading/downloading of files or folders
    - the `Console` provides shell access
    - Jupyter notebooks can be run from the `Jupyter` tab
    - the first couple of sections of the tutorial may be of interest.  Later sections are Python-oriented and perhaps of less interest.

# Importing data

## RData

- the `RData` package can used to read saved `.RData` or `.rda` files.  It does not require a local installation of `R`

## RCall

- if you have a local installation of `R`, the `RCall` package allows you to run and communicate with an `R` process from within `julia`.

## Feather

   - [`feather`](https://github.com/wesm/feather) is a language-agnostic form of
    dataframe storage.  The R package is
    [`feather`](https://CRAN.R-project.org/package=feather), Julia package is
    [`Feather`](https://github.com/JuliaStats/Feather.jl) and Python package is
    [`feather-format`](https://github.com/wesm/feather/tree/master/python).

   - when reading a Feather file in Julia use `nullable=false` for the time being

## readtable and the CSV package

- there is the `readtable` function in `DataFrames` and a `CSV` package for reading CSV files.

## PyCall/Pandas

- the `PyCall` package essentially integrates Python into Julia.
- the `Pandas` package provides access to the `pandas` package for `Python`
