# 🦉 OKey

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OCipher-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.1-cyan?style=flat-square"/>
</p>

> **OKey** — Key Derivation & Password Hashing

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OKey derives cryptographic keys from passwords and manages password hashing utilities. It supports PBKDF2, scrypt, bcrypt, Argon2id, and HKDF (stdlib for PBKDF2/scrypt; optional libs for bcrypt/Argon2), plus password generation, salt generation, and hash-format identification via subcommands.

---

## ✨ Features

- Key derivation subcommand with PBKDF2-SHA256/512, scrypt, bcrypt, argon2id, and hkdf-sha256
- Password via `--password-env` (preferred) or `--password`; hex salt generation when omitted
- Configurable iteration count, output length, and HKDF info string; JSON output option
- Secure password generator with length/count and optional no-special charset
- Random salt/key generation in hex, base64, or base64url formats
- Password-hash format identification for common hash strings

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OKey derive --password-env PASS --algo pbkdf2-sha256 --iter 600000 --json
./OKey genpass --length 24 --count 3
./OKey salt --bytes 32 --fmt hex
./OKey --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
