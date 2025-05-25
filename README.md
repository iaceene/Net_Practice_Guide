# 🌐 **Net Practice 42: Networking Fundamentals**  
*A comprehensive guide to the OSI model, TCP/IP, subnetting, and network devices.* 

[![NetPractice](https://img.shields.io/badge/NetPractice-42-blue?style=for-the-badge)](https://iaceene.github.io/42_Subjects/?subject=NetPractice)


---

## 📌 **Table of Contents**  
1. [OSI Model](#-the-osi-model)  
2. [TCP vs UDP](#-tcp-vs-udp-key-differences)  
3. [IP Addresses & Subnet Masks](#-ip-addresses--subnet-masks)  
4. [Network Devices](#-network-devices-explained)  
5. [How Data Travels](#-how-data-travels-across-networks)  

---

## 🧩 **The OSI Model**  
The **OSI (Open Systems Interconnection) Model** is a 7-layer framework for network communication.  

### **7 Layers Overview**  
| Layer | Name             | Key Function                          | Example Protocols       |  
|-------|------------------|---------------------------------------|-------------------------|  
| **7** | Application      | User interfaces (HTTP, FTP, DNS)      | `HTTP`, `SMTP`, `FTP`   |  
| **6** | Presentation     | Data translation (encryption, compression) | `SSL/TLS`, `JPEG` |  
| **5** | Session          | Manages connections                   | `NetBIOS`, `RPC`        |  
| **4** | Transport        | Reliable data delivery (TCP/UDP)      | `TCP`, `UDP`            |  
| **3** | Network          | Routing & logical addressing (IP)     | `IP`, `ICMP`, `OSPF`    |  
| **2** | Data Link        | Frame forwarding (MAC addresses)      | `Ethernet`, `ARP`       |  
| **1** | Physical         | Raw bit transmission (cables, Wi-Fi)  | `Fiber`, `Wi-Fi`, `Hub` |  

### **Key Concepts**  
- **Encapsulation**: Data moves down layers (adding headers) and up (removing headers).  
- **Mnemonic**:  
  - *"All People Seem To Need Data Processing"* (Top → Bottom)  
  - *"Please Do Not Throw Sausage Pizza Away"* (Bottom → Top)  

---

## 🔄 **TCP vs UDP: Key Differences**  

| Feature          | TCP (Transmission Control Protocol)       | UDP (User Datagram Protocol)       |  
|------------------|-------------------------------------------|------------------------------------|  
| **Connection**   | Connection-oriented (handshake)           | Connectionless                    |  
| **Reliability**  | Guaranteed delivery (retransmits lost data)| No delivery guarantees            |  
| **Speed**        | Slower (overhead for reliability)         | Faster (low overhead)             |  
| **Use Cases**    | Web browsing, email, file transfers       | Streaming, gaming, VoIP           |  

---

## 🔢 **IP Addresses & Subnet Masks**  

### **IPv4 Address Structure**  
- **Example**: `192.168.1.10`  
- **Subnet Mask**: `255.255.255.0` → `/24` in CIDR.  
  - **Network Part**: `192.168.1` (first 24 bits).  
  - **Host Part**: `.10` (unique to the device).  

### **How Subnetting Works**  
- A subnet mask divides an IP into **network** and **host** portions.  
- Devices use it to determine if an IP is **local** (directly reachable) or **remote** (requires a router).  

**Example**:  
- If your IP is `192.168.1.10/24`, devices in `192.168.1.1–254` are local.  
- `8.8.8.8` (Google) is remote → traffic goes to the **router**.  

---

## 🖥 **Network Devices Explained**  

| Device   | Layer  | Function                                   | Example                     |  
|----------|--------|--------------------------------------------|-----------------------------|  
| **Switch** | L2     | Connects local devices (uses MAC addresses) | `Ethernet switch`          |  
| **Router** | L3     | Routes traffic between networks (uses IP)  | `Home Wi-Fi router`        |  
| **Hub**   | L1     | Broadcasts data to all ports (obsolete)    | `Legacy network hub`       |  

**Key Differences**:  
- **Switch**: Smart (forwards to specific devices).  
- **Router**: Connects LAN to WAN (internet).  
- **Hub**: Dumb (broadcasts to all).  

---

## 📡 **How Data Travels Across Networks**  

1. **Device Sends Data**:  
   - Checks subnet mask: Is the destination **local** or **remote**?  
2. **Local Traffic**:  
   - Switch forwards using **MAC addresses**.  
3. **Remote Traffic**:  
   - Router sends data to the **ISP** → internet.  
4. **TCP Ensures Reliability**:  
   - Breaks data into packets, numbers them, and retransmits if lost.  

**Diagram**:  
```
[Device] → [Switch] → [Router] → [Internet] → [Server]
```

---

## 💡 **Key Takeaways**  
- **OSI Model**: Standardizes network communication into 7 layers.  
- **TCP vs UDP**: Choose TCP for reliability, UDP for speed.  
- **Subnet Mask**: Defines network boundaries.  
- **Router vs Switch**: Routers connect networks; switches connect local devices.  

---

## 📚 **Further Reading**  
- [TCP/IP Illustrated (Book)](https://en.wikipedia.org/wiki/TCP/IP_Illustrated)  
- [Subnetting Practice](https://www.subnetting.net/)  

---
