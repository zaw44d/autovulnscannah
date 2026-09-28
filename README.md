# Automated Vulnerability Scanner

It takes time out of a Cybersecurity Professionals work shift to manually find common vulnerabilities within endpoint devices, so I decided to look into how to code my own script to save precious time, enabling the user to be able to cut out the tedious work with one simple python script. 

## Conceptual Premise

The way I want the tool to be structured is by having one min script that accepts arguments and triggers dual functionalities. These include ,but hopefully will not be limited to, a dedicated network vulnerability scanner and a configuration auditor. 

- **Network vulnerability scanner should achieve**:
	- Host and IP discovery
	- Services and Port scanning
	- Reporting feature

- **Configuration auditor should achieve:**
	- Operating system check (Windows/Linux)
	- Scan against hardening standards
	- Reporting feature

```
┌─────────────────────────────────────────────────────────┐ 
│                  auto_vuln_scannah.py                   │
└───────────┬─────────────────────────────────┬───────────┘ 
            │                                 │ 
            ▼                                 ▼ 
┌─────────────────────────┐ ┌─────────────────────────┐ 
│ network_scanner.py      │ │ config_audit.py         │ 
│ - Host and IP discovery │ │ - Operating system      │
│                         │ │ check (Windows/Linux)   │ 
│ - Services and Port     │ │ - Scan against hardening│
│ scanning                │ │ standards               │
│ - Reporting feature     │ │ - Reporting feature     │
└─────────────────────────┘ └─────────────────────────┘

```

## First Iteration


