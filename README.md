# Docker files for Specfem3D_Globe images
This repository contains Dockerfiles for creating Docker images preinstalled with Specfem3D_Globe and its dependencies including ADIOS2 and ASDF.
The images are built on the [base containers](https://github.com/SeisSCOPED/container-base), which is prepared for using a specific version of IntelMPI with GNU libraries that are compatible with a run on NACC's HPC "Frontera" with Singularity.

Below are the Dockerfiles for the images:
- [Dockerfile](Dockerfile): A ubuntu20.04 based image with MPI, Specfem3D_Globe and Jupyter notebook.
- [Dockerfile_mpi](Dockerfile_mpi): A ubuntu20.04 based image with MPI, Specfem3D_Globe but no Jupyer notebook.
- [Dockerfile_centos7](Dockerfile_centos7): A centos7 based image with MPI, Specfem3D_Globe and Jupyter notebook.
- [Dockerfile_centos7_mpi](Dockerfile_centos7_mpi): A centos7 based image with MPI, Specfem3D_Globe but no Jupyer notebook.


# for deploying the image from your forked repository
This repository includes an action script for building and pushing the image to the GitHub Container Registry. In order to enable the action, you need to add the following secrets to your repository:
- `DOCKER_USERNAME`: Your Docker Hub username.
- `DOCKER_PASSWORD`: Your Docker Hub password.

from your forked repository, go to `Settings` -> `Secrets` -> `New repository secret` and add the above secrets. (https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions)