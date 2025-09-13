# ZWall – Next-Gen eBPF/XDP Firewall

ZWall is a modern, high-performance firewall and security platform built with **XDP, eBPF, and TC**.  
It provides low-latency, kernel-level packet filtering and advanced traffic control for **virtualization platforms (KVM, ESXi), Kubernetes clusters, and hosting environments**.

---

## ✨ Features

- **High-Performance Firewall** – Kernel-level filtering with XDP/eBPF.
- **Agent & Manager Architecture** – Centralized management with scalable agents.
- **Modern Web Panel** – Responsive UI for rule management and monitoring.
- **Advanced Security Rules**
  - Block/Allow IP, MAC, Ports, Protocols
  - Rate Limiting (ICMP, SYN, general traffic)
  - Port Scan Detection
  - DHCP Guard
  - Bandwidth Control & VM Isolation
- **Extensible Roadmap** – Traffic shaping, QoS, latency control, and more (future releases).

---

## 🏗️ Architecture

1. **Manager**  
   - Central controller with PostgreSQL database  
   - Web Panel for defining firewall rules  
   - Sends rules to agents  

2. **Agent**  
   - Runs on each host  
   - Attaches firewall logic (XDP/TC) to network interfaces  
   - Enforces rules in kernel space  

3. **Firewall Components**  
   - XDP/eBPF programs for high-speed packet filtering  
   - TC for egress control and advanced shaping  

---

## 🚀 Installation

> ⚠️ ZWall does **not use Docker**. All setup is native/manual.  
Complete installation guides are available in 👉 https://zwall.net/docs (see project website).

---

## 📊 Roadmap

- [x] Core firewall engine (XDP/eBPF)
- [x] Manager + Agent communication
- [x] Web Panel with rule management
- [ ] QoS / Traffic Shaping *(next release)*
- [ ] VM Bandwidth Quotas *(future release)*
- [ ] Kubernetes-native integration *(future roadmap)*

Full roadmap: [`ROADMAP_EN.md`](ROADMAP_EN.md)

---

## 🔒 Security

ZWall is designed with security-first principles:
- Kernel-level packet blocking
- Minimal userland exposure
- Configurable rules with strict validation  
See: [`Security-Analysis.md`](Security-Analysis.md)

---

## 📜 License

This project is licensed under the **Apache License 2.0** – see [LICENSE](LICENSE) for details.

---

## 🤝 Contributing

Contributions, feature requests, and issue reports are welcome!  
Please open a GitHub Issue or Pull Request.

---

## 📬 Contact

- Website: [zwall.net](https://zwall.net)  
- Email: support@zwall.net  

---

### Why ZWall?
Because next-generation firewalls need **performance, scalability, and flexibility** – and ZWall delivers all three.
