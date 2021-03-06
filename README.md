# Depth-averaged gas-particles model

Shallow water model for multiphase flow (gas+particles) with density of gas temperature-dependent. 

To compile:

> ./configure

To compile the code with OpenMP add the following flag in src/Makefile:
1) with gfortran: -fopenmp
2) with intel: -qopenmp

> make

> make install


The executable is copied in the bin folder.

Several examples can be found in the EXAMPLES folder.

It is possible also to use Docker container with the latest version of the model:

> docker pull demichie/sw_var_dens_model_alpine

Create a folde named SW_RUNS and then, from the folder containing SW_RUNS (not from within SW_RUNS).

Run the container with:

> docker run -v $PWD/SW_RUNS:/home/user_sw/SW_RUNS -i -t demichie/sw_var_dens_model_alpine bash

The docker container contains the code compiled and the utility to convert the output of the model in netcdf format. All the files in the SW_RUNS folder will be shared with the host system.


