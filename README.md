# Plot data for arXiv:2512.23917

Summary data for **Tensor Computing Application Programming Interface: An
Application-Oriented, Lightweight API for Portable High-Performance Tensor
Network Computations** ([arXiv:2512.23917](https://arxiv.org/abs/2512.23917)).
Figure numbers below refer to the accepted manuscript.

## Files

- [`data/itebd_summary.csv`](data/itebd_summary.csv): iTEBD wall-clock timings for
  Application A (1D transverse-field Ising model), used in Figs. 6 and 8(a).
- [`data/bp_summary.csv`](data/bp_summary.csv): belief-propagation (BP) wall-clock
  timings for Application B (kicked Ising model on a 156-qubit heavy-hex lattice),
  used in Figs. 7 and 8(b).

## Columns and series

Both files use the columns `series,chi,mean_s,min_s,max_s`. Here, `chi` is the
tensor-network bond dimension, and `mean_s`, `min_s`, and `max_s` are the mean,
minimum, and maximum wall-clock times **in seconds per iteration**. Means give
the plotted markers; minimum–maximum ranges give the shaded bands, not standard
deviations or confidence intervals. These files contain summaries, not raw
iteration records.

| File | `series` | API / back end | Hardware | Figures |
| --- | --- | --- | --- | --- |
| iTEBD | `tcapi_cpu` | TCAPI / TCF I | Intel Xeon 6240R CPU | 6, 8(a) |
| iTEBD | `native_cpu` | Native API / TCF I | Intel Xeon 6240R CPU | 8(a) |
| iTEBD | `tcapi_gpu` | TCAPI / TCF II | NVIDIA H100 GPU | 6 |
| BP | `tcapi_apple_m2_ultra` | TCAPI / TCF III | Apple M2 Ultra CPU | 7 |
| BP | `tcapi_fugaku_4` | TCAPI / TCF I | Fugaku, 4 Fujitsu A64FX nodes | 7 |
| BP | `tcapi_fugaku_156` | TCAPI / TCF I | Fugaku, 156 Fujitsu A64FX nodes | 7, 8(b) |
| BP | `native_fugaku_156` | Native API / TCF I | Fugaku, 156 Fujitsu A64FX nodes | 8(b) |

TCF I uses GraceQ/tensor, TCF II uses a wrapper over cuTENSOR and cuTensorNet,
and TCF III uses Cytnx.