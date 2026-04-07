# k8scout

**Kubernetes attack path intelligence for security teams.**

k8scout is an open-source attack path engine for authorized Kubernetes security assessments. Drop a single binary into a compromised pod, and get a complete map of every realistic escalation path — from your exact foothold to cluster-admin, node takeover, secret theft, and cloud IAM roles.

---

## What we build

| | |
|---|---|
| **[k8scout](https://github.com/k8scout/k8scout)** | Single-binary Kubernetes attack path engine — RBAC graph analysis, Dijkstra-based pathfinding, MITRE ATT&CK mapping, and an interactive attack graph visualizer |

---

## How it works

k8scout builds a weighted permission graph from your foothold and finds the cheapest (most realistic) multi-hop attack chains across:

- Pod → cluster-admin via RBAC mutation or workload patching
- Container escape → node via privileged containers, hostPID, hostPath
- Lateral movement via exec and SA token theft
- Cloud IAM escalation (AWS IRSA, GKE Workload Identity, Azure WI)
- Impersonation chains and webhook injection

---

## Team

| | |
|---|---|
| **[hac01](https://github.com/hac01)** | Co-creator & maintainer |
| **[Tomlmmrs](https://github.com/Tomlmmrs)** | Co-creator & maintainer |

---

> **Intended use**: Penetration testing engagements, red team operations, internal security reviews, and cluster hardening audits. Always obtain proper authorization before running against any cluster.
