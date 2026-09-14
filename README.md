<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/ThreadCrash/ThreadCrash/main/assets/banner-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/ThreadCrash/ThreadCrash/main/assets/banner-light.svg">
  <img alt="ThreadCrash System Terminal" src="https://raw.githubusercontent.com/ThreadCrash/ThreadCrash/main/assets/banner-dark.svg" width="100%" />
</picture>

<p align="center">
  <b>Site Reliability Engineering</b> • <b>SecOps Runtime Defense</b> • <b>Kernel eBPF & NetOps</b> • <b>High-Performance C++20</b>
</p>

<p align="center">
  <a href="https://github.com/ThreadCrash?tab=repositories"><img src="https://img.shields.io/badge/Architecture-SRE%20%7C%20SecOps%20%7C%20NetOps-38bdf8?style=for-the-badge&logo=linux&logoColor=white" /></a>
  <a href="https://github.com/ThreadCrash/raytracing-from-scratch-cpp"><img src="https://img.shields.io/badge/Raytracer-C%2B%2B20%20BVH-f43f5e?style=for-the-badge&logo=c%2B%2B&logoColor=white" /></a>
  <a href="https://github.com/ThreadCrash/zero-trust-proxy"><img src="https://img.shields.io/badge/Zero--Trust-eBPF%20%7C%20mTLS%201.3-a855f7?style=for-the-badge&logo=go&logoColor=white" /></a>
</p>

</div>

---

### 🖥️ Core Focus & Engineering Philosophy

delusional systems & kernel hackerobsessed with zero-copy eBPF socket routing, Kubernetes cluster resilience, and building render engines from scratch.

- ⚡ **Kernel & NetOps:** eBPF / XDP socket redirection, WireGuard overlay mesh peering, low-level Linux network stack tuning.
- 🛡️ **SecOps & Zero-Trust:** Falco runtime behavioral detection, SPIFFE/SPIRE workload attestation, automated mTLS 1.3 certificate rotation.
- 📉 **SRE & Chaos Engineering:** Chaos mesh fault injection, error-budget burn rate alarms, sub-millisecond p99 SLO telemetry.
- 🎯 **Graphics & Systems:** Monte Carlo CPU raytracers built from first principles in modern C++20 with BVH spatial acceleration.

---

### 🛠️ Technology Stack

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=cpp,c,go,rust,linux,kubernetes,docker,python,bash,prometheus,grafana,git,terraform&perline=13" />
  </a>
</p>

| Category | Technologies & Tooling |
| :--- | :--- |
| **Languages** | C++20, Go 1.22, Rust, Python 3.12, Bash, x86-64 Assembly |
| **Kernel & Networking** | Linux eBPF (XDP, sockmap), WireGuard, Envoy, Netfilter, TCP/IP, mTLS 1.3 |
| **Cloud & SRE** | Kubernetes, Docker, Helm, ArgoCD, Chaos Mesh, Prometheus, OpenTelemetry, Grafana |
| **Security (SecOps)** | Falco, SPIFFE / SPIRE, Vault, OPA (Open Policy Agent), Cosign, Trivy |

---

### 🚀 Featured Repositories

| Repository | Focus | Tech Stack | Highlights |
| :--- | :--- | :--- | :--- |
| [**raytracing-from-scratch-cpp**](https://github.com/ThreadCrash/raytracing-from-scratch-cpp) | Graphics / Engines | `C++20`, `AVX2`, `CMake` | Multithreaded Monte Carlo path tracer with BVH slab acceleration & glass refraction. |
| [**zero-trust-proxy**](https://github.com/ThreadCrash/zero-trust-proxy) | SecOps / NetOps | `Go`, `eBPF`, `SPIFFE` | L7 reverse proxy featuring kernel sockmap bypass and automated mTLS 1.3 enforcement. |
| [**sre-probe-toolkit**](https://github.com/ThreadCrash/sre-probe-toolkit) | SRE / Diagnostics | `eBPF`, `Kernel`, `C` | Open-source SRE latency diagnostics, socket ring buffers, and trace telemetry. |
| [**chaos-mesh-operator**](https://github.com/ThreadCrash/chaos-mesh-operator) | SRE / Resilience | `Kubernetes`, `Go` | Kubernetes operator injecting network latency, packet corruption, and DNS jitter. |
| [**falco-threat-rules**](https://github.com/ThreadCrash/falco-threat-rules) | SecOps / Detection | `Falco`, `YAML`, `SecOps` | Production container runtime threat detection rules mapped to MITRE ATT&CK. |

---

### 📊 Telemetry & Diagnostics

```
┌──[ThreadCrash@telemetry-daemon]──[~/benchmarks]
└──$ ./run-benchmarks.sh --all
  [+] RayTracer throughput:   2.64M rays/sec (16 cores, AVX2 SIMD enabled)
  [+] eBPF sockmap bypass:    48.2% drop in packet round-trip latency
  [+] Resilience operator:    Zero-downtime recovery during 15% packet drop injection
  [+] Total Private Commits:  13,400+ commits across eBPF, K8s, and SecOps repositories
```

---

<div align="center">
  <sub>Configured & maintained by <a href="https://github.com/ThreadCrash">@ThreadCrash</a>. 100% pure SRE, SecOps, NetOps & Systems.</sub>
</div>
