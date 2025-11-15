# The Parallel Sparse Computation Toolkit

PSCToolkit is new software framework for solving large and sparse linear systems on current hybrid architectures, from small servers to high-end supercomputers, embedding multi-core CPUs and Nvidia GPUs at the node level. The framework has a modular structure and is composed of three main components which separate basic functionalities for managing distributed sparse matrices and executing some sparse matrix computations involved in iterative Krylov projection methods, eventually exploiting multi-threading and CUDA-based programming models, from the functionalities for setup and application of different types of one-level and multi-level algebraic preconditioners.

<p align="center">
  <a href="https://psctoolkit.github.io">
    <img src="https://skillicons.dev/icons?i=fortran,c,cpp" />
  </a>
</p>

- :earth_africa: Website: https://psctoolkit.github.io
- :mailbox_with_mail: E-Mail: psctoolkit@na.iac.cnr.it

:books: The *main scientific libraries* are:
- :blue_book: [PSBLAS](https://github.com/sfilippone/psblas3)
- :blue_book: [AMG4PSBLAS](https://github.com/sfilippone/amg4psblas)

:heavy_exclamation_mark: PSBLAS-EXT deprecation

- GPU/extension plugin: [PSBLAS-EXT](https://github.com/sfilippone/psblas3-ext)
- **Status:** *discontinued*; features merged into PSBLAS since 3.9
- Use it only if you must build against PSBLAS $<$ 3.9
- **Migration:** routine names are largely compatible—prefer upgrading to PSBLAS $>=$ 3.9 as soon as possible

## How to get them

To get them you can use the repository: [https://github.com/psctoolkit/psctoolkit](psctoolkit) which
has two branches inside:
- a _master_ branch, containing the pointers to the latest release
- a _development_ branch, containing pointers to compatible commits of the development.

You can clone the master version by doing:
```bash
git clone git@github.com:psctoolkit/psctoolkit.git
cd psctoolkit
git submodule update --init --recursive
```
while for obtaining the development version you should do:
```bash
git clone git@github.com:psctoolkit/psctoolkit.git
cd psctoolkit
git checkout development
git submodule update --init --recursive
```

For both libraries, releases of the source code are available on the dedicated repositories:
- :blue_book: [PSBLAS](https://github.com/sfilippone/psblas3/releases)
- :blue_book: [AMG4PSBLAS](https://github.com/sfilippone/amg4psblas/releases)

### Docker images

The master version is available as a Docker image with
```bash
docker pull psctoolkit/psctoolkit
docker run -it psctoolkit:latest /bin/bash
```
while the development version can be obtained by doing:
```bash
docker pull psctoolkit/psctoolkit
docker run -it psctoolkit:development /bin/bash
```

In both cases, it can be buil directly from the repository
```bash
git clone git@github.com:psctoolkit/psctoolkit.git
cd psctoolkit
# If you want the master:
git submodule update --init --recursive
docker build -t psctoolkit .
# If you want the development:
git checkout development
git submodule update --init --recursive
docker build -t psctoolkit .
```

### Spack packages

We have a [Spack package](https://packages.spack.io/package.html?name=psblas) for PSBLAS, 
which can be installed by doing
```bash
spack install psblas
```

### Fedora Packages

The libraries are also available for the [Fedora distro](https://www.fedoraproject.org/):
- [PSBLAS](https://packages.fedoraproject.org/pkgs/psblas3/)
- [AMG4PSBLAS](https://packages.fedoraproject.org/pkgs/amg4psblas/)

They can be installed by doing
```bash
dnf install packagename
```
See the [Fedora help page](https://docs.fedoraproject.org/en-US/quick-docs/dnf/) for 
the usage of `dnf`, and [PSBLAS](https://packages.fedoraproject.org/pkgs/psblas3/) and
[AMG4PSBLAS](https://packages.fedoraproject.org/pkgs/amg4psblas/) for the various
 `packagename`.