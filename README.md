<div align="center">

```
 ██████╗██╗   ██╗██████╗ ███████╗██████╗      ██████╗██╗  ██╗███████╗ ██████╗██╗  ██╗██╗     ██╗███████╗████████╗
██╔════╝╚██╗ ██╔╝██╔══██╗██╔════╝██╔══██╗    ██╔════╝██║  ██║██╔════╝██╔════╝██║ ██╔╝██║     ██║██╔════╝╚══██╔══╝
██║      ╚████╔╝ ██████╔╝█████╗  ██████╔╝    ██║     ███████║█████╗  ██║     █████╔╝ ██║     ██║███████╗   ██║   
██║       ╚██╔╝  ██╔══██╗██╔══╝  ██╔══██╗    ██║     ██╔══██║██╔══╝  ██║     ██╔═██╗ ██║     ██║╚════██║   ██║   
╚██████╗   ██║   ██████╔╝███████╗██║  ██║    ╚██████╗██║  ██║███████╗╚██████╗██║  ██╗███████╗██║███████║   ██║   
 ╚═════╝   ╚═╝   ╚═════╝ ╚══════╝╚═╝  ╚═╝     ╚═════╝╚═╝  ╚═╝╚══════╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═╝╚══════╝   ╚═╝
```

# 🛡️ Cyber_Security_Checklist

**Comprehensive offensive security checklists for authorized penetration testing and OSINT investigations.**

