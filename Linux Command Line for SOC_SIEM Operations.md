## Overview
This document includes commonly used Linux commands that are important for Security Operations Center (SOC) and SIEM tasks such as log analysis, monitoring, and incident response.

--------------------------------------------------

## 1. File & Directory Management

### ls
Purpose: List files and directories  
Example:
ls -la 
Explanation: Shows all files including hidden ones in detailed format  
![[ls.png]]

---

### cd
Purpose: Change directory  
Example:
cd /var/log  
Explanation: Move into log directory  
![[cd.png]]
---

### cp
Purpose: Copy files  
Example:
cp auth.log backup_auth.log  
![[cp.png]]
---

### mv
Purpose: Move or rename files  
Example:
mv old.log new.log  
![[mv.png]]

---

### rm
Purpose: Remove files  
Example:
rm suspicious_file.sh  
Note: Use carefully in investigations  
![[rm.png]]

--------------------------------------------------

## 2. File Viewing & Log Analysis

### cat
Purpose: Display file content  
Example:
cat /var/log/syslog  
Screenshot: (Add here)

---

### less
Purpose: View large files interactively  
Example:
less /var/log/auth.log  
Tip: Press / to search inside file  
Screenshot: (Add here)

---

### head / tail
Purpose: View beginning or end of file  
Example:
head -n 20 auth.log  
tail -f auth.log  
Explanation: tail -f is used for real-time log monitoring  
Screenshot: (Add here)

---

### grep
Purpose: Search for specific patterns  
Example:
grep "failed" /var/log/auth.log  
Advanced:
grep -i "error" syslog  
Explanation: -i ignores case  
Screenshot: (Add here)

---

### awk
Purpose: Process and extract data  
Example:
awk '{print $1, $2, $3}' auth.log  
Use: Extract timestamp or fields  
Screenshot: (Add here)

---

### cut
Purpose: Extract columns  
Example:
cut -d ' ' -f1 auth.log  
Screenshot: (Add here)

--------------------------------------------------

## 3. Process & System Monitoring

### ps
Purpose: Show running processes  
Example:
ps aux  
Screenshot: (Add here)

---

### top
Purpose: Real-time system monitoring  
Example:
top  
Screenshot: (Add here)

---

### htop
Purpose: Interactive process viewer  
Example:
htop  
Screenshot: (Add here)

---

### kill
Purpose: Stop a process  
Example:
kill -9 PID  
Screenshot: (Add here)

--------------------------------------------------

## 4. Networking Commands

### ip
Purpose: Show network interfaces  
Example:
ip a  
Screenshot: (Add here)

---

### netstat
Purpose: Show network connections  
Example:
netstat -tulnp  
Explanation:
t = TCP  
u = UDP  
l = listening  
n = numeric  
p = process  
Screenshot: (Add here)

---

### ss
Purpose: Modern netstat replacement  
Example:
ss -tuln  
Screenshot: (Add here)

---

### ping
Purpose: Check connectivity  
Example:
ping google.com  
Screenshot: (Add here)

---

### curl
Purpose: Send web requests  
Example:
curl http://example.com  
Screenshot: (Add here)

--------------------------------------------------

## 5. User & Permissions

### whoami
Purpose: Show current user  
Example:
whoami  
Screenshot: (Add here)

---

### chmod
Purpose: Change file permissions  
Example:
chmod 755 script.sh  
Screenshot: (Add here)

---

### chown
Purpose: Change ownership  
Example:
chown user:user file.txt  
Screenshot: (Add here)

--------------------------------------------------

## 6. Disk & System Info

### df
Purpose: Check disk space  
Example:
df -h  
Screenshot: (Add here)

---

### du
Purpose: Check directory size  
Example:
du -sh /var/log  
Screenshot: (Add here)

---

### uname
Purpose: System information  
Example:
uname -a  
Screenshot: (Add here)

--------------------------------------------------

## 7. Security & Log Commands

### journalctl
Purpose: View system logs  
Example:
journalctl -xe  
Screenshot: (Add here)

---

### last
Purpose: Show login history  
Example:
last  
Use: Detect suspicious login activity  
Screenshot: (Add here)

---

### history
Purpose: Show command history  
Example:
history  
Use: Track user activity  
Screenshot: (Add here)

---

### find
Purpose: Search files  
Example:
find / -name "*.log"  
Screenshot: (Add here)

--------------------------------------------------

## Conclusion
These commands are essential for SOC and SIEM tasks including monitoring, log analysis, and incident investigation. Practice them regularly in a lab environment.

--------------------------------------------------