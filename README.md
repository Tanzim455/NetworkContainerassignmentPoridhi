

```
# NetworkContainerassignmentPoridhi

A bash script to automatically create a virtual routed network topology using Linux Network Namespaces, Bridges, and NAT.

## 🚀 How to Run

**1. Grant permissions:**
```bash
chmod +x run.sh
```

**2. Run the `run.sh` file:**
```bash
sudo ./run.sh
```

**3. From the several options, select one to test connectivity:**
```text
==============================================
       🌐 Network Namespace Test Menu 🌐      
==============================================
  1) Ping ns1  -> ns2   (10.0.2.10)
  2) Ping ns2  -> ns1   (10.0.1.10)
  3) Ping ns1  -> Google (google.com)
  4) Ping ns2  -> Google (google.com)
  5) Ping ns1  -> Host  (10.99.99.1)
  6) Ping ns2  -> Host  (10.99.99.1)
  7) Ping Host -> ns1   (10.0.1.10)
  8) Ping Host -> ns2   (10.0.2.10)
  9) 🚪 Exit and Cleanup
==============================================

Select an option [1-9]: 
```

   
