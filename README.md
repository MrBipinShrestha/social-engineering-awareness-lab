# 🎭 Social Engineering Attack Simulation Lab

![SET](https://img.shields.io/badge/Tool-SET_Toolkit-red?style=for-the-badge)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-T1566-red?style=for-the-badge)
![Focus](https://img.shields.io/badge/Focus-Human_Attack_Vectors-purple?style=for-the-badge)

> **Cybersecurity awareness lab simulating real-world social engineering attacks using the Social Engineering Toolkit (SET), with documented detection controls and defensive countermeasures.**
>
> This lab validates the most underestimated attack surface in any organization: human behavior.

---

## 🧠 Security Engineering Objective

This lab answers a critical SOC and red team question:

> "How do attackers exploit human trust to bypass technical security controls, and how can organizations detect and prevent it?"

To validate this, I simulated real social engineering attack scenarios and documented:

- Attack execution methodology
- Human vulnerability patterns
- Detection controls and their effectiveness
- Defensive countermeasures

---

## 🏗️ Attack Surface Architecture

```
                    ┌─────────────────────┐
                    │   Social Engineer   │
                    │   (Attacker)        │
                    │   SET Toolkit       │
                    └──────────┬──────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
    ┌─────▼──────┐      ┌─────▼──────┐      ┌─────▼──────┐
    │  Phishing  │      │  Credential│      │  Malware   │
    │  Campaigns │      │  Harvesting│      │  Delivery  │
    └─────┬──────┘      └─────┬──────┘      └─────┬──────┘
          │                   │                   │
          └───────────────────┼───────────────────┘
                              │
                    ┌─────────▼─────────┐
                    │   Human Target    │
                    │   (Victim)        │
                    │   Clicks / Trusts │
                    └─────────┬─────────┘
                              │
                    ┌─────────▼─────────┐
                    │   Compromise      │
                    │   Credentials /   │
                    │   System Access   │
                    └───────────────────┘
```

---

## 🚨 Attack Scenarios Simulated

| # | Attack Type | MITRE Technique | Outcome |
|---|------------|----------------|---------|
| 1 | Credential harvesting site | T1566.002 | Captures login credentials |
| 2 | Spear phishing email | T1566.001 | Delivers malicious payload |
| 3 | Pretexting simulation | T1598 | Extracts sensitive information |
| 4 | USB drop simulation | T1091 | Physical vector payload delivery |

---

## 🔍 Detection Engineering Controls

### Technical Controls

**Email Gateway Detection:**
```
Rule: Flag emails with mismatched Reply-To and From headers
Alert: Potential phishing — domain spoofing detected
Severity: HIGH
Action: Quarantine + analyst review
```

**Web Proxy Detection:**
```
Rule: Block access to domains registered < 30 days ago
Alert: New domain access attempt blocked
Severity: MEDIUM
Action: Log + user notification
```

**Credential Harvesting Detection:**
```
Rule: POST request to non-corporate domain containing password fields
Alert: Potential credential submission to external site
Severity: CRITICAL
Action: Block + immediate SOC alert
```

### Human Controls

| Control | Effectiveness | Implementation |
|---------|--------------|----------------|
| Security awareness training | HIGH | Quarterly simulations |
| Phishing simulation campaigns | HIGH | Monthly randomized tests |
| Reporting culture | HIGH | No-blame reporting policy |
| Multi-factor authentication | CRITICAL | Mandatory for all accounts |

---

## 📊 MITRE ATT&CK Mapping

| Tactic | Technique | Scenario |
|--------|-----------|---------|
| Initial Access | T1566.001 (Spear Phishing) | Email-based attack |
| Initial Access | T1566.002 (Phishing Link) | Credential harvesting |
| Reconnaissance | T1598 (Phishing for Information) | Pretexting |
| Lateral Movement | T1091 (Removable Media) | USB drop |

---

## 📈 Key Findings

**Human Vulnerability Patterns:**
- Authority-based requests bypass critical thinking
- Urgency reduces verification behavior
- Familiar branding increases click rates
- Technical users are not immune

**Most Effective Defenses:**
1. Multi-factor authentication (stops credential theft impact)
2. Security awareness training (reduces initial click rate)
3. Email filtering with SPF/DKIM/DMARC validation
4. Incident reporting culture (speeds detection)

---

## 🧰 Tools Used

| Tool | Purpose |
|------|---------|
| Social Engineering Toolkit (SET) | Attack simulation framework |
| Kali Linux | Attack platform |
| Email analysis tools | Header forensics |
| OSINT tools | Target reconnaissance |

---

## ⚠️ Ethical Notice

All simulations conducted in isolated lab environment on systems owned and authorized for testing. Social engineering techniques documented for defensive education only. Never use these techniques against unauthorized targets.

---

## 🔮 Extensions

- [ ] Vishing (voice phishing) simulation
- [ ] SMS phishing (smishing) lab
- [ ] Business Email Compromise (BEC) scenarios
- [ ] Deepfake social engineering analysis
- [ ] Security awareness training curriculum

---

## 📬 Contact

**GitHub:** [github.com/MrBipinShrestha](https://github.com/MrBipinShrestha)
**LinkedIn:** [linkedin.com/in/shresthabipin](https://www.linkedin.com/in/shresthabipin)
**Location:** Sydney, Australia
