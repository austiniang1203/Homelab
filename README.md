# 🏠 Homelab

> A personal infrastructure lab for learning, experimenting, and self-hosting — built on virtualization.

---

## 📋 Overview

This repository documents my homelab environment — including infrastructure configs, automation scripts, lab exercises, and notes. It serves as both a reference for myself and a learning journal for all things technology.

---

## 🖥️ Hardware

### Server
| Component | Details |
|-----------|---------|
| Model | HP ProLiant DL380 Gen9 |
| CPU | 24 vCPUs — Intel Xeon E5-2670 v3 @ 2.30GHz |
| RAM | 128GB DDR3 ECC |
| Storage (OS) | 272GB HDD (2x 136GB HDD) |
| Storage (VM) | 2TB iSCSI datastore via Synology DS220+ |
| Networking | Dual NIC |
| Hypervisor | VMware ESXi 8 (Bare Metal) |

### Network Attached Storage (NAS)
| Component | Details |
|-----------|---------|
| Model | Synology DS220+ |
| Storage | 4TB HDD (RAID 1) |
| Allocation | 2TB cold storage / 2TB VMware datastore via iSCSI |

### Networking
| Device | Model | Role |
|--------|-------|------|
| Router/Firewall | Ubiquiti UniFi Dream Machine Pro | Routing, firewall, IDS/IPS |
| Switch | Ubiquiti USW-24-PoE | Core switching, PoE |
| Access Point | Ubiquiti U6-Pro | WiFi 6 wireless |

---

## 🗂️ Repository Structure

```
homelab/
├── docs/               # Notes, diagrams, and learning references
├── infrastructure/     # VM configs, templates, ESXi settings
├── networking/         # Firewall rules, VLAN configs, DNS settings
├── automation/         # PowerShell scripts, bash/Python scripts
├── security/           # Network security, IAM
├── monitoring/         # Prometheus, Grafana, alerting configs
├── services/           # Self-hosted app configs
└── labs/               # Structured lab exercises and walkthroughs
```

---

## 🧱 Current Stack

### Virtualization
- **Hypervisor:** VMware ESXi 8 (Bare Metal)
- **VM Datastore:** Synology DS220+ via iSCSI

### Networking
- **Router/Firewall:** Ubiquiti UDM Pro
- **DNS:** Pi-hole
- **VPN:** WireGuard

### Orchestration & Automation
- **Container Orchestration:** _e.g., k3s (planned)_
- **Automation:** _e.g., Ansible (planned)_

### Monitoring
- **Metrics:** _e.g., Prometheus + Node Exporter (planned)_
- **Dashboards:** _e.g., Grafana (planned)_

### Self-Hosted Services
| Service | Purpose | Status |
|---------|---------|--------|
| Game servers | Host game server for myself and friends to play on | Complete |

---

## 🗺️ Network Topology

```
Internet
   │
[UDM Dream Machine Pro]
   │
[USW-24-PoE Switch]
   ├── HP ProLiant DL380 Gen9 (ESXi 8)
   │     └── iSCSI ──► Synology DS220+
   ├── Synology DS220+ (NAS)
   ├── U6-Pro (Access Point)
   └── [Other LAN Devices]
```

> 📌 VLANs and further segmentation to be added as the lab evolves.

---

## 🧪 Labs & Learning Goals

Structured labs I'm working through, organized by topic:

- [ ] **VMware ESXi** — VM provisioning, snapshots, templates
- [ ] **Storage** — iSCSI configuration, datastore management
- [ ] **Networking** — VLAN segmentation, firewall rules, UniFi management
- [ ] **Kubernetes** — Deploy k3s, practice kubectl, set up ingress
- [ ] **Automation** — Ansible playbooks for VM provisioning
- [ ] **Monitoring** — Full Prometheus + Grafana observability stack
- [ ] **Security** — Hardening, network scanning, IDS/IPS tuning

---

## 🚀 Getting Started

> For anyone (including future me) replicating this setup.

### Prerequisites
- VMware ESXi 8 installed on bare metal
- Synology DS220+ configured with iSCSI LUN
- SSH access to the ESXi host
- UniFi Network app access for network management

### Quick Start
```bash
# Clone this repo
git clone https://github.com/austiniang1203/homelab.git
cd homelab
```

---

## 📓 Changelog / Journal

| Date | Entry |
|------|-------|
| 2026-04-18 | Initialized repo, documented hardware |
| | |

---

## 📚 Resources

- [VMware ESXi Documentation](https://docs.vmware.com/en/VMware-vSphere/index.html)
- [Ubiquiti UniFi Documentation](https://help.ui.com)
- [Synology Knowledge Base](https://kb.synology.com)
- [r/homelab](https://reddit.com/r/homelab)
- [awesome-selfhosted](https://github.com/awesome-selfhosted/awesome-selfhosted)
- [TechnoTim YouTube](https://www.youtube.com/@TechnoTim)

---

## ⚠️ Security Note

This repo contains **no secrets, passwords, API keys, or private IPs**. Sensitive values are managed via environment variables or a secrets manager and are never committed.

---

## 📄 License

MIT — use freely, learn openly.
