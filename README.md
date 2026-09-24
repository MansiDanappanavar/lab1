  Abstract
This experiment compares four approaches for 
4000
×
4000
 matrix multiplication: sequential C, OpenMP, Open MPI, and CUDA. All implementations produced the correct result, 
C
[
0
]
[
0
]
=
4000.00
. The sequential execution took 348.02 s, while OpenMP and Open MPI achieved speedups of 
2.63
×
 and 
3.74
×
, respectively. CUDA provided the highest performance, achieving a 
2109.18
×
 speedup with a total phase time of 0.1650 s. The results demonstrate the significant benefits of parallel and GPU computing for large-scale matrix operations.
