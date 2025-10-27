# 🧩 Wireshark Network Traffic Analysis

## 📘 Overview
This project demonstrates how to capture and analyze network packets using **Wireshark** on **Kali Linux**.  
The objective is to identify different network protocols, filter captured packets, and summarize the observed traffic.

---

## ⚙️ Steps Performed

### 1. Install Wireshark
```bash
sudo apt update
sudo apt install wireshark -y
```
> During installation, allow non-root users to capture packets if prompted.

### 2. Start Capturing Packets
- Open Wireshark from the applications menu or terminal:
  ```bash
  wireshark &
  ```
- Select your active network interface (e.g., `eth0`, `wlan0`) and click **Start Capturing**.

### 3. Generate Network Traffic
- Open a web browser and visit any website (e.g., `https://www.google.com`).
- Or use the ping command:
  ```bash
  ping -c 5 google.com
  ```

### 4. Stop the Capture
- Click the **Stop (Red Square)** button in Wireshark after ~1 minute.

### 5. Filter Captured Packets
Use display filters to focus on specific protocols:
- **HTTP:** `http`
- **DNS:** `dns`
- **TCP:** `tcp`
- **ICMP:** `icmp`

### 6. Identify Different Protocols
Analyze captured packets to identify at least **3 protocols**, such as:
- **DNS** – Domain name resolution queries  
- **TCP** – Data transport between hosts  
- **HTTP** – Web traffic  
- *(Optional)* **ICMP** – Ping messages

### 7. Export the Capture
- Go to **File → Export Specified Packets → PCAP File Format**  
- Save it as: `network_capture.pcap`

### 8. Summarize Findings
| Protocol | Function | Example Packet |
|-----------|-----------|----------------|
| **DNS** | Resolves domain names | Query for `www.google.com` |
| **TCP** | Establishes reliable connections | SYN, SYN-ACK, ACK |
| **HTTP** | Requests web pages | `GET / HTTP/1.1` |
| **ICMP** | Network diagnostics | Echo Request/Reply |

---

## 📁 Output Files
- `network_capture.pcap` – Packet capture file  
- `Wireshark_Summary_Report.docx` – Summary report of captured traffic  

---

## 🧠 Learning Outcome
- Learned how to use Wireshark for packet analysis.  
- Understood how multiple protocols operate together in network communication.  
- Gained insight into filtering and identifying protocol-based data.
---
