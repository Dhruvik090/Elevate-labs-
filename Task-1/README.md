# Cyber Security Internship - Task 1: Local Network Port Scan

## 🔍 Objective
To perform a local network port scan using Nmap and understand the devices and services running within my LAN.

## 🖥️ My Local IP Address
```
192.168.52.1
```

## 🛠 Tools Used
- OS: Kali Linux
- Tool: Nmap 7.94
- Command Used:
```bash
sudo nmap -sS 192.168.52.0/24
```

## 📊 Scan Summary

| IP Address       | Open Ports         | Services                  | Notes                           |
|------------------|--------------------|---------------------------|----------------------------------|
| 192.168.52.1     | 135, 139, 445, 3306 | MSRPC, NetBIOS, SMB, MySQL | Your Windows machine            |
| 192.168.52.19    | 5060               | SIP                       | VoIP or softphone device        |
| 192.168.52.144   | 3306, 5800, 5900   | MySQL, VNC                | Remote desktop & database host  |
| 192.168.52.187   | 53                 | DNS                       | DNS or router device            |
| 192.168.52.253   | (All filtered)     | —                         | Likely firewall or printer      |
| 192.168.52.254   | 5060               | SIP                       | VoIP device                     |

## 🔐 Risk Analysis
- **Common Ports Found**: SSH, HTTP, MySQL, VNC, SMB.
- **Security Concerns**:
  - Exposed ports could allow unauthorized access.
  - Services like VNC, FTP, MySQL, and SMB can be exploited if not secured.
- **Best Practices**:
  - Disable unused ports/services.
  - Use firewalls.
  - Keep software up to date.

## 📁 Files Included
- `scan_results.txt`: Nmap scan output
- `README.md`: Task explanation and analysis

## 🎯 Outcome
- Learned how to find my IP and local subnet.
- Performed Nmap scan to identify devices and services.
- Understood the security risks associated with open ports.
