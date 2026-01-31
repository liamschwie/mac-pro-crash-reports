### **The Problem**
Mac Pro froze due to a **"Loss of MMIO space"** kernel panic. This was caused by the **ADATA SX8200PNP** NVMe drive losing communication with macOS during power management transitions.

---

### **The Fixes**

#### **1. Disabled System & Disk Sleep**
Used Terminal to force the Mac to stay fully awake and keep the SSD powered on at all times by running the following commands.

```bash
sudo pmset -a sleep 0
sudo pmset -a disksleep 0
sudo pmset -a standby 0
sudo pmset -a autopoweroff 0
