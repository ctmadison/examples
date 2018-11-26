# ParaView

ParaView is an open source multiple-platform application for interactive, scientific visualization. It has a client–server architecture to facilitate remote visualization of datasets, and generates level of detail models to maintain interactive frame rates for large datasets.

This is a build of the ParaView [https://www.paraview.org] 5.6.0 source code located at [](https:/https://www.paraview.org/download/)

## Instructions


### Build instructions
Download the [ParaView_Superbuild.def](https://github.com/sylabs/examples/blob/master/visualization/ParaView/ParaView_Superbuild.def) file to your local computer.

Build the sif file by executing the following command:

```
   sudo singularity build ParaView.sif ParaView_Superbuild.def
```

Copy the resultant `ParaView.sif` file to all nodes you wish to run on (global storage can also be used).

### Infrastructure Requirements
Singularity 3.0 must be installed on all of the nodes you are running on.

The resultant `horovod.sif` file (from the above build step) must be located in the same directory structure on every node.

The same (or ABI compatible) version of OpenMPI has to be installed on all of the nodes you intend to run on (**NOTE:** this host version must match the OpenMPI version, or be ABI compatible, with the MPI in the container).

Nvidia GPU's must be installed and the CUDA/Nvidia drivers must be installed on the nodes (at least one per node).

An existing network infrastructure running across all nodes you intend to run on.

The ability to SSH between all of the nodes (for the user running horovod) without having to supply passwords (ssh keys setup).

Knowledge of MPI and mca parameters (these are specific to your site installation/network).

### Example runs


