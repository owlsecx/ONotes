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

Encrypted operator notes & engagement log

---

## ✨ Features

- Encrypted notebook store under ~/ONotes/ — every notebook is one JSON document encrypted at rest
- Container: MAGIC|hdr|salt|iv|hmac|ciphertext with PBKDF2-HMAC-SHA256 key derivation and encrypt-then-MAC (HMAC-SHA256) authentication
- Cipher: AES-256-CBC when PyCryptodome is present, otherwise a stdlib-only HMAC-SHA256 counter-mode keystream (documented below) — both authenticated
- Notes CRUD — title, tags, markdown-ish body, created/modified timestamps, pin & favourite
- Full-text search with tag / date / pin filters, AND-terms, "quoted phrases" and -exclusions
- Engagement templates — recon log, finding write-up, IOC sheet, credentials-handled checklist, timeline
- Attachment metadata — path + SHA-256 + size, no binaries embedded; verify integrity later
- Engagement log — timestamped operator activity log
- Export — Markdown / TXT / JSON (password confirm) and redacted export masking secret patterns
- Auto-lock after idle, manual lock, change password (full re-encryption with fresh salt + IV)
- Full CLI (--new, --open, --add, --search, --list, --export, ...) and interactive menu

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./ONotes
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
