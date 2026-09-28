# Hi, I'm Roberto Natera 👋

**Moving from 15 years of U.S. Navy aviation quality assurance into cloud engineering and test automation — Python, AWS, Linux, and security.**

My job was verifying that complex systems met specification before they flew — writing and executing test procedures, isolating faults across interacting subsystems, and confirming a fix actually worked. Zero-defect standard, because the cost of a miss wasn't a bad release.

Same question, different systems now.

---

### 🔨 Projects

**[vulnerability-management-program](https://github.com/Naterar/vulnerability-management-program)** — End-to-end vulnerability management implementation: policy drafting, stakeholder negotiation, scan authorization, prioritization, CAB approval, and a full remediation cycle verified across four authenticated scans. Baseline of 23 findings reduced to 3 — Critical and High eliminated.

Also contains ten DISA Windows 11 STIG controls scripted in PowerShell, each reading current state before applying and verifying after. One of them deliberately doesn't remediate: limiting non-system file shares depends on which shares are operationally required, and only the system owner knows that. It reports and stops.

**[soc-detection-lab](https://github.com/Naterar/soc-detection-lab)** — Security operations work in Microsoft Sentinel and Defender XDR. Detection queries across authentication, network flow, process execution, and cloud control-plane telemetry, each documented with what it catches and where it fails. Includes a full intrusion investigation report with attack timeline, IOC set, MITRE ATT&CK mapping, and containment plan.

**[python-practice](https://github.com/Naterar/python-practice)** — Applied Python covering object-oriented design, classes and inheritance, control flow, data structures, and module use. Aviation and motorsport domain problems — weight and balance calculator, weather minimums checker, pit stop fuel calculator.

Includes formal test documentation across three programs — 77 test cases spanning functional and computational coverage, boundary value analysis, compound-condition truth tables, evaluation-order precedence, and negative input handling. Six defects logged, two High severity, one caught in requirements review before a single test was executed. The weather-minimums cases are now being automated in pytest with GitHub Actions.

---

### 🚧 Currently building

**logon-triage** — A Python tool that reads Windows logon events and flags a burst of failed logons followed by a success from the same source IP: the KQL detection from soc-detection-lab, ported to code. Built test-first, one stage at a time — CLI and tests, then PostgreSQL storage, a FastAPI service, LLM-assisted triage with schema-validated output, then Docker, GitHub Actions, and an AWS deployment. Every stage ships with its own tests and a security check. Public once the first stage passes its tests.

---

### 📌 What I'd point to first

The parts of these repos worth reading are the limitations, not the capabilities.

A detection that joins failed logons to a subsequent success looks solid until you notice it has no time ordering and misses password spray entirely. A weather checker that reports only the first failing condition is correct behavior for its `elif` structure — but a pilot never learns a second limit was also breached. A weight calculator that accepts a negative ramp weight and prints it confidently is worse than one that crashes; the crash at least tells you something broke. Three of my remediation scripts reported success and didn't take — the rescan is the only reason I know.

Documenting why something isn't a defect, and what it still costs the user, is the distinction I care about.

---

### 🧰 Stack

**Languages** `Python` `SQL` `KQL` `PowerShell` `Bash`
**Testing** `Test case design` `Boundary value analysis` `Equivalence partitioning` `Defect tracking` `Verification`
**Systems** `Linux` `Windows` `Windows Server` `Git` `VS Code`
**Cloud & Security** `AWS` `Azure` `Microsoft Sentinel` `Defender XDR` `Tenable` `DISA STIG` `MITRE ATT&CK`
**In progress** `pytest` `GitHub Actions` `AWS hands-on (EC2, VPC, S3, IAM)` `Docker` `FastAPI` `LLM APIs`

---

### 🎓 Credentials

- **M.S.** Information Technology · **Post-Master's Certificate**, Information Systems · **B.S.** Aeronautical Science
- Meta Programming in Python (2026) · Duke University OOP in Python (2026) · Meta Introduction to Back-End Development (2026)
- AWS Certified Cloud Practitioner · Google Cybersecurity Professional Certificate (2026) · FCC General Radiotelephone Operator License · Lean Six Sigma Yellow Belt
- CompTIA Security+ SY0-701 — **in progress**; next: AWS AI Practitioner and Solutions Architect – Associate
- **Secret clearance** — inactive, investigation completed 2024
- 100% service-connected disabled veteran — VEOA and 30%-or-more disabled veteran appointing authority eligible
- Bilingual English / Spanish

---

### 🎯 Open to

Cloud support and engineering, QA and test automation, security analyst, federal IT specialist (2210), and data center operations roles. Remote, or Texas / Northern Virginia / Ohio / Florida.

📫 nateraroberto@outlook.com · [LinkedIn](https://www.linkedin.com/in/roberto-natera)
