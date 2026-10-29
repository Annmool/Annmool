
<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3000&pause=900&color=58A6FF&center=true&vCenter=true&width=700&lines=Hey%2C+I'm+Anmol+Yadav+%F0%9F%91%8B;I+build+things+under+the+hood.;Systems+%7C+AI+%7C+Open+Source;Curiosity+drives+the+build." alt="Typing introduction" />

<br/>

*I like understanding how things work — and then making them work better.*

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-visit-161B22?style=flat-square&logo=vercel&logoColor=white)](https://heyanmol.netlify.app/)
[![GitHub](https://img.shields.io/badge/GitHub-follow-161B22?style=flat-square&logo=github)](https://github.com/Annmool)
[![FinIntel](https://img.shields.io/badge/FinIntel-explore-161B22?style=flat-square&logo=googleanalytics&logoColor=58A6FF)](https://finintel.pages.dev/)
[![Email](https://img.shields.io/badge/Email-say%20hello-161B22?style=flat-square&logo=gmail&logoColor=EA4335)](mailto:aydv.tech@gmail.com)

</div>

---

### `whoami`

Not particularly interested in stopping at *"it works."*

I want to know why it works, where it breaks, what the bottleneck is, and whether I can build it better.

I spend my time exploring the intersection of:

- ⚙️ **Systems engineering** — performance, concurrency, networking, and what's happening beneath abstractions.
- 🧠 **AI & retrieval** — vector search, RAG, embeddings, and making information useful.
- 📈 **Quantitative computing** — simulations, portfolio optimisation, and the mathematics behind financial decisions.
- 🌐 **Open source** — reading real codebases, fixing things, and learning from systems built by others.

Currently interested in backend engineering, distributed systems, applied AI, and the engineering challenges that connect them.

---

### `things i've built`

<details open>
<summary><b>⚡ VectorCore — search, built from the inside out</b></summary>

<br/>

A hands-on exploration of vector databases and retrieval systems. The goal: understand the machinery instead of treating it as a black box.

- Implemented **Flat, IVF/K-Means, HNSW, BM25, scalar quantisation, and PQ-ADC** components.
- Combined dense and sparse retrieval with reciprocal-rank fusion, reranking, and citation-grounded RAG.
- Replaced repeated NumPy array reconstruction with capacity-doubling buffers.
- Vectorised distance calculations and reduced redundant computation.

**One benchmark, one useful lesson:**

| Metric | Before | After |
|---|---:|---:|
| Build time · 1,000 × 32D vectors | 43.35 s | 2.06 s |
| Query latency | 8.05 ms | 1.21 ms |

<sub>Approximately 21× faster build time in this specific benchmark. Results depend on workload and configuration.</sub>

</details>

<details>
<summary><b>📊 FinIntel — quantitative finance meets systems engineering</b></summary>

<br/>

[Explore FinIntel ↗](https://finintel.pages.dev/)

A quantitative finance platform with a native C++ computation engine behind a web interface.

- **C++20 + OpenMP** for parallel Monte Carlo simulation.
- **Geometric Brownian Motion** for modelling asset-price paths.
- **Cholesky decomposition** for correlated random shocks.
- **VaR, CVaR, and maximum drawdown** for portfolio risk analysis.
- **Markowitz optimisation** and efficient-frontier exploration.
- React + Express.js + child-process IPC connecting the UI, API, and native engine.

A project about more than finance: numerical computing, process boundaries, performance, and the trade-offs involved in putting them together.

</details>

<details>
<summary><b>🔬 Q-RouteRL — quantum network routing research</b></summary>

<br/>

Exploring **reinforcement learning for constrained quantum network routing**, where routing decisions must account for more than just physical distance.

The research direction involves:

- Quantum-network modelling with distance, decoherence, and entanglement-swapping dynamics.
- Classical routing baselines for reproducible comparisons.
- A planned neuro-symbolic reinforcement-learning approach to constrained routing.

**Current status:** The repository contains a simulator and classical routing baselines. A trained RL agent and variational quantum circuit are not yet implemented or evaluated.

</details>

<details>
<summary><b>🔐 Komms — peer-to-peer file sharing</b></summary>

<br/>

A desktop file-sharing project exploring networking, secure transfers, and responsive interfaces.

- TCP/UDP networking and chunked, multithreaded transfers.
- RSA-2048 encryption and SHA-256 integrity verification.
- PyQt6 thread-pool execution to keep the UI responsive.

</details>

---

### `open source`

I enjoy working in established codebases where the details matter.

**Ceph ecosystem**

- [ceph-nvmeof #1726](https://github.com/ceph/ceph-nvmeof/pull/1726) — structured certificate-validation logging and exception handling around gRPC channel setup.
- [teuthology #2102](https://github.com/ceph/teuthology/pull/2102) — structured `failure_reason` schema.
- [Ceph #68173](https://github.com/ceph/ceph/pull/68173) · [Ceph #67803](https://github.com/ceph/ceph/pull/67803)

The interesting part of debugging isn't just finding the failure. It's making the next failure easier to understand.

---

### `my toolbox`

<div align="center">

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

**Also exploring:** HNSW · BM25 · RAG · OpenMP · WebSockets · distributed systems · Monte Carlo methods · quantitative risk

---


### `the github corner`

<div align="center">

<a href="https://github.com/Annmool">
  <img height="180" src="https://github-readme-stats.vercel.app/api?username=Annmool&show_icons=true&theme=github_dark&hide_border=true" alt="GitHub Stats" />
</a>
<a href="https://github.com/Annmool">
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Annmool&layout=compact&theme=github_dark&hide_border=true" alt="Top Languages" />
</a>

<br/>

<img src="https://streak-stats.demolab.com/?user=Annmool&theme=github-dark-blue&hide_border=true" alt="GitHub Contribution Streak" />

</div>


<div align="center">

### `always building. always learning.`

*Understand the problem. Question the abstraction. Measure the result.*

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:161B22,100:1F6FEB&height=100&section=footer" width="100%" alt="Decorative animated-style footer" />

</div>
