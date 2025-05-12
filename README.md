# nmap-tool-basic-usage
A collection of Nmap commands, usage examples, and scanning techniques for cybersecurity learning and assessment.

🔍 Nmap Tool – Network Scanning & Security Auditing

📌 What is Nmap?

Nmap (Network Mapper) is an open-source tool used for:

* Network discovery
* Port scanning
* Operating system and service detection
* Vulnerability assessment

---

📁 Project Structure (Optional)

If you're uploading scan reports, demo scripts, or sample output, mention this:

```
/nmap-commands
   ├── basic_scans.md
   ├── advanced_scans.md
   └── reports/
```

---

🛠️ Common Nmap Commands

✅ **Basic Scanning**

```bash
nmap <IP>                    # Scan a single host
nmap 192.168.1.1-20          # Scan a range of IPs
nmap -p- 192.168.1.10        # Scan all 65535 ports
```

🔐 **Service & OS Detection**

```bash
nmap -sV 192.168.1.10        # Detect service versions
nmap -O 192.168.1.10         # Detect operating system
nmap -A 192.168.1.10         # Aggressive scan (OS + version + scripts + traceroute)
```

🔁 **Port Scanning Variations**

```bash
nmap -p 80 192.168.1.10                # Scan one port
nmap -p 22,80,443 192.168.1.10         # Scan multiple ports
nmap -p 1-1000 192.168.1.10            # Scan port range
```

📡 **Protocol Scanning**

```bash
nmap -sS 192.168.1.10        # TCP SYN Scan (stealthy)
nmap -sT 192.168.1.10        # TCP Connect Scan
nmap -sU -p 53 192.168.1.10  # UDP Scan on port 53
```

⏱️ **Timing Options**

```bash
nmap -T4 192.168.1.10        # Fast scan
nmap -T0 192.168.1.10        # Very slow, stealthy
```

---

📜 Nmap Scripting Engine (NSE)

```bash
nmap --script vuln 192.168.1.10        # Run all vulnerability scripts
nmap --script http-title 192.168.1.10  # Get the web page title
```

📂 Script Location (Linux):
`/usr/share/nmap/scripts/`

To update the script database:

```bash
sudo nmap --script-updatedb
```

---

📈 Sample Use Case

Use `netdiscover` and `ping` to identify live hosts, then scan them with Nmap for vulnerabilities.

---

🧠 Note:

Some scans (like `-sS`, `-A`) require **sudo/root access**. Use responsibly and only on **authorized networks**.

---

🤝 Credits

* Tool: [Nmap Official Site](https://nmap.org)
* Created by: M. Madhan Mohan Naidu
* Project: Nmap PPT Presentation & Tool Exploration
