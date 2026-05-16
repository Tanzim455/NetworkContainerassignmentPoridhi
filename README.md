
```
# Network Namespace Lab - Virtual Routed Network

A complete Bash script that automatically sets up a virtual network topology using **Linux Network Namespaces**, **Bridges**, **veth pairs**, and **NAT** for educational and testing purposes.

---

## 📖 Overview

This project simulates a real-world network environment with:
- Two isolated client namespaces (`ns1` & `ns2`)
- One router namespace (`router-ns`)
- Two internal LAN segments
- Internet access via NAT and IP forwarding

Perfect for learning Linux networking, routing, firewall (iptables), and network namespaces.

---

## 🚀 Features

- Full network isolation using namespaces
- Layer 2 bridging with `br0` and `br1`
- Router simulation with IP forwarding
- NAT (MASQUERADE) for internet access
- Proper routing between all networks
- DNS configured inside namespaces
- Interactive test menu
- Clean setup and teardown

---

## 🛠️ How to Use

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/NetworkContainerassignmentPoridhi.git
cd NetworkContainerassignmentPoridhi
```

### 2. Make Script Executable
```bash
chmod +x run.sh
```

### 3. Run the Script
```bash
sudo ./run.sh
```

After running, an interactive menu will appear:

```text
==============================================
       🌐 Network Namespace Test Menu 🌐      
==============================================
  1) Ping ns1  → ns2   (10.0.2.10)
  2) Ping ns2  → ns1   (10.0.1.10)
  3) Ping ns1  → Google (google.com)
  4) Ping ns2  → Google (google.com)
  5) Ping ns1  → Host  (10.99.99.1)
  6) Ping ns2  → Host  (10.99.99.1)
  7) Ping Host → ns1   (10.0.1.10)
  8) Ping Host → ns2   (10.0.2.10)
  9) 🚪 Exit and Cleanup
==============================================
```

---

## 🧪 Network Topology

| Namespace     | Interface   | IP Address       | Role                     |
|---------------|-------------|------------------|--------------------------|
| ns1           | veth1       | 10.0.1.10/24     | Client 1                 |
| ns2           | veth2       | 10.0.2.10/24     | Client 2                 |
| router-ns     | veth3       | 10.0.1.1/24      | Gateway for ns1          |
| router-ns     | veth4       | 10.0.2.1/24      | Gateway for ns2          |
| router-ns     | veth5       | 10.99.99.2/24    | Uplink to Host           |
| Host          | veth5host   | 10.99.99.1/24    | Internet Gateway         |

---

## 📋 Requirements

- Linux system with root access (`sudo`)
- `iproute2` package (usually pre-installed)
- `iptables`

---

## 🧹 Cleanup

The script automatically cleans up previous environments on every run.  
To manually stop everything, choose option **9** from the menu.

---

## 🎯 Use Cases

- Learning Linux networking concepts
- Testing routing and firewall rules
- Container networking experimentation
- Educational labs and assignments
- Troubleshooting network issues in isolation

---

## 📝 Author

**Tanzim Ibthesam**

---

## ⭐ Star this repo if you found it helpful!

Feel free to fork and extend it with DHCP, firewall policies, VPNs, or monitoring tools.
```