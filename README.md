# Social Engineering Awareness Lab

**Educational phishing simulation using SET (Social Engineering Toolkit) to understand credential harvesting attacks, social engineering tactics, and prevention strategies.**

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Kali](https://img.shields.io/badge/platform-Kali%20Linux-blue.svg)
![Status](https://img.shields.io/badge/status-Educational-green.svg)
![Ethical](https://img.shields.io/badge/purpose-Defense%20Only-brightgreen.svg)

---

## 🎯 Overview

This lab demonstrates **how credential harvesting phishing attacks work** in a controlled environment using the Social Engineering Toolkit (SET). By understanding the attack methodology, organizations can:

- Recognize how phishing emails deceive users
- Understand why fake websites convince victims
- Implement multi-layered defenses
- Train employees to identify phishing attempts
- Respond effectively to phishing incidents

**Target Audience:** Security professionals, penetration testers, security awareness trainers, students, SOC teams.

---

## 🔬 Lab Objectives

After completing this lab, you will understand:

✅ How the Social Engineering Toolkit (SET) works  
✅ Website cloning and credential harvesting techniques  
✅ How attackers exploit user psychology  
✅ Why users fall for phishing attacks  
✅ How to detect phishing at multiple layers  
✅ Multi-layered prevention strategies  

---

## 📋 Lab Environment

### Requirements

**Hardware:**
- Virtual Machine with 2GB+ RAM
- Network interface with internet access
- 10GB free disk space

**Software:**
- Kali Linux (or Ubuntu with SET installed)
- Social Engineering Toolkit (SET) — pre-installed on Kali
- Web browser (Firefox, Chromium)
- Terminal access
- Optional: Wireshark for traffic analysis

**Knowledge:**
- Basic Linux command line
- Understanding of HTTP/HTTPS
- Web browsers and login pages
- Networking concepts (IP, DNS)

---

## 🚀 Quick Start (30 Minutes)

### Step 1: Start Kali Linux & Verify SET
```bash
# Check SET installation
which setoolkit

# If not installed:
sudo apt-get update
sudo apt-get install set

# Get your local IP (for hosting fake page)
ifconfig
# Note: inet 192.168.1.100 (or similar)
```

### Step 2: Launch SET
```bash
# Start SET with elevated privileges
sudo setoolkit

# Navigate: 
# 1) Social-Engineering Attacks
# → 2) Website Attack Vectors
# → 3) Credential Harvester Attack Method
```

### Step 3: Clone Target Website
```
SET Menu:
→ 2) Site Cloner
→ Enter URL: https://www.instagram.com
→ Enter YOUR attacker IP: 192.168.1.100
→ SET clones the page and hosts it
```

### Step 4: Capture Credentials
```
✓ SET is now hosting fake Instagram at http://192.168.1.100
✓ When victim visits and enters credentials:
  [Credentials displayed in SET terminal]
  Username: victim@email.com
  Password: VictimPassword123!
```

---

## 📊 Lab Components

### Phase 1: Attack Setup
- Kali Linux environment configuration
- SET installation and setup
- Network interface identification
- Target website selection

### Phase 2: Website Cloning
- Instagram login page cloning
- HTML/CSS/JavaScript acquisition
- Local hosting configuration
- Post-back IP configuration

### Phase 3: Social Engineering
- Phishing email crafting
- Social engineering tactics (authority, urgency, social proof)
- Victim targeting
- Link distribution methods

### Phase 4: Credential Harvesting
- User visits fake page
- Credentials submitted via form
- Credential capture and logging
- Data extraction

### Phase 5: Detection & Analysis
- Email header analysis
- URL verification
- Network traffic inspection
- Behavioral indicators

### Phase 6: Prevention & Remediation
- Multi-layered controls
- User training strategies
- Email filtering
- MFA implementation

---

## 🔍 Attack Flow

```
┌─────────────────────────────────────────────────────┐
│ PHISHING ATTACK METHODOLOGY                         │
└─────────────────────────────────────────────────────┘

1. RECONNAISSANCE
   Target selection & intelligence gathering
   ↓
2. WEBSITE CLONING (SET)
   Clone legitimate Instagram login page
   ↓
3. HOSTING
   Host fake page on attacker's machine
   ↓
4. SOCIAL ENGINEERING
   Craft phishing email with urgency/authority
   ↓
5. DELIVERY
   Send email to target with malicious link
   ↓
6. USER INTERACTION
   Victim clicks link → visits fake page
   ↓
7. CREDENTIAL SUBMISSION
   Victim enters username/password
   ↓
8. CREDENTIAL CAPTURE
   SET intercepts and logs credentials
   ↓
9. ACCOUNT COMPROMISE
   Attacker logs into real account with stolen credentials
```

---

## 🛡️ Prevention Strategies

### Technical Controls
```
✓ SPF/DKIM/DMARC
  - Prevent email spoofing
  
✓ Email Filtering
  - Block phishing emails before delivery
  
✓ MFA/2FA
  - Second factor stops account takeover even with password
  
✓ HTTPS Enforcement
  - Certificate warnings catch fake pages
  
✓ Browser Security
  - Built-in phishing detection
```

### User Practices
```
✓ Verify Sender Address
  - Check actual email (not display name)
  
✓ Hover Over Links
  - See real URL before clicking
  
✓ Type URLs Manually
  - Never click email links for login
  
✓ Check for HTTPS
  - Verify certificate before entering credentials
  
✓ Enable MFA
  - Second factor provides additional protection
  
✓ Report Suspicious Emails
  - Help security team identify threats
```

### Organizational Controls
```
✓ Security Awareness Training
  - Educate users about phishing
  
✓ Phishing Simulations
  - Test employee preparedness
  
✓ Incident Response
  - Clear procedures for handling compromises
  
✓ Email Security Policies
  - Guidelines for safe email practices
```

---

## 📈 Key Findings from Lab

### Why This Attack Works

**User Psychology:**
- ✗ Authority bias — "Instagram expert" = trust
- ✗ Urgency — "Act now" triggers panic
- ✗ Social proof — Fake screenshots show "others succeed"
- ✗ Familiarity — Cloned page looks identical

**Technical Factors:**
- ✗ No HTTPS verification
- ✗ No domain verification
- ✗ No email authentication (SPF/DKIM)
- ✗ No MFA protection

### Prevention Insights

**Why Prevention Fails:**
- Users don't verify email addresses
- Users don't check URLs before clicking
- Users don't notice HTTP vs HTTPS
- Users panic and skip verification steps

**Why Prevention Works:**
- MFA blocks account takeover even with password
- Email filtering removes phishing emails
- User training improves recognition
- Technical controls catch many attacks

---

## 🧪 Lab Exercises

### Exercise 1: Basic Credential Harvesting
**Objective:** Clone Instagram and capture credentials  
**Duration:** 30 minutes  
**Difficulty:** Beginner  
See: `01-basic-credential-harvesting.md`

### Exercise 2: Social Engineering Email
**Objective:** Craft convincing phishing email  
**Duration:** 20 minutes  
**Difficulty:** Beginner  
See: `02-phishing-email-crafting.md`

### Exercise 3: Detection & Analysis
**Objective:** Identify phishing indicators  
**Duration:** 30 minutes  
**Difficulty:** Intermediate  
See: `03-phishing-detection.md`

### Exercise 4: Prevention Controls
**Objective:** Implement multi-layered defenses  
**Duration:** 45 minutes  
**Difficulty:** Intermediate  
See: `04-prevention-implementation.md`

### Exercise 5: Incident Response
**Objective:** Respond to phishing incident  
**Duration:** 30 minutes  
**Difficulty:** Advanced  
See: `05-incident-response-drill.md`

---

## 📁 Repository Structure

```
social-engineering-awareness-lab/
├── README.md (this file)
├── ETHICAL-GUIDELINES.md (IMPORTANT - read first!)
├── LICENSE
│
├── 01-lab-setup/
│   ├── environment-setup.md
│   ├── set-installation.md
│   └── network-configuration.md
│
├── 02-attack-methodology/
│   ├── step-by-step-walkthrough.md
│   ├── attack-flow-diagram.txt
│   └── set-commands-reference.md
│
├── 03-exercises/
│   ├── 01-basic-credential-harvesting.md
│   ├── 02-phishing-email-crafting.md
│   ├── 03-phishing-detection.md
│   ├── 04-prevention-implementation.md
│   └── 05-incident-response-drill.md
│
├── 04-detection-prevention/
│   ├── email-header-analysis.md
│   ├── red-flags-checklist.md
│   ├── prevention-controls-matrix.md
│   └── user-awareness-tips.md
│
├── 05-resources/
│   ├── tools-reference.md
│   ├── psychological-tactics.md
│   └── case-studies.md
│
└── screenshots/
    ├── set-menu.png
    ├── fake-instagram-page.png
    ├── credential-capture.png
    └── email-header-analysis.png
```

---

## 🔐 Ethical & Legal Guidelines

### ⚖️ IMPORTANT: Read First!

This lab is **for educational and authorized testing ONLY**.

**What You CAN Do:**
✅ Learn phishing attack methodologies in **isolated lab environments**  
✅ Conduct **authorized** phishing simulations with **written permission**  
✅ Test **your own** systems and infrastructure  
✅ Teach cybersecurity to students in **controlled labs**  
✅ Help organizations improve their defenses  

**What You CANNOT Do:**
❌ Conduct unauthorized phishing attacks  
❌ Test others' systems without written approval  
❌ Use for malicious purposes or fraud  
❌ Harvest real credentials without consent  
❌ Deploy against real users without explicit authorization  

**Legal Consequences:**
Unauthorized phishing is illegal in most jurisdictions and can result in:
- Criminal charges (felony)
- Fines ($1,000 - $100,000+)
- Imprisonment (1-5+ years)
- Civil liability
- Restitution to victims

**See:** `ETHICAL-GUIDELINES.md` for detailed requirements.

---

## 💼 Career Relevance

**Why Recruiters Love This Project:**

### SOC Analyst Roles
- Demonstrates attack understanding
- Shows detection capabilities
- Practical phishing analysis skills
- Email security knowledge

### Penetration Tester Roles
- Real attack tool expertise
- Social engineering understanding
- Methodology documentation
- Authorized testing knowledge

### Security Engineer Roles
- Multi-layered defense design
- Email security implementation
- User awareness training
- Risk mitigation strategies

### Security Awareness Trainer Roles
- Training material creation
- User behavior understanding
- Practical demonstrations
- Incident response knowledge

---

## 📊 Statistics & Context

**Why Phishing Matters:**
- Phishing is the **#1 initial compromise vector** in breaches
- **90%+** of breaches start with phishing
- Average cost per breach: **$4.29 million USD**
- Average employee click rate: **34%** (2023 data)
- Time from click to compromise: **1-2 hours**

**This Lab Teaches:**
- Real attack mechanisms
- Why users are vulnerable
- How to defend effectively
- Importance of layered defenses

---

## 🛠️ Tools Reference

### Social Engineering Toolkit (SET)
```
Website: https://www.trustedsec.com/tools/social-engineer-toolkit/
Creator: David Kennedy (ReL1K)
License: Open source
Platform: Kali Linux (pre-installed)
```

### Related Tools
```
Kali Linux — Penetration testing platform
Wireshark — Network traffic analysis
Metasploit — Exploitation framework
Burp Suite — Web application testing
```

---

## 📚 Learning Resources

### Official Documentation
- **SET Documentation:** https://www.trustedsec.com/tools/social-engineer-toolkit/
- **Kali Linux:** https://www.kali.org/
- **MITRE ATT&CK:** https://attack.mitre.org/

### Recommended Reading
- **Phishing Domain Classifier:** https://www.owasp.org/
- **Security Awareness:** https://www.sans.org/
- **Email Security:** https://www.cyberdefensereview.army.mil/

### Related Projects
- Network Anomaly Detection (Machine Learning for IDS)
- Wireshark HTTP vs HTTPS Analysis
- ClamAV Malware Detection Lab

---

## ❓ FAQ

**Q: Is this legal?**  
A: Authorized use in controlled labs is legal. Unauthorized phishing is not.

**Q: Can I use this against real users?**  
A: Only with written permission from the organization. See ETHICAL-GUIDELINES.md.

**Q: What if I get caught testing without permission?**  
A: You could face criminal charges. Always get written authorization.

**Q: How do I protect myself?**  
A: Test in isolated lab environments. Document authorization. Keep records.

**Q: What should my organization do?**  
A: Conduct authorized phishing simulations with vendor support. Train employees. Implement technical controls.

---

## 🤝 Contributing

Found an improvement? Have a question?

- **Bug Reports:** Open a GitHub issue
- **Suggestions:** Discussions section
- **Lab Ideas:** Pull requests welcome

See `CONTRIBUTING.md` for guidelines.

---

## 📄 License

MIT License — Educational use only.

**See LICENSE file for full details.**

---

## 👤 Author

**Repository Created By:** Bipin Shrestha  
**Based On:** MIT503 Information Security Course (Task 1)  
**Last Updated:** June 2024  
**Maintained For:** Security professionals, educators, students

---

## 🔗 Related Projects

⭐ **[Network-Anomaly-Detection-UNSW-NB15](https://github.com/MrBipinShrestha/network-anomaly-detection-unsw-nb15)**  
Machine learning-based network intrusion detection using ML pipeline

⭐ **[Wireshark-HTTP-vs-HTTPS-Analysis](https://github.com/MrBipinShrestha/wireshark-http-vs-https-analysis)**  
Network traffic analysis demonstrating HTTP plaintext vs TLS encryption

⭐ **[ClamAV-Malware-Detection-Lab](https://github.com/MrBipinShrestha/clamav-malware-detection-lab)**  
Antivirus signature-based malware detection and remediation

---

## ⭐ Don't Forget to Star!

If this lab helped you understand phishing attacks, **please star this repository** ⭐

Your star helps others discover this educational resource.

---

**Let's make cybersecurity education better.** 🛡️

