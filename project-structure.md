
# 🧱 AzothSolver Project Structure

This document provides an overview of the core components that make up the AzothSolver system. Each component serves a distinct purpose in building a high-performance solver aligned with the CoW Protocol ecosystem.

---

## 📦 Components Overview

### 1. `documentation/`
Central hub for all technical references, including:

- `README.md`: Overview of the system and development roadmap.
- `architecture.md`: Rust-based system design and solver modules.
- `cow-protocol/`: CIP-related documentation and alignment notes.
- `benchmarking/`: Performance evaluation plans and scripts.
- `assets/documents/`: Whitepaper (PDF + Markdown version).

This repo is intended to help external reviewers, auditors, and protocol contributors understand the system’s architecture and rationale.

---

### 2. `website/`
Frontend landing page for AzothSolver, hosted at [azothsolver-web.vercel.app](https://azothsolver-web.vercel.app). Features:

- Clean, mobile-friendly design with an alchemy-inspired aesthetic.
- Pages: `index.html`, `roadmap.html`, `whitepaper.html`.
- Links to:
  - Whitepaper
  - Socials (X)
  - Project vision
- Static hosting via Vercel, Netlify, or GitHub Pages.
- Located at: [github.com/AzothSolver/azothsolver-web](https://github.com/AzothSolver/azothsolver-web)

---

### 3. `solver/` *(private or in progress)*
Rust-based core of AzothSolver. Implements:

- Auction ingestion (CoW Protocol format)
- Quote generation engine (pathfinding & order matching)
- Quote evaluation logic (objective scoring)
- Solution submission (driver interface, shadow mode)

Design emphasizes:
- Sub-5ms latency targets
- Modular plug-and-play strategies
- Real-time metrics (Prometheus-compatible)
- CoW CIP compatibility (e.g., CIP-67)

Once stabilized, this repo will be made public with:
- Build instructions
- Endpoint simulation scripts
- Sample auction data and mock runner

---

## 🧩 Integration Flow (High-Level)

```text
           ┌────────────┐
           │  Website   │
           └────┬───────┘
                │
                ▼
           ┌────────────┐
           │ Documentation
           └────┬───────┘
                │
                ▼
           ┌────────────┐
           │   Solver   │
           └────────────┘
````

* **Website** introduces the project.
* **Documentation** explains how it works.
* **Solver** delivers the core functionality.

---

## 🔄 Sync Strategy

| Task                    | Maintained In                     |
| ----------------------- | --------------------------------- |
| Project vision, roadmap | `website/`, `docs/roadmap.html`   |
| Technical deep dives    | `documentation/`                  |
| Source code + modules   | `solver/`                         |
| Deployment scripts      | Planned (`infra/` or CI pipeline) |

---

## 📬 Contact

* Email: [azothsolver@gmail.com](mailto:azothsolver@gmail.com)
* X: [@AzothSolver](https://x.com/AzothSolver)
* Live site: [azothsolver-web.vercel.app](https://azothsolver-web.vercel.app)

---

## 🧪 License

**License**: `NotYetDefined`
© AzothSolver, 2025 – Licensing policy pending public release of the solver.

