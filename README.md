# KubeTrouble — Interactive Kubernetes Troubleshooting Lab & Protocol Simulator

An interactive, 60 FPS Kubernetes troubleshooting simulation built on the **3-Mode Interactive Lab Triad** (`SIMULATION_DESIGN_PATTERN.md`).

## Quick Start

```bash
npm install
npm run dev       # Starts local dev server at http://localhost:5173
npm run test:sim  # Runs headless Node domain accuracy & Stress Mode benchmark suite
npm run build     # Type-checks (tsc -b) and builds production bundle + Web Worker
```

## Highlights

- **Mode `1` — Hands-On Troubleshooting Labs (15 Labs · 5 Chapters, Beginner → CKA Expert)**:
  Each lab boots a deterministic broken Kubernetes cluster on the live topology canvas, provides step-by-step Triage → Diagnose → Remediate guidance, embeds an interactive `kubectl` / `etcdctl` CLI shell (`T`), and **only accepts the lab once every logical & visual desired-state invariant passes**.
- **Mode `2` — Live Cluster Sandbox & Chaos Engine**:
  Scale RPS (`0–5,000 req/s`), scale replicas, add/remove/fail/cordon worker nodes, inject 7 production failure modes, or toggle **Heavy-Load Stress Test (`X`)** with **8 Worker Nodes + 240 Pods** (`~1.5ms` Worker tick, High-Density Pod Status Matrix, and windowed `VirtualizedList` tables).
- **Mode `3` — Hop-by-Hop Data Flow & Protocol Simulator**:
  9 deep packet & control-plane scenarios with Play/Pause/Step transport and a **Layered Wire / Frame / Kernel Dissector** (L3/L4/L7 headers, HTTP/2 Watch frames, etcd Raft WAL commits, Netfilter/IPVS `nf_conntrack` DNAT tuples, CNI eBPF drops, CoreDNS `ndots:5`, and CSI volume staging).
