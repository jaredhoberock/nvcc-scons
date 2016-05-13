# nvcc-scons
A SCons build tool for the NVIDIA compiler

This tool is based on the implementations at

 * github.com/thrust/thrust/blob/master/site_scons/site_tools/nvcc.py
 * bitbucket.org/scons/scons/wiki/CudaTool

The main difference between this tool and the tool found in the Thrust codebase
is that it has the simpler structure suggested by the CudaTool on bitbucket.

The main difference between this tool and CudaTool is that it does a more
comprehensive job incorporating the vanilla C and C++ command line flags into
nvcc's command line.

Other assorted enhancements:
* Automatically links a program with `nvcc` when it is discovered that CUDA source files have been compiled with separate compilation enabled
* Automatically links against `cudart` when it is discovered that object files originated with CUDA source files
