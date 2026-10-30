<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:58A6FF&height=220&section=header&text=Anmol%20Yadav&fontSize=64&fontColor=FFFFFF&animation=fadeIn&fontAlignY=36&desc=Systems%20%E2%80%A2%20AI%20%E2%80%A2%20Open%20Source&descSize=20&descAlignY=58" width="100%" alt="Anmol Yadav header" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=24&duration=3000&pause=900&color=58A6FF&center=true&vCenter=true&width=720&height=50&lines=Hey%2C+I'm+Anmol+Yadav+%F0%9F%91%8B;I+build+things+under+the+hood.;Systems+%7C+AI+%7C+Open+Source;Curiosity+drives+the+build." alt="Typing introduction" />

<br/>

*I like understanding how things work, and then making them work better.*

<br/>

[![Portfolio](https://img.shields.io/badge/Portfolio-visit-1F6FEB?style=for-the-badge&logo=vercel&logoColor=white)](https://heyanmol.netlify.app/)
[![GitHub](https://img.shields.io/badge/GitHub-follow-161B22?style=for-the-badge&logo=github)](https://github.com/Annmool)
[![FinIntel](https://img.shields.io/badge/FinIntel-explore-161B22?style=for-the-badge&logo=googleanalytics&logoColor=58A6FF)](https://finintel.pages.dev/)
[![Email](https://img.shields.io/badge/Email-say%20hello-161B22?style=for-the-badge&logo=gmail&logoColor=EA4335)](mailto:aydv.tech@gmail.com)

<img src="https://komarev.com/ghpvc/?username=Annmool&label=Profile%20views&color=1F6FEB&style=flat-square" alt="Profile views" />
<img src="https://img.shields.io/github/followers/Annmool?label=Followers&style=flat-square&color=161B22&labelColor=0D1117&logo=github" alt="Followers" />

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:1F6FEB&height=2&section=header" width="100%" alt="divider" />

## 🧭 `whoami`

> Not particularly interested in stopping at *"it works."*
> I want to know **why** it works, **where** it breaks, **what** the bottleneck is, and whether I can build it better.

<table>
<tr>
<td width="50%" valign="top">

### ⚙️ Systems engineering
Performance, concurrency, networking, and what's happening beneath abstractions.

</td>
<td width="50%" valign="top">

### 🧠 AI & retrieval
Vector search, RAG, embeddings, and making information useful.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 📈 Quantitative computing
Simulations, portfolio optimisation, and the mathematics behind financial decisions.

</td>
<td width="50%" valign="top">

### 🌐 Open source
Reading real codebases, fixing things, and learning from systems built by others.

</td>
</tr>
</table>

**Currently interested in:** backend engineering · distributed systems · applied AI · and the engineering challenges that connect them.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:1F6FEB&height=2&section=header" width="100%" alt="divider" />

## 🛠️ `things i've built`

<details open>
<summary><b>⚡ VectorCore: search, built from the inside out</b></summary>

<br/>

A hands-on exploration of vector databases and retrieval systems. The goal: understand the machinery instead of treating it as a black box.

- Implemented **Flat, IVF/K-Means, HNSW, BM25, scalar quantisation, and PQ-ADC** components.
- Combined dense and sparse retrieval with reciprocal-rank fusion, reranking, and citation-grounded RAG.
- Replaced repeated NumPy array reconstruction with capacity-doubling buffers.
- Vectorised distance calculations and reduced redundant computation.

**How a query flows through it:**

```mermaid
flowchart LR
    Q([Query]) --> D[Dense retrieval<br/>Flat · IVF · HNSW]
    Q --> S[Sparse retrieval<br/>BM25]
    D --> F{{Reciprocal-rank fusion}}
    S --> F
    F --> R[Reranker]
    R --> G[Citation-grounded RAG]
    G --> A([Answer])

    style Q fill:#1F6FEB,stroke:#58A6FF,color:#fff
    style A fill:#1F6FEB,stroke:#58A6FF,color:#fff
    style F fill:#161B22,stroke:#58A6FF,color:#fff
```

**One benchmark, one useful lesson:**

| Metric | Before | After | Change |
|---|---:|---:|---:|
| Build time · 1,000 × 32D vectors | 43.35 s | 2.06 s | **~21× faster** ⚡ |
| Query latency | 8.05 ms | 1.21 ms | **~6.7× faster** ⚡ |

```text
Build time   before  ████████████████████████████████████████  43.35 s
             after   ██                                         2.06 s
```

<sub>Results are from this specific benchmark and depend on workload and configuration.</sub>

</details>

<details>
<summary><b>📊 FinIntel: quantitative finance meets systems engineering</b></summary>

<br/>

[![Explore FinIntel](https://img.shields.io/badge/Explore-FinIntel%20%E2%86%97-1F6FEB?style=for-the-badge)](https://finintel.pages.dev/)

A quantitative finance platform with a native C++ computation engine behind a web interface.

- **C++20 + OpenMP** for parallel Monte Carlo simulation.
- **Geometric Brownian Motion** for modelling asset-price paths.
- **Cholesky decomposition** for correlated random shocks.
- **VaR, CVaR, and maximum drawdown** for portfolio risk analysis.
- **Markowitz optimisation** and efficient-frontier exploration.
- React + Express.js + child-process IPC connecting the UI, API, and native engine.

**Architecture:**

```mermaid
flowchart LR
    UI[React UI] -->|HTTP| API[Express.js API]
    API -->|child-process IPC| ENG[C++20 engine<br/>OpenMP Monte Carlo]
    ENG -->|VaR · CVaR · drawdown<br/>efficient frontier| API
    API --> UI

    style UI fill:#161B22,stroke:#61DAFB,color:#fff
    style API fill:#161B22,stroke:#58A6FF,color:#fff
    style ENG fill:#1F6FEB,stroke:#58A6FF,color:#fff
```

A project about more than finance: numerical computing, process boundaries, performance, and the trade-offs involved in putting them together.

</details>

<details>
<summary><b>🔬 Q-RouteRL: quantum network routing research</b></summary>

<br/>

Exploring **reinforcement learning for constrained quantum network routing**, where routing decisions must account for more than just physical distance.

The research direction involves:

- Quantum-network modelling with distance, decoherence, and entanglement-swapping dynamics.
- Classical routing baselines for reproducible comparisons.
- A planned neuro-symbolic reinforcement-learning approach to constrained routing.

> **Current status:** The repository contains a simulator and classical routing baselines. A trained RL agent and variational quantum circuit are not yet implemented or evaluated.

</details>

<details>
<summary><b>🔐 Komms: peer-to-peer file sharing</b></summary>

<br/>

A desktop file-sharing project exploring networking, secure transfers, and responsive interfaces.

- TCP/UDP networking and chunked, multithreaded transfers.
- RSA-2048 encryption and SHA-256 integrity verification.
- PyQt6 thread-pool execution to keep the UI responsive.

</details>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:1F6FEB&height=2&section=header" width="100%" alt="divider" />

## 🌐 `open source`

I enjoy working in established codebases where the details matter.

**Ceph ecosystem**

| Contribution | What it does |
|---|---|
| [ceph-nvmeof #1726](https://github.com/ceph/ceph-nvmeof/pull/1726) | Structured certificate-validation logging and exception handling around gRPC channel setup |
| [teuthology #2102](https://github.com/ceph/teuthology/pull/2102) | Structured `failure_reason` schema |
| [Ceph #68173](https://github.com/ceph/ceph/pull/68173) | Contribution to the Ceph core repository |
| [Ceph #67803](https://github.com/ceph/ceph/pull/67803) | Contribution to the Ceph core repository |

> The interesting part of debugging isn't just finding the failure. It's making the next failure easier to understand.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:1F6FEB&height=2&section=header" width="100%" alt="divider" />

## 🧰 `my toolbox`

<div align="center">

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=cpp,py,js,react,nodejs,express,fastapi,numpy,git,linux&perline=10" alt="Tech stack icons" />
</a>

<br/><br/>

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

**Also exploring:** `HNSW` · `BM25` · `RAG` · `OpenMP` · `WebSockets` · `distributed systems` · `Monte Carlo methods` · `quantitative risk`

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0D1117,100:1F6FEB&height=2&section=header" width="100%" alt="divider" />

## 📈 `the github corner`

<div align="center">

<a href="https://github.com/Annmool">
  <img height="180" src="https://github-readme-stats.vercel.app/api?username=Annmool&show_icons=true&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=1F6FEB" alt="GitHub Stats" />
</a>
<a href="https://github.com/Annmool">
  <img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Annmool&layout=compact&theme=github_dark&hide_border=true&bg_color=0D1117&title_color=58A6FF" alt="Top Languages" />
</a>

<br/>

<img src="https://streak-stats.demolab.com/?user=Annmool&theme=github-dark-blue&hide_border=true" alt="GitHub Contribution Streak" />

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Annmool&theme=react-dark&hide_border=true&bg_color=0D1117&color=58A6FF&line=1F6FEB&point=FFFFFF&area=true&area_color=1F6FEB" alt="Contribution activity graph" width="95%" />

</div>

<!--
OPTIONAL: animated contribution snake.
1. Add .github/workflows/snake.yml using Platane/snk (github-contribution-grid-snake)
2. Let it run once so it creates the "output" branch
3. Uncomment the block below

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Annmool/Annmool/output/github-snake-dark.svg" />
    <img alt="Contribution snake" src="https://raw.githubusercontent.com/Annmool/Annmool/output/github-snake.svg" />
  </picture>
</div>
-->

<div align="center">

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=4000&pause=1200&color=58A6FF&center=true&vCenter=true&width=700&lines=always+building.+always+learning.;Understand+the+problem.;Question+the+abstraction.;Measure+the+result." alt="Closing tagline" />

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:58A6FF&height=140&section=footer&animation=twinkling" width="100%" alt="Animated footer" />

</div>
