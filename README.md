## Hi, I'm Abderrahmen Takrouni

**Cloud Security · Linux Hardening · DevSecOps**

I build the part of security that actually runs on machines: hardened server
baselines, encrypted private clouds, backups that survive ransomware, and CI
pipelines that prove the work instead of claiming it. Every project I ship is tested in CI, documented, and
reviewable — the same standard I'd want on a production system.

---

### 🔐 Featured projects

#### [linux-hardening](https://github.com/abdrahmentakrouni/linux-hardening)

One-shot, idempotent hardening for fresh Ubuntu/Debian and RHEL/Rocky servers — pure Bash, zero dependencies.

- **3 run modes** — read-only `--audit` (scored report, CIS-inspired check IDs), zero-change `--dry-run`, and `--apply` that backs up every file it touches
- **Firewall automation** — auto-detects ufw / firewalld / raw iptables with persisted rules
- **SSH hardening** — validated with `sshd -t` before reload, automatic revert on failure, smart key-only auth that never locks you out
- **Password & account policies** — pwquality complexity, faillock lockout, login.defs aging
- **Kernel hardening** — 27 sysctl controls in a managed drop-in, Docker-aware
- **Brute-force protection** — fail2ban with escalating bans
- **Automatic security updates** — unattended-upgrades / dnf-automatic
- **CI-verified** — Docker test matrix (Ubuntu 24.04, Debian 12, Rocky 9) + shellcheck & bashate on every push

`bash` `linux` `security` `cis-benchmarks` `devsecops` `docker` `github-actions`

#### [secure-nextcloud](https://github.com/abdrahmentakrouni/secure-nextcloud)

A private cloud, hardened — GDPR-aligned Nextcloud for the "our client files
leaked" nightmare that keeps European companies up at night.

- **TLS everywhere** — local PKI generator (root CA + SAN cert), nginx with TLS 1.2/1.3 only, HSTS, login rate limiting
- **2FA forced on every account** — TOTP + backup codes, enforced instance-wide, no exceptions
- **RBAC / IAM** — five role groups, quotas, internal apps hidden from external clients, one-command offboarding
- **Encrypted backups** — AES-256 + PBKDF2, SHA-256 manifests, retention policy, documented restore drills
- **GDPR mapping** — every control documented against the regulation article it answers (Art. 32, 25, 5)
- **CI boots the whole stack** — hardening, 2FA, IAM and audit run end-to-end against a real Nextcloud on every push

`nextcloud` `docker-compose` `tls` `2fa` `iam` `gdpr` `nginx` `cloud-security`


#### [backup-vault](https://github.com/abdrahmentakrouni/backup-vault)

Ransomware-resilient automated backup and disaster recovery — the survival
layer for the night a company's servers get encrypted.

- **Automated nightly backups** — cron / systemd timers, files + consistent MariaDB/MySQL dumps, installed with one command
- **AES-256 encryption in one stream** — PBKDF2 (300k iterations), plaintext never touches the disk, passphrase never touches argv
- **3-2-1 off-site replication** — S3 (rclone), append-only SSH vault with a hardened ingest wrapper that refuses deletes, or a plain NAS/USB target
- **Grandfather-father-son retention** — 7 daily / 4 weekly / 12 monthly, pruned locally and remotely
- **Ransomware canary tripwire** — decoy business files checksummed before every run; drift aborts the backup with exit 42 before it can overwrite good copies
- **Provable recovery** — SHA-256 manifests, one-command drill with measured RTO, full health audit (RPO age, encryption, off-site, schedule)
- **CI disaster simulation** — every push: real backup, ransomware scrambles files and drops the database, restore from the vault, byte-for-byte proof (19 checks green)

`backup` `disaster-recovery` `ransomware` `business-continuity` `encryption` `rclone` `s3` `bash`

---

### 🧰 Toolkit

![Linux](https://img.shields.io/badge/Linux-05122A?style=flat&logo=linux&logoColor=white)
![Bash](https://img.shields.io/badge/GNU_Bash-05122A?style=flat&logo=gnu-bash&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-05122A?style=flat&logo=docker&logoColor=white)
![Nextcloud](https://img.shields.io/badge/Nextcloud-05122A?style=flat&logo=nextcloud&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-05122A?style=flat&logo=nginx&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-05122A?style=flat&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-05122A?style=flat&logo=redis&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-05122A?style=flat&logo=minio&logoColor=white)
![rclone](https://img.shields.io/badge/rclone-05122A?style=flat&logo=rclone&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-05122A?style=flat&logo=githubactions&logoColor=white)
![Git](https://img.shields.io/badge/Git-05122A?style=flat&logo=git&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-05122A?style=flat&logo=ubuntu&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-05122A?style=flat&logo=debian&logoColor=white)
![Red Hat](https://img.shields.io/badge/RHEL_.Rocky-05122A?style=flat&logo=redhat&logoColor=white)

**Focus areas:** server hardening · private cloud · backup & disaster recovery · ransomware resilience · TLS / PKI · identity & access management · data protection (GDPR) · CI security gates · firewalls · fail2ban

---

### 📊 GitHub Stats

<img src="https://github-readme-stats.vercel.app/api?username=abdrahmentakrouni&show_icons=true&theme=github_dark&hide_border=true" height="150" alt="GitHub stats"/> <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=abdrahmentakrouni&layout=compact&theme=github_dark&hide_border=true" height="150" alt="Top languages"/>

---

### 🌱 Currently learning

- **Cloud:** AWS core (IAM, VPC, EC2, CloudTrail) with a security lens
- **IaC:** Terraform — codified, reviewable infrastructure
- **Next builds:** more hands-on cloud security automation → watch this space

---

### 📫 Contact

[![Email](https://img.shields.io/badge/abdrahmentakrouni25@gmail.com-05122A?style=flat&logo=gmail&logoColor=white)](mailto:abdrahmentakrouni25@gmail.com)
