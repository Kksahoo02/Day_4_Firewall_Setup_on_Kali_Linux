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
