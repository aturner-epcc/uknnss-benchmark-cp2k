# UK NSS CP2K benchmark

**Important:** Please do not contact the benchmark maintainers directly with any questions.
All questions on the benchmark must be submitted via the procurement response mechanism.

This repository describes the CP2K benchmark for the UK NSS procurement. CP2K is ...

The specific benchmark used for this procurement is the H2O-DFT-LS benchmark available
in the main CP2K repository on Github. This is a large system that runs a single-point
energy calculation using linear scaling DFT.

## Status

Stable

## Maintainers

- Andrew Turner

## Overview

### Software

[https://github.com/aportelli/grid-benchmark](https://github.com/aportelli/grid-benchmark)

### Architectures

- CPU: x86
- GPU: NVIDIA, AMD

### Languages and programming models

- Programming languages: Fortran
- Parallel models: MPI, OpenMP
- Accelerator offload models: CUDA, HIP

## Building the benchmark

**Important:** All results submitted should be based on the following repository commits:

- CP2K repository: release version 2026.1
- H2O-DFT-LS benchmark: version from CP2K release 2026.1

Any modifications made to the source code for the baseline build or the optimised build must be 
shared as part of the offerer submission.

### Permitted modifications

#### Baseline build

For the baseline run the only permitted modifications allowed are those that
modify the CP2K or its dependencies to resolve unavoidable compilation or
runtime errors.

#### Optimised build

Any modifications to the source code are allowed as long as they are able to be provided
back to the community under the same licence as is used for the software package that is
being modified.

### Manual build

As an example, we provide manual instructions for building CP2K on
[IsambardAI](https://docs.isambard.ac.uk/specs/#system-specifications-isambard-ai-phase-2).

It is also possible to install CP2K using Spack.

## Running the benchmark

### Required Tests

- **Target configuration:** Grid_Benchmark should be run on a minimum of * ?? GPU/GCD*.
- **Reference FoM:** The reference FoM is from the IsambardAI system using 128 GPU (32 nodes) is * ?? *.

**Important:** For the both the baseline build and the optimised build, the projected FoM submitted 
must give at least the same performance as the reference value.

### Benchmark execution

TBC

## Correctness Checking

TBC - confirm energy from PRACE UBS

## Reporting Results

The offeror should provide copies of:

- Details of any modifications made to the CP2K or dependencies source code
- The compilation process and configuration settings used for the benchmark results - 
  including makefiles, compiler versions, dependencies used and their versions or
  Spack environment configuration and lock files if Spack is used
- The job submission scripts and launch wrapper scripts used (if any)
- The `H2O-dft-ls.inp` file used
- The output from the `validate.py` script
- All standard CP2K output files
- A list of options passed to CP2K (if any)

## License

This benchmark description and any associated files are released under the
MIT license.
