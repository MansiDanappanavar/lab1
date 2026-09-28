
Course Title: Parallel and Grid Computing (PGC)

Experiment Title: Performance Analysis of Matrix Multiplication using Sequential, OpenMP.

1. Abstract
Abstract
This experiment compares sequential and OpenMP implementations of 
4000
×
4000
matrix multiplication. The sequential program took 348.02 seconds, while the OpenMP implementation using 8 threads reduced the execution time to 132.46 seconds, achieving a 
2.63
×
 speedup. Both implementations produced the correct result, 
C
[
0
]
[
0
]
=
4000.00
. The results demonstrate the performance improvement achieved through shared-memory parallelism using OpenMP.

2. Experimental Objectives
To implement 
4000
×
4000
 matrix multiplication using Sequential C and OpenMP.
To verify the correctness of the result by confirming 
C
[
0
]
[
0
]
=
4000.00
.
To measure the execution time of both implementations and calculate the speedup of OpenMP over the sequential program.
To compare the performance of single-threaded execution with 8-thread OpenMP parallel execution.
To analyze the performance improvement achieved through shared-memory parallelism using OpenMP.

3.Environment

•⁠  ⁠Operating System: Ubuntu on WSL2
•⁠  ⁠Programming Language: C
•⁠  ⁠Compiler: GCC
•⁠  ⁠Matrix Size: 4000 × 4000

Result

•⁠  ⁠Matrix Size: 4000 × 4000
•⁠  ⁠Verification: C[0][0] = 4000.00

The sequential execution time is used as the baseline for calculating the speedup of parallel implementations.
## 3. System Architecture & Source Code Matrix

| Paradigm | Source File | Compute Units | Compiler / Toolchain |
|---|---|---|---|
| Sequential | `matrix_sequential.c` | 1 CPU Core | GCC `-O2` |
| OpenMP | `matrix_openmp.c` | 8 CPU Threads | GCC `-O2 -fopenmp` |
## 4. Empirical Data & Benchmarking Results

### 4.1 Performance Summary Table

| Computing Model | Resources | Execution Time (s) | Speedup vs Sequential | Verification C[0][0] |
|---|---|---:|---:|---:|
| Sequential Baseline | 1 CPU Core | 348.023990 | 1.00× | 4000.00 |
| OpenMP Shared Memory | 8 Threads | 132.457362 | 2.63× | 4000.00 |
### 4.2 Experimental Configuration

| Parameter | Details |
|---|---|
| Course | Parallel and Grid Computing (PGC) |
| Experiment | Performance Analysis of Matrix Multiplication |
| Matrix Size | 4000 × 4000 |
| Programming Language | C |
| Operating System | Ubuntu on WSL2 |
| Compiler | GCC |
| Sequential Resources | 1 CPU Core |
| OpenMP Resources | 8 CPU Threads |
| Correctness Check | C[0][0] = 4000.00 |
| Baseline | Sequential Execution |
### Result

| Result | Observation |
|---|---|
| Correctness | Both implementations produced **C[0][0] = 4000.00** |
| Execution Time | OpenMP reduced execution time from **348.02 s to 132.46 s** |
| Speedup | OpenMP achieved a **2.63× speedup** over sequential execution |
| Parallelism | Performance improved using **8-thread shared-memory parallelism** |
| Baseline | Sequential execution was used as the baseline for speedup calculation |
## 5. Performance Visualizations

### Figure 1: Sequential Execution

![Sequential Execution](sequential.JPG)

**Figure 1:** Sequential matrix multiplication execution output.

### Figure 2: OpenMP Execution

![OpenMP Execution](openmp.JPG)

**Figure 2:** OpenMP matrix multiplication execution using 8 threads.

### Figure 3: Sequential Verification

![Sequential Verification](sequential.PNG)

**Figure 3:** Verification of the Sequential matrix multiplication result.

### Figure 4: OpenMP Verification

![OpenMP Verification](openmp.PNG)

**Figure 4:** Verification of the OpenMP matrix multiplication result.
## 6. Discussion & Technical Findings

1. **Sequential CPU Baseline (348.02 s):**  
   The sequential implementation performs matrix multiplication using a single CPU core. The large execution time is due to the computational cost of multiplying two 4000 × 4000 matrices.

2. **OpenMP Shared Memory (132.46 s, 2.63× Speedup):**  
   OpenMP parallelizes the matrix multiplication across 8 CPU threads. This reduces the execution time significantly compared with the sequential implementation.

3. **Parallel Performance:**  
   Although 8 threads were used, the speedup is 2.63× rather than an ideal 8×. This is due to factors such as memory access overhead, thread management, synchronization, and limitations of shared-memory bandwidth.

4. **Correctness Verification:**  
   Both Sequential and OpenMP implementations produced the same verified result, **C[0][0] = 4000.00**, confirming the correctness of the matrix multiplication.
   ## 7. Conclusion

The experiment demonstrates the performance improvement achieved through shared-memory parallelism using OpenMP. For 4000 × 4000 matrix multiplication, the Sequential implementation required **348.02 seconds**, whereas the OpenMP implementation using **8 threads** required only **132.46 seconds**.

The OpenMP implementation achieved a **2.63× speedup** compared with the sequential baseline. Both implementations produced the correct result of **C[0][0] = 4000.00**.

Overall, the experiment shows that OpenMP can significantly reduce execution time by distributing computational work across multiple CPU threads while maintaining result correctness.

