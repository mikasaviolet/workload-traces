# workload-traces
# ML Workload Execution Traces

This dataset describes the execution of machine-learning workloads
under different CPU and GPU allocations. It supports studies of
resource-dependent execution performance and workload scheduling,
including simulations of container-based ML environments.

The dataset contains three CSV files:

- **trace.csv**: 768 records covering image classification (`mnist`),
  language modeling (`lm`), and audio workloads (`audio`).
- **trace_container.csv**: 768 records covering the same workload
  categories and allocation ranges, with different execution measurements.
- **trace_old.csv**: 512 records covering image classification and
  audio workloads.

All files are headerless. The first four columns contain the workload
category, CPU allocation, GPU allocation, and execution duration.
CPU allocations range from 1 to 16, and GPU allocations range from
1 to 8. Each workload category has two records per allocation combination.

Training-task records in `trace.csv` and `trace_container.csv` also
contain time-series observations, resulting in variable-length rows.
`trace_old.csv` contains only the four basic fields.

The execution profiles can be used to examine how resource allocation
affects workload performance and to construct scheduling simulations.
Task-arrival sequences and scheduling decisions are not included.
