# 🦉 ONotes

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCore-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **ONotes** — Encrypted Operator Notebook

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

ONotes is an encrypted operator notebook for engagement notes, templates, attachments metadata, search, and export. Notebooks are stored encrypted at rest under `~/ONotes/` with PBKDF2-HMAC-SHA256 and encrypt-then-MAC; AES-256-CBC is used when PyCryptodome is available, otherwise a documented stdlib keystream. Full CLI and interactive menu are provided.

---

## ✨ Features

- Encrypted notebook store (MAGIC|hdr|salt|iv|hmac|ciphertext) with PBKDF2 and encrypt-then-MAC
- Notes CRUD with title, tags, markdown-ish body, pin/favourite, and timestamps
- Full-text search with tag/date/pin filters, AND terms, quoted phrases, and exclusions
- Engagement templates (recon, finding, IOC, credentials checklist, timeline) and engagement log
- Attachment metadata (path + SHA-256 + size) with later verify; secret-like data scan
- Export Markdown/TXT/JSON with optional redaction; re-key via password change; auto/manual lock

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ONotes --new engagement1 --engagement "Pentest A" --client Acme
./ONotes --open engagement1 --add --title "Finding" --template finding --body-file note.md
./ONotes --open engagement1 --search "sqli #web" --export md -o export.md --redact
./ONotes --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
