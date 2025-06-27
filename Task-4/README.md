
# 🔒 Task 4: Configure and Use Windows Firewall

## 🎯 Objective:
To configure and test basic firewall rules on a Windows system. This includes blocking traffic on Telnet port 23 and allowing traffic on SSH port 22 using Windows Defender Firewall with Advanced Security.

---

## 📷 Step-by-Step Guide with Screenshots

 ✅ Step 1: Open Windows Firewall
- Press `Win + R`, type `wf.msc`, and press Enter.
- This opens Windows Defender Firewall with Advanced Security.

 ✅ Step 2: Open Inbound Rules
- Select Inbound Rules on the left panel.
- Click New Rule on the right to create a new inbound rule.

 ✅ Step 3: Choose Port Rule
- In the New Rule Wizard, select Port.
- Click Next.

 ✅ Step 4: Block Telnet (Port 23)
- Choose TCP, and select Specific local ports.
- Enter port `23`, then click Next.
- Select Block the connection.
- Continue through the wizard and name the rule ( "Block Telnet Port 23").

 ✅ Step 5: Allow SSH (Port 22)
- Repeat the same steps, but:
  - Use port `22`.
  - Select Allow the connection.
  - Name it (e.g., "Allow SSH Port 22").

 ✅ Step 6: Test Rule – Telnet Blocked
- Open Command Prompt and type:
  
  telnet 127.0.0.1 23
  
- Expected output:
  
  Could not open connection to the host, on port 23: Connect failed
  

 ✅ Step 7: Delete Test Rule
- Go back to Inbound Rules.
- Select the "Block Telnet Port 23" rule and click Delete to restore default settings.

---

## 🧠 Summary Table

| Action             | Port | Protocol | Rule Type | Result     |
|--------------------|------|----------|------------|------------|
| Block Telnet       | 23   | TCP      | Inbound    | Blocked    |
| Allow SSH          | 22   | TCP      | Inbound    | Allowed    |
| Telnet Test        | ✔️   | CLI      | Verified   | Connection failed |
| Rule Cleanup       | ✔️   | GUI      | Deleted    | Restored   |

---

## 💡 Tools Used:
- `wf.msc` (Windows Firewall GUI)
- Command Prompt
- Telnet Client

---

## ✅ Outcome:
This task demonstrates practical knowledge of:
- Creating and applying Windows Firewall rules.
- Controlling network traffic by port and protocol.
- Testing and verifying rule enforcement.
- Cleaning up configurations.

