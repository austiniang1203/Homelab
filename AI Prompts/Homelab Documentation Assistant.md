## Homelab Documentation Assistant

I am building a documentation repository on GitHub for my homelab. 
I need help creating structured markdown documents for each folder 
in my repo. Here is my setup:

### Hardware
- **Server:** HP ProLiant DL380 Gen9
  - CPU: 24 vCPUs — Intel Xeon E5-2670 v3 @ 2.30GHz
  - RAM: 128GB DDR3 ECC
  - Storage (OS): 272GB HDD (2x 136GB HDD)
  - Networking: Dual NIC
  - Hypervisor: VMware ESXi 8 (Bare Metal)

- **NAS:** Synology DS220+
  - 4TB HDD (RAID 1)
  - 2TB cold storage / 2TB VMware iSCSI datastore

- **Router/Firewall:** Ubiquiti UDM Dream Machine Pro
- **Switch:** Ubiquiti USW-24-PoE
- **Access Point:** Ubiquiti U6-Pro

### Repo Folder Structure
- Docs/           → Notes, diagrams, learning references
- Infrastructure/ → VM configs, templates, ESXi settings
- Networking/     → Firewall rules, VLAN configs, DNS
- Automation/     → Ansible playbooks, scripts
- Security/       → Network security, IAM
- Monitoring/     → Prometheus, Grafana configs
- Services/       → Self-hosted app configs
- Labs/           → Structured lab exercises

### My Experience Level
- Overall homelab: [X]
- Linux CLI: [X]
- PowerShell: [X]
- VMware ESXi: [X]
- Networking: [X]
- Kubernetes: [X]

### My Ask
Help me create a [DOCUMENT NAME] for my [FOLDER NAME] folder. 
The document should be:
- Written in Markdown
- Practical and specific to my hardware
- Formatted so I can copy it directly into my repo
- Include placeholders where I need to fill in my own details

Just replace the last line with whatever document you want to work on first, for example:
- "Help me create a network-topology.md for my docs/ folder"
- "Help me create a vm-inventory.md for my infrastructure/ folder"
- "Help me create a lab-01-esxi-vm-provisioning.md for my labs/ folder"
