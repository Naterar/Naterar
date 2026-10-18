# Hi, I'm Roberto Natera 👋

**U.S. Navy veteran (15 yrs aviation QA) | Applied AI & cloud support | Python, LLM tooling, KQL, AWS, Linux | AWS Cloud Practitioner | Security+ in progress**

My job was verifying that complex systems met specification before they flew — writing and executing test procedures, isolating faults across interacting subsystems, and confirming a fix actually worked. Zero-defect standard, because the cost of a miss wasn't a bad release.

Same question, different systems now.

## 🔨 Projects

**[vulnerability-management-program](https://github.com/Naterar/vulnerability-management-program)** — End-to-end vulnerability management implementation: policy drafting, stakeholder negotiation, scan authorization, prioritization, CAB approval, and a full remediation cycle verified across four authenticated scans. Baseline of 23 findings reduced to 3 — Critical and High eliminated.

Also contains ten DISA Windows 11 STIG controls scripted in PowerShell, each reading current state before applying and verifying after. One of them deliberately doesn't remediate: limiting non-system file shares depends on which shares are operationally required, and only the system owner knows that. It reports and stops.

**[soc-detection-lab](https://github.com/Naterar/soc-detection-lab)** — Security operations work in Microsoft Sentinel and Defender XDR. Detection queries across authentication, network flow, process execution, and cloud control-plane telemetry, each documented with what it catches and where it fails. Includes a full intrusion investigation report with attack timeline, IOC set, MITRE ATT&CK mapping, and containment plan.

**[cyber_code](https://github.com/Naterar/cyber_code)** — Python pipeline that pulls Microsoft Defender telemetry from Azure Log Analytics with KQL, shows the estimated cost before spending anything, sends the logs to an LLM threat hunter, and saves the report. Five pytest tests cover the query builder (table whitelist, validated row limits) and the CSV conversion. On a 200-row slice of real logon data it surfaced a slow credential spray and an external admin logon. It also flagged the range's own vulnerability scanner as a possible attacker, which I only caught by checking the raw rows.

**[python-practice](https://github.com/Naterar/python-practice)** — Applied Python covering object-oriented design, classes and inheritance, control flow, data structures, and module use.

Includes formal test documentation across three programs — 77 test cases spanning functional and computational coverage, boundary value analysis, compound-condition truth tables, evaluation-order precedence, and negative input handling. Six defects logged, two High severity, one caught in requirements review before a single test was executed. The weather-minimums cases are now being automated in pytest with GitHub Actions.

## 🚧 Currently building

**[angel-flight-matcher](https://github.com/Naterar/angel-flight-matcher)** — Mission-matching assistant for volunteer medical-transport flights, built on synthetic data after three years volunteering with Angel Flight West. Parses intake requests, validates them, and matches each one against pilot and aircraft constraints — seats, useful load, range, availability — returning a reason for every rejection rather than a filtered list. Next: LLM extraction from free-text requests with schema-validated output, then tests in CI. Not affiliated with or endorsed by Angel Flight West.

## 📌 What I'd point to first

The parts of these repos worth reading are the limitations, not the capabilities.

A detection that joins failed logons to a subsequent success looks solid until you notice it has no time ordering and misses password spray entirely. A weather checker that reports only the first failing condition is correct behavior for its `elif` structure — but a pilot never learns a second limit was also breached. A weight calculator that accepts a negative ramp weight and prints it confidently is worse than one that crashes; the crash at least tells you something broke. A matcher that gives a reason per pilot beats a filter — until every pilot fails the same check and the coordinator reads eighteen identical lines to learn one fact.

Three of my configuration changes didn't take on the first attempt — the rescan is the only reason I know. An LLM threat hunter called the range's own vulnerability scanner a possible attacker; the failed logons arrived at machine-exact intervals, which is a scanner, not a person. I only know because I checked the raw rows before believing the report.

Documenting why something isn't a defect, and what it still costs the user, is the distinction I care about.

## 🧰 Stack

- **Languages:** Python · SQL · KQL · PowerShell · Bash
- **Testing:** pytest · test case design · boundary value analysis · equivalence partitioning · defect tracking · verification
- **Systems:** Linux · Windows · Windows Server · Git · VS Code
- **Cloud & security:** AWS · Azure · Microsoft Sentinel · Defender XDR · Tenable · DISA STIG · MITRE ATT&CK · LLM APIs
- **In progress:** GitHub Actions · AWS hands-on (EC2, VPC, S3, IAM) · Docker · FastAPI

## 🎓 Credentials

- Master of Information Systems · Post-Master's Certificate, Information Systems and Technology · B.S. Aeronautics
- LogN Pacific Cyber Range — Cybersecurity Internship (2026), completed; verifiable by employers
- Meta Programming in Python (2026) · Duke University OOP in Python (2026) · Meta Introduction to Back-End Development (2026) · Claude Academy: AI Fluency, Claude 101 (2026)
- AWS Certified Cloud Practitioner · Google Cybersecurity Professional Certificate (2026) · FCC General Radiotelephone Operator License · Lean Six Sigma Yellow Belt
- CompTIA Security+ SY0-701 — in progress; next: AWS AI Practitioner and Solutions Architect – Associate
- Secret clearance — inactive, investigation completed 2024
- Bilingual English / Spanish

## 🎯 Open to

Applied AI and forward-deployed engineering, cloud support and engineering, and QA and test automation. Remote, or Indiana / Texas / Northern Virginia / Ohio / Florida / New York / California.

## 📫 Contact

[nateraroberto@outlook.com](mailto:nateraroberto@outlook.com) · [LinkedIn](https://www.linkedin.com/in/roberto-natera/)
