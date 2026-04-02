Open-Source Software Audit: Git

Name: Shashwat Pandey (Reg. No. 24BEC10121)
Date: 31/03/2026

This repository contains a detailed audit report analyzing Git as a prime example of open-source software (OSS). The report covers Git's origin from the 2005 Linux kernel crisis, GPL v2 licensing philosophy, ethical considerations, Linux system integration, role in the FOSS ecosystem, and comparison with proprietary alternatives like Perforce Helix Core.

[

📖 Project Summary
Git was created by Linus Torvalds when the Linux kernel team lost access to proprietary BitKeeper VCS. Facing an urgent need for fast, distributed version control, Git was built from scratch in days—prioritizing speed, data integrity (SHA-1 hashing), and complete independence from vendors.

Key Philosophy: Every developer gets a full repository copy, enabling offline work, rapid branching, and community-driven evolution. Stewardship passed to Junio Hamano in July 2005, proving OSS sustainability beyond founders.

📋 Main Components from Report

1. Origin & Problem Solved
2. 
2005 Crisis → BitKeeper revoked → Git born in days
- Distributed model (no central server dependency)
- Fast for massive kernel codebase
- Initial rough version → modern Git (branches, tags, remotes)

2. GPL v2 License Analysis

Four Freedoms: run, study, redistribute, modify
Key Feature: Reciprocity - derivatives must stay open
vs MIT: GPL prevents "enclosure" of community work

3. Linux Footprint

Installation: apt install git (Debian) | dnf install git (Fedora)
Config layers: /etc/gitconfig → ~/.gitconfig → .git/config
No daemon service - runs as user process
Updates via distro package managers

4. FOSS Ecosystem Role

Dependencies: Unix tools (diff, SSH, editors)
Powers: GitHub, GitLab, CI/CD pipelines
Impact: Pull requests, branching strategies now industry standard

5. OSS vs Proprietary Comparison

Aspect	Git (OSS)	Perforce Helix Core
Cost	Free	Enterprise licensing
Security	Community audits	Vendor transparency
Freedom	Full GPL modification	Vendor restrictions
Support	Docs + forums	Formal SLAs
Control	Community governance	Corporate roadmap
Verdict	Education/collaboration	Controlled enterprises

🖥️ Shell Scripts (Appendix)
Five practical audit scripts planned in report:

#!/bin/bash

1. System Identity

echo "OS: $(lsb_release -d | cut -f2)"
git --version

2. Package Check

dpkg -l | grep git || rpm -qa | grep git

3. Config Audit

git config --list --global | grep user

4. Repo Scan

find . -name ".git" -type d | head -5

5. OSS Manifesto

echo "Git: Crisis → Community → Infrastructure. GPL v2."

🚀 Quick Setup

git clone https://github.com/YOUR_USERNAME/oss-git-audit.git

cd oss-git-audit
chmod +x *.sh
./sys_id.sh  # Test Git installation
