# Watcher 1.4 (Production) - README
The Watcher-V1 series is the rendition for xtables firewalls managed by 'iptables' and 'ipset'.

# Official Resources:
## Official Watcher repository
- [Repository](https://watcher.comserve-it-services.de/repo/)

## Official Packages
- [Production](https://watcher.comserve-it-services.de/repo/Watcher-1.4-Prod/)
- [Nightly](https://watcher.comserve-it-services.de/repo/Watcher-1.4-nightly/)

## Official Documentation
- [Docs](https://watcher.comserve-it-services.de/repo/Docs/)
- [Master Doc](https://watcher.comserve-it-services.de/repo/Docs/Watcher-Master-V1.4doc.pdf)
- [Modules Doc](https://watcher.comserve-it-services.de/repo/Docs/Watcher-Modules-V1.4doc.pdf)

# Introduction:
# 🛡️ Watcher – Driving Attackers Mad

**Watcher is not a simple script.**
Watcher is a **program system** and a **complex framework**
It is a modular, fully automated IDS/IPS framework designed to block potential attackers in real-time, at the firewall level, before your services even become aware of them.

## What It Does

Watcher modules continuously monitor service logs (e.g., SSH, web, and mail) in real-time.  
When suspicious behavior is detected, it immediately blocks the source IP via `ipset' – protecting the services from wasting CPU on known offenders.

**Its purpose is simple:**  
Let your services do their job — not log endless abuse from IP `aa.bb.cc.dd`.

## Key Features

- Real-time log monitoring
- Modular detection engine (per-service filters)
- Immediate firewall blocking (DROP via 'ipset')
- No dependencies: no RPM, no APT, no pip – *drop-in, superuser-only*
- Works with syslog/syslog-ng
- Portable, robust – designed for Linux server environments

## Installation Philosophy

Watcher is **drop-anywhere software**. It is intentionally kept minimalistic:

```sh
# tar xf Watcher.tar
# cd Watcher
# ./Prep

## Watcher efficiency

```text
[root@vmd123606 rules]# Watcher-Report -e | grep 'Summary' -A15
_____ Summary ________________________________________
          Total DROPed connections:   106631
          Total passed connections:    31105
        Total passthru connections:    28210
         Total records in firewall:    36678
                        Efficiency:    77.40% 
                          .... min:    77.30% 
                          .... max:    90.80% 

_____ Legend _________________________________________
	passthru 	- Count of 'white bots'
	TD/TP 		~ Total dropped/passed 
	Efficiency	= TD / (TD+TP)

```
