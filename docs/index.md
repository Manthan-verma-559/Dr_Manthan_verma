# <p align="center">AITHON <br> Asynchronous Implementation of Turbulence for Hydro-Astrophysical Applications using Optimized Numerics</p>

**Developers**:  
- *Manthan Verma (PhD student at IIT Kanpur)*  
- *Prof. Mahendra Verma (IIT Kanpur)*

## Overview
AITHON is a code developed for solving general-purpose Direct Numerical Simulations (DNS) of Hydro-Astrophysical turbulence problems. The code leverages optimized numerics for efficient and scalable computation.

## Problems It Can Solve
AITHON is capable of solving the following types of problems:
- **Hydrodynamics** (with and without anisotropy)
- **Magnetohydrodynamics (MHD)** (with and without anisotropy)
- **Scalar flows**

## Scalability and Testing
AITHON has been rigorously tested and scaled on various high-performance computing platforms, including:

- **Frontier (Oak Ridge National Laboratory)**: 32,768 AMD MI250X GPUs across 4,096 nodes.
- **Selene (NVIDIA)**: 512 nodes.
- **ALCF (Polaris)**: 256 nodes.

The scalability and performance of the code make it suitable for handling large-scale turbulence simulations in astrophysical contexts.

## Advanced GPU and Communication Technologies
<p align="justify"> AITHON employs the latest GPU technologies such as CUDA-aware MPI for efficient communication. Additionally, it can be built with advanced technologies like NVSHMEMs or ROCSHMEMs, which allow for kernel-to-kernel communication. These shared memory (SHMEM) technologies, which are rarely utilized in turbulence codes, enable AITHON to achieve nearly linear scaling, significantly enhancing its performance in terms of both time and memory efficiency.</p>

## FFTs INTEGRATED
For single GPU solver it uses normal cufft/rocfft. But For Multi-GPU/multi-node following FFTs are integrated in solver
- GPU-FFT (By Verma et al) (https://github.com/Manthan-Verma/GPU_FFT)
- cuFFTMp (By NVIDIA)