![Maintained](https://img.shields.io/badge/Maintained-Yes-00e676?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-00e5ff?style=flat-square)
![Tools](https://img.shields.io/badge/Type-Offensive%20Security-ff4081?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-557c94?style=flat-square)
![Author](https://img.shields.io/badge/Author-Prathiv--Raj-b388ff?style=flat-square)

[![TryHackMe](https://img.shields.io/badge/TryHackMe-PrathivRaj-red?style=flat-square&logo=tryhackme)](https://tryhackme.com/p/PrathivRaj)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-cyberbot007-9fef00?style=flat-square&logo=hackthebox&logoColor=9fef00&labelColor=141d2b)](https://app.hackthebox.com/profile/cyberbot007)
[![GitHub](https://img.shields.io/badge/GitHub-Prathiv--Raj-181717?style=flat-square&logo=github)](https://github.com/Prathiv-Raj)

</div>

---

## 📁 Repository Structure

```
Cyber_Security_Checklist/
├── 📄 index.html                   ← Main Hub (links to all checklists)
├── 📄 README.md
├── 🌐 pentest_checklist.html       ← Web App Pentest Checklist (Pen Test)
└── 🔍 email_osint_checklist.html   ← Email OSINT Checklist
```

---

<br>

# 🌐 Web Application Pentest Checklist

> **Pen Test** — OWASP-aligned manual web application penetration testing checklist with 9 phases, 79 checks, and full methodology + command references per phase.

## Overview

| Property | Detail |
|---|---|
| **Total Checks** | 79 |
| **Phases** | 9 |
| **Critical Checks** | 54 |
| **Methodology** | OWASP Top 10 aligned |
| **Format** | Single-file HTML (offline capable) |

## Phases

```
01  Recon & Information Gathering        ████░░░░░░  0/10   Passive & active surface mapping
02  Scanning & Enumeration               ████░░░░░░  0/10   Port mapping, directory discovery, tech fingerprinting
03  Authentication & Session             ████░░░░░░  0/12   Login flows, JWT, session tokens, MFA
04  Authorization & Access Control       ████░░░░░░  0/8    IDOR, privilege escalation, path traversal
05  Input Validation & Injection         ████░░░░░░  0/12   SQLi, XSS, SSTI, SSRF, RCE, file upload
06  CORS, CSRF & Clickjacking            ████░░░░░░  0/5    Cross-origin attacks and request forgery
07  Business Logic                       ████░░░░░░  0/7    Workflow abuse, race conditions, price manipulation
08  Security Headers & Misconfig         ████░░░░░░  0/8    Headers, exposed files, cloud storage, debug interfaces
09  API-Specific Testing                 ████░░░░░░  0/7    REST, GraphQL, BOLA, versioning, rate limits
```

## Features

- ✅ **Checklist + Methodology tabs** per phase — tick checks, read step-by-step attack methodology
- ✅ **Syntax-highlighted commands** with one-click copy buttons
- ✅ **Severity badges** — CRIT / HIGH / MED / INFO per check
- ✅ **Live progress tracking** — overall bar + per-phase progress, persisted in `localStorage`
- ✅ **Search** — filter checks across all phases instantly
- ✅ **Export Report** — generates a standalone HTML evidence report
- ✅ **Expand All / Collapse All / Reset** controls
- ✅ **Fully offline** — single `.html` file, no dependencies, no internet required

## Sample Checks

```
Phase 01 — Recon & Information Gathering
  [HIGH]  Subdomain enumeration via subfinder, amass, dnsx, crt.sh
  [HIGH]  Google dorks: site:, filetype:, inurl:, intitle:, ext:env
  [HIGH]  GitHub dorking for exposed secrets, configs, API keys
  [MED]   WHOIS lookup and DNS record enumeration (A, MX, TXT, CNAME, NS)
  [MED]   Shodan / Censys / FOFA passive asset discovery
  [INFO]  Technology fingerprinting with WhatWeb / Wappalyzer

Phase 05 — Input Validation & Injection
  [CRIT]  SQL injection (manual + sqlmap) on all input parameters
  [CRIT]  Stored & reflected XSS across all user-controlled inputs
  [HIGH]  Server-Side Template Injection (SSTI) testing
  [HIGH]  SSRF via URL parameters, webhooks, file imports
  [HIGH]  Remote Code Execution (RCE) via file upload, deserialization
```

## Usage

```bash
# Clone the repo
git clone https://github.com/Prathiv-Raj/Cyber_Security_Checklist.git
cd Cyber_Security_Checklist

# Open in browser (no server needed)
# Start from the main hub to access both checklists
xdg-open index.html                    # Linux (recommended)
open index.html                        # macOS (recommended)

# Or open specific checklists directly:
xdg-open pentest_checklist.html        # Linux
open pentest_checklist.html            # macOS
```

---

<br>

# 🔍 Email OSINT Checklist

> Passive recon methodology for email address investigation — 7 phases, 62 checks, full command references per phase. For authorized red team engagements, CTF OSINT challenges, and lawful research.

## Overview

| Property | Detail |
|---|---|
| **Total Checks** | 62 |
| **Phases** | 7 |
| **Critical Checks** | 12 |
| **Methodology** | Passive OSINT — no active enumeration of target |
| **Format** | Single-file HTML (offline capable) |

## Phases

```
01  Target Validation & Email Recon     ████░░░░░░  0/10   Verify email, SMTP probe, provider fingerprint
02  Account & Platform Discovery        ████░░░░░░  0/10   Holehe, Epieos, h8mail — 100+ platform check
03  Breach & Credential Exposure        ████░░░░░░  0/8    HIBP, DeHashed, Snusbase, LeakCheck
04  Domain & Infrastructure Intel       ████░░░░░░  0/10   WHOIS, DNS, SPF/DKIM/DMARC, Shodan
05  Google & Cloud Account OSINT        ████░░░░░░  0/8    GHunt — Gmail profile, Maps, YouTube, Calendar
06  Social Media & Identity Mapping     ████░░░░░░  0/9    Sherlock, dorks, GitHub, LinkedIn, cross-correlation
07  Paste Sites & Dark Web Exposure     ████░░░░░░  0/7    psbdmp, Pastebin, IntelligenceX, paste archiving
```

## Features

- ✅ **Checklist + Methodology tabs** per phase — with bash commands ready to copy
- ✅ **Target email input bar** — stored locally, referenced in command examples
- ✅ **Severity badges** — CRIT / HIGH / MED / INFO per check
- ✅ **Live progress tracking** — overall bar + per-phase progress, persisted in `localStorage`
- ✅ **Search** — filter checks across all phases
- ✅ **Export Report** — generates a standalone HTML investigation report
- ✅ **Fully offline** — single `.html` file, no server, no internet required

## Sample Checks & Commands

```
Phase 02 — Account & Platform Discovery
  [HIGH]  Run Holehe against target email
  [HIGH]  Epieos email lookup (Google + Gravatar pivot)
  [HIGH]  Check GitHub account registration
  [HIGH]  Run h8mail for cross-platform correlation

# Commands:
pip install holehe --break-system-packages
holehe target@domain.com --only-used | tee holehe_results.txt

pip install h8mail --break-system-packages
h8mail -t target@domain.com

Phase 05 — Google & Cloud Account OSINT
  [HIGH]  Confirm Gmail address with GHunt
  [HIGH]  Extract Google profile name and photo URL
  [HIGH]  Google Calendar public event exposure
  [MED]   Check linked YouTube channel

# Commands:
git clone https://github.com/mxrch/GHunt
cd GHunt && pip install -r requirements.txt --break-system-packages
python3 ghunt.py email target@gmail.com --json ghunt_output.json
```

## Usage

```bash
# Clone the repo
git clone https://github.com/Prathiv-Raj/Cyber_Security_Checklist.git
cd Cyber_Security_Checklist

# Open in browser (no server needed)
# Start from the main hub to access both checklists
xdg-open index.html                    # Linux (recommended)
open index.html                        # macOS (recommended)

# Or open specific checklists directly:
xdg-open email_osint_checklist.html   # Linux
open email_osint_checklist.html       # macOS
```

---

<br>

## 🛠️ Tool Arsenal Reference

### Web App Pentest Tools

| Tool | Category | Install |
|---|---|---|
| `nmap` | Port scanning | `sudo apt install nmap` |
| `subfinder` | Subdomain enum | `go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest` |
| `ffuf` | Directory fuzzing | `go install github.com/ffuf/ffuf/v2@latest` |
| `sqlmap` | SQL injection | `sudo apt install sqlmap` |
| `nuclei` | Vulnerability scanning | `go install github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest` |
| `burpsuite` | Web proxy | [portswigger.net](https://portswigger.net/burp) |
| `whatweb` | Tech fingerprinting | `sudo apt install whatweb` |
| `nikto` | Web scanner | `sudo apt install nikto` |
| `gau` | URL harvesting | `go install github.com/lc/gau/v2/cmd/gau@latest` |
| `dalfox` | XSS scanner | `go install github.com/hahwul/dalfox/v2@latest` |

### Email OSINT Tools

| Tool | Category | Install |
|---|---|---|
| `holehe` | Account discovery | `pip install holehe --break-system-packages` |
| `h8mail` | Breach aggregation | `pip install h8mail --break-system-packages` |
| `GHunt` | Google OSINT | `git clone https://github.com/mxrch/GHunt` |
| `sherlock` | Username hunt | `pip install sherlock-project --break-system-packages` |
| `theHarvester` | Email harvest | Built into Kali Linux |
| `HaveIBeenPwned` | Breach check | [haveibeenpwned.com](https://haveibeenpwned.com) |
| `Epieos` | Google + Gravatar | [epieos.com](https://epieos.com) |
| `MXToolbox` | DNS / SPF / DMARC | [mxtoolbox.com](https://mxtoolbox.com) |

---

## ⚠️ Legal Disclaimer

> All tools and checklists in this repository are intended **solely for authorized security testing**, red team engagements, CTF challenges, and lawful OSINT research on targets you have explicit permission to test. Unauthorized use against systems or individuals without consent may violate applicable laws including the Computer Fraud and Abuse Act (CFAA), UK Computer Misuse Act, and similar legislation in your jurisdiction.
>
> **The author accepts no liability for any misuse of the content in this repository.**

---

## 👤 Author

<div align="center">

**Prathiv Raj**
*Red Team Operator · Offensive Security · M.Sc. Cyber Security*

[![TryHackMe](https://img.shields.io/badge/TryHackMe-PrathivRaj-red?style=for-the-badge&logo=tryhackme)](https://tryhackme.com/p/PrathivRaj)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-cyberbot007-9fef00?style=for-the-badge&logo=hackthebox&logoColor=9fef00&labelColor=141d2b)](https://app.hackthebox.com/profile/cyberbot007)
[![GitHub](https://img.shields.io/badge/GitHub-Prathiv--Raj-181717?style=for-the-badge&logo=github)](https://github.com/Prathiv-Raj)

*"The quieter you become, the more you are able to hear."*

</div>

---

<div align="center">
<sub>Made for the security community · Use responsibly · Star ⭐ if useful</sub>
</div>
