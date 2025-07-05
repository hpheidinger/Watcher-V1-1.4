# Watcher 1.4 (Production) - README

# Resources:
## Official Watcher repository

- [Repository](https://watcher.comserve-it-services.de/repo/)

## Official Packages

- [Production](https://watcher.comserve-it-services.de/repo/Watcher-1.4-Prod/)
- [Nightly](https://watcher.comserve-it-services.de/repo/Watcher-1.4-nightly/)

## Official Documentation

- [Docs](https://watcher.comserve-it-services.de/repo/Docs/)

# Introduction:
# 🛡️ Watcher – Driving Attackers Mad

**Watcher is not a script.**  
It is a modular, fully automated IDS/IPS framework designed to block potential attackers in real-time, at the firewall level, before your services even become aware of them.

## What It Does

Watcher continuously monitors service logs (e.g., SSH, web, and mail) in real-time.  
When suspicious behavior is detected, it immediately blocks the source IP via `iptables` or `nftables` – protecting the services from wasting CPU on known offenders.

**Its purpose is simple:**  
Let your services do their job — not log endless abuse from `aa.bb.cc.dd`.

## Key Features

- 🔍 Real-time log monitoring
- 🧩 Modular detection engine (per-service filters)
- 🔒 Immediate firewall blocking (DROP via iptables/nftables)
- 📦 No dependencies: no RPM, no APT, no pip – *drop-in, superuser-only*
- 🔧 Works with syslog/syslog-ng, firewalld, and custom nftables rulesets
- 📁 Portable, robust – designed for UNIX/Linux environments

## Installation Philosophy

Watcher is **drop-anywhere software**. It is intentionally kept minimalistic:

```sh
# tar xf Watcher.tar
# cd Watcher
# ./Prep
