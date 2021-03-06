# Implementation of Fast-GPU-PCC algorithm with Python CUDA and C OPENMP

This repository contains the implementation of Fast-GPU-PCC algorithm in Python CUDA and C OPENMP.

The original repository of the algorithm can be viewed here: https://github.com/pcdslab/Fast-GPU-PCC .

The folder fast-gpu-pcc contains the original code modified for our tests. 

## Matrix generator

Use the following command to compile the random_matrix_to_file.cpp code:

g++ random_matrix_to_file.cpp -o random_matrix_to_file_exec

Execution: 

./random_matrix_to_file_exec n m 

where:

n = number of voxel;

m = length of time series.

## Python-CUDA

Use the following command to execute the python-cuda-pycuda/CPU_side.py code:

python3 CPU_side.py

## C-OPENMP
Use the following command to compile the c-openmp/CPU_side.c code:

gcc -fopenmp CPU_side.c -o CPU_side.x -lm

Execution:

./CPU_side.x N L t

n = number of voxel;

m = length of time series;

t = to write the matrix in a text file.

## Requirements

python: 3.6.9

GCC: 7.5.0

pycuda: 2019.1.2

scikit-cuda: 0.5.3

numpy: 1.19.1
