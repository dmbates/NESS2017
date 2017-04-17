# NESS2017
Materials for workshop, "Mixed-effects Models with Julia" at the 2017 New England Statistics Symposium

# Accessing Julia

## JuliaBox

- [`juliabox.com`](https://juliabox.com) provides a browser interface to `Julia` through [`Jupyter`](https://jupyter.org) notebooks.
    - login using one of the methods shown there
    - a good environment for classroom demonstrations
    - works best in live demo mode
    - the `Sync` tab allows access to [`github.com`](https://github.com) repositories or `Google Drive` directories.
    - the `Files` tab provides uploading/downloading of files or folders
    - the `Console` provides shell access
    - Jupyter notebooks can be run from the `Jupyter` tab
    - the first couple of sections of the tutorial may be of interest.  Later sections are more Python-oriented

## Downloads

- the web site for the open source system is https://julialang.org
- note the [`downloads`](https://julialang.org/downloads), [`docs`](https://docs.julialang.org), and [`packages`](https://pkg.julialang.org) tabs.
- under the [`learning`](https://julialang.org/learning/) tab there is a link to Julia version of the [`quantitative economics`](https://lectures.quantecon.org/jl/) course that may be useful.
- for those on Windows or Mac OSX, *JuliaPro* may be a better choice for installation.

## JuliaPro

- [`juliacomputing.com`](https://juliacomputing.com) is a company formed by core developers to provide commercial support
- They provide a *batteries included* version called `JuliaPro` for Windows and Mac OSX.
- You do need to create a login or use your google or facebook login before you can download the free version.


# Running Julia

- the REPL (read-eval-print-loop) provided by the application or the command-line
- Jupyter notebooks
   - also used for Python, R, Scala, etc.
   - need the `IJulia` package for Julia installed
- Juno within the Atom editor (part of JuliaPro) provides an integrated development environment (IDE)

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

# Julia packages in general

- Julia packages are always available as `git` repositories.  At present they must be available on https://github.com

- Registered packages are listed on https://pkg.julialang.org

- Documentation for packages is usually linked on the github repository.  Search for the package name on https://pkg.julialang.org then click on the name to get to the github repository.

- In the package listing you will see that several packages are owned by github groups, such as [`JuliaStats`](https://github.com/JuliaStats/), `JuliaIO`, `JuliaOpt`, `JuliaDiffEQ`.  These packages are expected to be well-maintained.

# Notebooks in this repository

The notebooks (files ending in `.ipynb`) whose names start with numbers are intended to be read in the sequence.
