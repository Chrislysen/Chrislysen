# Christian Lysenstøen

Second-year AI student at Inland Norway University of Applied Sciences, currently on exchange at UC Berkeley. I build ML systems that work under real-world constraints — crash-prone hardware, tight budgets, noisy quantum backends — and I publish the results honestly, including when things don't work.

Papers on arXiv:
* **[Feasible-First Exploration for Constrained ML Deployment Optimization](https://arxiv.org/abs/2604.25073)** — Crash-aware TBA→TPE hybrid optimizer. 80% discovery rate of the globally optimal model vs. 30% for standalone TPE; reduced wasted trials from 74% to 42%. Benchmarked on DeployBench: 5 architectures × 3 backends × 3 quantizations × 6 batch sizes across 5 NVIDIA GPUs (H100, A100, RTX 5080, L4, T4), 10 seeds each. 46/46 tests passing. (arXiv:2604.25073, April 2026)
* **[SLO-Guard: Crash-Aware, Budget-Consistent Autotuning for SLO-Constrained LLM Serving](https://arxiv.org/abs/2604.17627)** — Two-phase TBA→TPE optimizer for vLLM tuning. 150-trial A100 study: 75/75 feasibility, zero crashes; statistically tied with random search on best latency (p=0.84) but 4.4× tighter cross-seed variance under concurrent load. (arXiv:2604.17627, April 2026)
* **Hidden Device Heterogeneity in Constrained ML Deployment** — PyTorch's INT8 quantization silently switches from GPU to CPU, creating 39% feasibility flip rates. (submitted April 2026)

---

### Currently working on

- Expanding multi-GPU benchmark results for the TBA deployment optimizer (H100, A100, RTX 5080, L4, T4)
- Waiting on D-Wave LaunchPad QPU access to complete the quantum annealing benchmark
- Cross-hardware validation of SLO-Guard on non-A100 GPUs
- Coursework at UC Berkeley (CS 61C, concurrent with research)

---

### Coursework (UC Berkeley, Spring 2026)

**Enrolled:**
- CS 61C — Great Ideas in Computer Architecture
- EECS 127 — Optimization Models in Engineering
- ENGIN 183 — Technology Innovation and Entrepreneurship
- ASTRON C12 — The Planets (astrophysics breadth)

**Auditing:**
- CS 152/252A — Computer Architecture and Engineering
- CS 170 — Efficient Algorithms and Intractable Problems
- CS 185/285 — Deep Reinforcement Learning, Decision Making, and Control
- CS 61B — Data Structures

Focus areas: systems architecture, optimization theory, and deep RL — chosen to complement my ML deployment research with hardware-level understanding and formal optimization foundations.

---

### Research interests

**ML systems and deployment optimization** — How do you find the best inference configuration (backend, quantization, batch size) when most of the search space crashes or violates constraints? I built a two-phase optimizer (Thermal Budget Annealing → constrained TPE) that treats crashes as data and maps feasible regions before exploiting them.

**Quantum-classical benchmarking** — Fair comparisons between classical simulated annealing, D-Wave quantum annealing, and QAOA on IBM hardware. I design standardized solver interfaces and report negative results when the hypothesis doesn't hold.

**Agentic AI and applied CV** — LLM-powered tool-calling agents for domain-specific automation, and competition-grade object detection pipelines with ONNX inference and ensemble methods.

---

### Pinned repositories

[**Constrained-ML-Deployment**](https://github.com/Chrislysen/Constrained-ML-Deployment)
Two research papers sharing the DeployBench infrastructure. (1) TBA: crash-aware two-phase optimizer for constrained ML deployment. (2) Hidden Device Heterogeneity: empirical study showing INT8 dynamic quantization silently moves inference to CPU, creating stochastic feasibility boundaries. 2,150 measurement trials, 5 GPU types, full reproducibility.

[**SLO-Guard**](https://github.com/Chrislysen/SLO-Guard)
Crash-aware autotuner for vLLM serving. Optimizes vLLM configs (batching, memory, execution mode) under hard latency/memory SLOs. Crashes are encoded as constraint violations and replayed into a warm-started TPE phase, so failed trials inform subsequent search. 150-trial A100 study on Qwen2-1.5B: 75/75 feasibility, zero crashes; statistically tied with random search on peak latency (Mann-Whitney p=0.84) but 4.4× tighter cross-seed variance on best latency under concurrent load. Paper at arXiv:2604.17627. Both sequential and concurrent harness datasets published for replication.

[**deploy-agent**](https://github.com/Chrislysen/deploy-agent)
Productized version of TBA. CLI + FastAPI dashboard + MCP server for automated ML deployment optimization. Give it a model and hardware constraints, it searches backends/quantization/batch sizes and returns the best feasible config with full evidence. Crash handling, structured JSON logs, live WebSocket charts.

[**dwave-benchmark**](https://github.com/Chrislysen/dwave-benchmark)
Classical SA vs D-Wave quantum annealing on Max-Cut and spin glass problems. Phase 1 complete: all classical solvers converge to identical solutions up to n=500 with zero quality gap. Phase 2 (QPU) pending D-Wave access. Common solver interface, reproducible seeds, timing analysis showing Neal SA ~400x faster than pure Python SA.

[**qaoa-benchmark**](https://github.com/Chrislysen/qaoa-benchmark)
Negative-result study: budget-aware classical optimizers vs COBYLA/SPSA for QAOA parameter tuning under noisy simulation. Finding: shallow QAOA landscapes are too smooth — COBYLA with fixed defaults matched or beat the learning optimizer. 375 total runs, 3 graphs, 5 budget levels, 5 seeds.

[**Norwegian-AI-Championship**](https://github.com/Chrislysen/Norwegian-AI-Championship)
NM i AI 2026 competition entry (Team INNBerkeley). Three tasks: YOLOv8x object detection with ONNX inference, multi-scale TTA, and WBF ensembling; a FastAPI accounting agent using Gemini 2.5 Flash + Tripletex API; and an A* pathfinding agent for Norse world prediction.

[**ML2-Exam**](https://github.com/Chrislysen/ML2-Exam)
Machine Learning 2 exam work.

---

### Stack

Python, PyTorch, vLLM, ONNX Runtime, Optuna, Qiskit, D-Wave Ocean SDK, FastAPI, Docker, LaTeX, SciPy, NetworkX, Matplotlib, NumPy, scikit-learn, Qiskit Aer, Google Colab

---

### Contact

UC Berkeley (exchange 2025–2026) · INN Norway (home institution)
