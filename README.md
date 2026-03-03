# 🛡️ LogSentinel — Log Analysis & Threat Detection Tool

A desktop log analyzer built with Python and Tkinter.
Designed as a cybersecurity portfolio project covering threat detection, pattern matching, and log forensics.

---

## Features

-  **Multi-format support** — Apache/Nginx, Windows Event Logs, syslog, generic text logs
-  **Failed login detection** — flags authentication failures across all log types
-  **IP threat reporting** — tracks failed attempts per IP, flags brute force attackers
-  **Keyword / regex search** — search for any term or pattern across the entire log
-  **Tabbed results UI** — Overview, Flagged Entries, IP Report, Keywords, Raw Log
-  **Export reports** — save findings as `.txt` or `.csv`

---

## Setup

```bash
python main.py
```

No dependencies beyond the Python standard library.

---

## How to use

1. Click **Browse File** and select a log file (`.log`, `.txt`, etc.)
2. Optionally enter keywords to search for (comma-separated, supports regex)
3. Set the brute force threshold (default: 5 failed logins from one IP)
4. Click **Run Analysis**
5. Review results across the tabs
6. Export to TXT or CSV if needed

A `sample.log` file is included to test the tool immediately.

---

## Detection Capabilities

| Threat | Method |
|---|---|
| Brute force login | Counts failed logins per IP, alerts over threshold |
| Failed authentication | Regex patterns: "Failed password", "Audit Failure", 401 etc. |
| Path traversal | Detects `../../` patterns in web logs |
| SQL injection attempts | Detects `UNION SELECT` and similar patterns |
| XSS attempts | Detects `<script>` in request paths |
| Sensitive file access | Flags requests for `.env`, `.git`, `/etc/passwd` etc. |
| Suspicious admin access | Flags `/admin`, `/wp-login` probes |

---

## Resume Bullet Points

- *"Built a multi-format log analyzer detecting brute force, SQLi, XSS, and path traversal attacks"*
- *"Implemented regex-based threat detection engine supporting Apache, syslog, and Windows Event Log formats"*
- *"Designed tabbed GUI with IP reputation reporting and CSV/TXT export for incident response workflows"*

---
