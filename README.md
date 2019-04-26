# Matrix multiplication with ring rotation

[![Build Status](https://travis-ci.com/aurelienspnll/matrix-mult-ring-rotation.svg?branch=master)](https://travis-ci.com/aurelienspnll/matrix-mult-ring-rotation)

Teacher in charge : *Fabrice Huet* - [fabrice.huet@unice.fr](mailto:fabrice.huet@unice.fr)

# Requirements

You need :

- gcc
- [openMP](https://www.openmp.org/)
- [open-mpi](https://www.open-mpi.org/)

# Building

To build this project you need to run the following command:

```bash
mpicc mult-matrix-ring-rotation.c -o main -Wall -lm -fopenmp
```

# Executing

To execute this project:

```bash
mpirun -np N ./main example/A example/B
```

Where N is the number of machines.

# Executing on MacOS

If you run the program on mac and you get this error :

```bash

--------------------------------------------------------------------------
There are not enough slots available in the system to satisfy the N slots
that were requested by the application:
  ./main

Either request fewer slots for your application, or make more slots available
for use.
--------------------------------------------------------------------------
```

Add --oversubscribe to the command line :

```bash
mpirun --oversubscribe -np N ./main example/A example/B
```
