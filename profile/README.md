# The Parallel Sparse Computation Toolkit

PSCToolkit is new software framework for solving large and sparse linear systems on current hybrid architectures, from small servers to high-end supercomputers, embedding multi-core CPUs and Nvidia GPUs at the node level. The framework has a modular structure and is composed of three main components which separate basic functionalities for managing distributed sparse matrices and executing some sparse matrix computations involved in iterative Krylov projection methods, eventually exploiting multi-threading and CUDA-based programming models, from the functionalities for setup and application of different types of one-level and multi-level algebraic preconditioners.

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=fortran,c,cpp" />
  </a>
</p>

- :earth_africa: Website: https://psctoolkit.github.io
- :mailbox_with_mail: E-Mail: psctoolkit@na.iac.cnr.it

:books: The *main scientific libraries* are:
- :blue_book: [PSBLAS](https://github.com/sfilippone/psblas3)
- :blue_book: [AMG4PSBLAS](https://github.com/sfilippone/amg4psblas)
- :blue_book: [PSBLAS-EXT](https://github.com/sfilippone/psblas3-ext)

## How to get them

To get them you can use the repository: [https://github.com/psctoolkit/psctoolkit](psctoolkit).

You can clone it
```
git clone git@github.com:psctoolkit/psctoolkit.git
cd psctoolkit
git submodule update --init --recursive
```
Or run it as a Docker image with
```
docker pull psctoolkit/psctoolkit
docker run -it psctoolkit:latest /bin/bash
```
or build it from the repository
```
git clone git@github.com:psctoolkit/psctoolkit.git
cd psctoolkit
docker build - < Dockerfile
```
