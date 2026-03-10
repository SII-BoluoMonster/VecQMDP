# Vec-QMDP: Vectorized POMDP Planning on CPUs for Real-Time Autonomous Driving

[![arXiv](https://img.shields.io/badge/arXiv-2602.08334-b31b1b.svg)](https://arxiv.org/pdf/2602.08334)
[![Project Page](https://img.shields.io/badge/Project-Website-blue)](https://xxx)

This repository contains the official implementation of **Vec-QMDP**, a high-performance, CPU-native parallel POMDP planner designed for robust autonomous driving in uncertain environments.

## News 📢
- **[2026-02]** Our paper is available on [ArXiv](https://arxiv.org/pdf/2602.08334)!
- **[2026-02]** Project website is live at [https://xxx](https://xxx).
- **[Coming Soon]** We are currently refactoring the codebase for open-source release. Stay tuned!

## Abstract
Planning under uncertainty for real-world robotics tasks requires reasoning in enormous high-dimensional belief spaces. **Vec-QMDP** is a CPU-native parallel planner that aligns POMDP search with modern CPUs' SIMD architecture. By adopting **Data-Oriented Design (DOD)** and a **hierarchical parallelism scheme**, Vec-QMDP achieves **227×–1073× speedup** over state-of-the-art serial planners, enabling real-time, high-fidelity planning on standard CPU hardware without the latency overhead of GPU-based solvers.

## Key Features
- **SIMD-Accelerated Search:** Fully vectorized tree expansion and belief updates using AVX-512/AVX2.
- **Data-Oriented Design (DOD):** Cache-friendly, contiguous memory layouts replacing traditional pointer-based tree structures.
- **Vectorized Collision Checking:** High-throughput spatial queries via vectorized STR-trees.
- **Load Balancing:** Optimized UCB-based distribution across multiple CPU cores and SIMD lanes.

## Citation
If you find our work or code useful, please cite our paper:

```bibtex
@article{jin2026vecqmdp,
  title={Vec-QMDP: Vectorized POMDP Planning on CPUs for Real-Time Autonomous Driving},
  author={Jin, Xuanjin and Dong, Yanxin and Sun, Bin and Xu, Huan and Hao, Zhihui and Lang, XianPeng and Cai, Panpan},
  journal={arXiv preprint arXiv:2602.08334},
  year={2026}
}
