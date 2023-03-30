# Virtual Plant Laboratory @ FSPM 2023

This repository contains the tutorials that were followed during the FSPM 2023
conference as a Jupyter notebook.

These tutorials here are also available at the offical website of the VPLverse 
[virtualplantlab.org](http://virtualplantlab.com/) 
and at [VPLTutorials](https://github.com/AleMorales/VPLTutorials).The main difference
with respect to the tutorials in this repository is that a single notebook is
used here, in order to avoid starting a new Julia session for each tutorial.

## Setup

Follow these steps to setup the environment to run the tutorials locally:

* Install [Julia](https://julialang.org/downloads/) on your machine (version 1.8.5).

* Run Julia within a terminal and run the following code to install the dependencies:

```julia
using Pkg
pkg"add https://github.com/AleMorales/VPL.git; precompile"
pkg"add https://github.com/AleMorales/Ecophys.jl.git; precompile"
pkg"add https://github.com/AleMorales/Sky.jl.git; precompile"
pkg"add Distributions"
pkg"add Plots"
```

* Add suport for Jupyter notebooks (replace `"4"` with the number of threads you
want to use in your machine).

```julia
pkg"IJulia"
using IJulia
installkernel("Julia (multi-threaded)", env=Dict("JULIA_NUM_THREADS"=>"4"))
```

* Download the notebook from this repository.

* In the same terminal, run the following code to start the Jupyter notebook 
server. Replace `"dir"` with the path where the notebook is located:

```julia
notebook(dir="dir")
```

* The notebook will open in the brower. Make sure to select the multithreaded
kernel.