# Christian Lysenstøen

Second-year AI student at Inland Norway University of Applied Sciences, currently on exchange at UC Berkeley. I build ML systems that work under real-world constraints — crash-prone hardware, tight budgets, noisy quantum backends — and I publish the results honestly, including when things don't work.

Paper pending on arXiv: *Feasible-First Exploration for Constrained ML Deployment Optimization in Crash-Prone Hierarchical Search Spaces* (on hold, April 2026).

---

### Currently working on

- Expanding multi-GPU benchmark results for the TBA deployment optimizer (H100, A100, RTX 5080, L4, T4)
- Waiting on D-Wave LaunchPad QPU access to complete the quantum annealing benchmark
- Coursework at UC Berkeley (CS 61C, concurrent with research)

---

### Research interests

**ML systems and deployment optimization** — How do you find the best inference configuration (backend, quantization, batch size) when most of the search space crashes or violates constraints? I built a two-phase optimizer (Thermal Budget Annealing → constrained TPE) that treats crashes as data and maps feasible regions before exploiting them.

**Quantum-classical benchmarking** — Fair comparisons between classical simulated annealing, D-Wave quantum annealing, and QAOA on IBM hardware. I design standardized solver interfaces and report negative results when the hypothesis doesn't hold.

**Agentic AI and applied CV** — LLM-powered tool-calling agents for domain-specific automation, and competition-grade object detection pipelines with ONNX inference and ensemble methods.

---

### Pinned repositories

[**Constrained-ML-Deployment**](https://github.com/Chrislysen/Constrained-ML-Deployment)
Research repo and paper for Thermal Budget Annealing (TBA). Crash-aware deployment optimization under hard latency/memory constraints. Two-phase TBA→TPE hybrid, DeployBench benchmark suite, 46 tests, results across 5 GPU types. Includes v1–v3 paper PDFs.

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

Python, PyTorch, ONNX Runtime, Optuna, Qiskit, D-Wave Ocean SDK, FastAPI, Docker

---

### Contact

UC Berkeley (exchange 2025–2026) · INN Norway (home institution)
