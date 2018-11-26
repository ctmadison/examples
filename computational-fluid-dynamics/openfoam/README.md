# OpenFOAM

OpenFOAM is a C++ toolbox for the development of customized numerical solvers, and pre-/post-processing utilities for the solution of continuum mechanics problems, including computational fluid dynamics. 

## Instructions

### Build Instructions

Build the sif file by executing the following command:
```
   sudo singularity build OpenFOAM.sif OpenFOAM.def
```

Copy the resultant `OpenFOAM.sif` file to all nodes you wish to run on (global storage can also be used).

### Infrastructure Requirements
Singularity 3.0 must be installed on all of the nodes you are running on.

The resultant `horovod.sif` file (from the above build step) must be located in the same directory structure on every node.

The same (or ABI compatible) version of OpenMPI has to be installed on all of the nodes you intend to run on (**NOTE:** this host vers
ion must match the OpenMPI version, or be ABI compatible, with the MPI in the container).

Nvidia GPU's must be installed and the CUDA/Nvidia drivers must be installed on the nodes (at least one per node).

An existing network infrastructure running across all nodes you intend to run on.

The ability to SSH between all of the nodes (for the user running horovod) without having to supply passwords (ssh keys setup).

Knowledge of MPI and mca parameters (these are specific to your site installation/network).

### Example runs


