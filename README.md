# 🌐 Day_4_Firewall_Setup_on_Kali_Linux 🔥

## ✅ Steps Performed
1️⃣ Checked firewall status 🛡️  
2️⃣ Listed existing firewall rules 📜  
3️⃣ Blocked Telnet (Port 23) 🚫🔌  
4️⃣ Verified block by testing connection 🧪  
5️⃣ Allowed SSH (Port 22) 🔑  
6️⃣ Removed test rule and restored firewall ♻️  

---

## 💻 Commands Used (Linux - UFW)
```bash
sudo ufw status        # check firewall status
sudo ufw deny 23       # block Telnet (port 23)
sudo ufw allow 22      # allow SSH (port 22)
sudo ufw delete deny 23  # remove the Telnet block
```
## 🔎 How Firewall Filters Traffic  

A firewall filters traffic based on these criteria:  

### 🗺️ Source IP / Destination IP  
- Example: Only allow traffic from a trusted IP.  

### 🔌 Port Numbers  
- Example: Allow `80` (HTTP) and `443` (HTTPS), block `23` (Telnet).  

### 📡 Protocol  
- Example: TCP, UDP, ICMP (ping).  

### ↔️ Direction  
- **Inbound** → Traffic coming into your system (e.g., a web request).  
- **Outbound** → Traffic going out (e.g., you visiting a website).  

### 🔄 State Tracking (if Stateful Firewall)  
- Remembers active connections and only allows return traffic that matches.  

---

## 🧠 Example  
**Rule:** “Block inbound traffic on port 23”  

- When a packet arrives with **destination port 23**, the firewall checks the rule.  
- Since Telnet is insecure, the firewall 🚫 drops it.  
- All other allowed ports (like SSH `22`) continue working.  

---

## 🔍 Types of Filtering  
- **Stateless firewall** → Checks each packet individually against rules.  
- **Stateful firewall** → Tracks active sessions, only allows return traffic that matches.  

---

## 🎯 Outcome  
By filtering this way, a firewall:  
- Prevents **unauthorized access** 🚫  
- Blocks **insecure/unused services** 🔒  
- Reduces **attack surface** ⚔️  
