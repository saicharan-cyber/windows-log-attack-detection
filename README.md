# 🖥 Windows Log Attack Detection Project

## 📖 Objective
Analyze Windows Security logs to detect suspicious activity and potential compromise.

---

## 🔎 Event IDs Monitored

- 4624 – Successful Logon
- 4625 – Failed Logon
- 4688 – Process Creation
- 4720 – User Account Creation
- 4104 – PowerShell Script Logging

---

## 🔍 Suspicious Process Detection

index=wineventlog EventCode=4688
| search CommandLine="*powershell*"
| search CommandLine="*enc*"

---

## 🔐 Admin Account Creation Detection

index=wineventlog EventCode=4720

---

## 🎯 MITRE ATT&CK Mapping

T1059 – Command and Scripting Interpreter  
T1136 – Create Account  

---

## 📌 Investigation Steps
1. Identify suspicious user
2. Check logon source
3. Validate process execution
4. Confirm lateral movement

---

## 📈 Learning Outcome
Improved log analysis capability and threat detection accuracy.
