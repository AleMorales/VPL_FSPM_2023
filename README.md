# Virtual Plant Laboratory @ FSPM 2023

This repository contains the tutorials that were followed during the FSPM 2023
conference. Several versions of the tutorials are available depending on the 
context in which they are ran:

* Quarto document (`.qmd`) which may be opened in VS Code in rendered (or code
cells ran step by step).  

* Jupyter notebok (`.ipynb`) which may be opened in VS Code, Jupyter Lab or any
server that supports it (note: currently VPL depends on OpenGL so it will not 
run on a headless server).

* Julia script (`.jl`) which may be opened in VS Code or any text editor and ran
on a terminal.

These tutorials here are also available at the offical website of the VPLverse 
[virtualplantlab.org](http://virtualplantlab.com/) 
and at [VPLTutorials](https://github.com/AleMorales/VPLTutorials).The main difference
with respect to the tutorials in this repository is that a single notebook is
used here, in order to avoid starting a new Julia session for each tutorial.

## Running the tutorials locally

To run the tutorials locally, you need to install the following software [Julia](https://julialang.org/downloads/)
and the [IJulia.jl](https://github.com/JuliaLang/IJulia.jl) package. To run the
simulations in parallel, it is also needed to setup a Jupyter kernel that enables
multithreading. This can be achieved with the following:

```julia
using IJulia
installkernel("Julia (multi-threaded)", env=Dict("JULIA_NUM_THREADS"=>"4"))
```

You should replace `"4"` with the number of threads you want to use (i.e., the
number of physical or virtual cores you have in your computer).

## Running the tutorials on Google Colab

To run the tutorials on Google Colab, you need to have a Google account. Then,
you can upload the corresponding notebook to the Colab environment. Follow the
instructions at the start which will install Julia and setup the environment. 
After that initial step, you will have to refresh the website (Ctrl + R) and 
then you can continue running the tutorials afterwards.