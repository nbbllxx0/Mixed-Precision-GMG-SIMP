# Mixed-Precision Matrix-Free Geometric Multigrid for 3D SIMP Topology Optimization

Companion repository for:

> Yang, S., Wang, J., and Wang, Y. (2026).
> *Mixed-Precision Matrix-Free Geometric Multigrid for 3D SIMP Topology Optimization on a Single GPU.*
> Preprint in preparation.

## Status

**Placeholder.** The reproducibility artifacts for this paper will be released
here once the arXiv preprint is online. A BibTeX entry and a tagged submission
revision will be added at that time.

## Scope

This paper builds directly on the companion paper:

> Yang, S., Wang, J., and Wang, Y. (2026).
> *Matrix-Free 3D SIMP Topology Optimization with Fused Gather-GEMM-Scatter
> Kernels.* arXiv:2604.18020.
> Companion repository:
> https://github.com/nbbllxx0/Fused-Gather-GEMM-Scatter-Kernels

The Level-0 fused gather-GEMM-scatter matvec kernel introduced in that paper
is used here as fixed infrastructure. The present work contributes the
matrix-free Galerkin multigrid hierarchy, the Chebyshev-Jacobi smoother, the
mixed-precision descent schedule (BF16 finest, FP32 mid, FP64 coarsest), and
the closed-form admissibility bound on the effective condition number.

## Planned contents

Following the structure of the companion repository:

- `src/gpu_fem/` — Galerkin matrix-free GMG hierarchy and SIMP driver
- `experiments/paper4/` — Phase-1 validation gates (M1–M8) and Phase-2
  headline experiments (E1–E10)
- `papers/paper4/` — manuscript source and figure-generation pipeline
- `ARTIFACT_MAP.md` — manuscript result ↔ driver script ↔ CSV artifact map
- `environment.yml` — conda environment specification

## License

Code will be released under the BSD 3-Clause license at the time of arXiv
publication, matching the license of the companion repository.
