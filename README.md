# Wazuh SIEM Deployment Guide

A complete, hands-on deployment of **Wazuh** — an open-source XDR and SIEM platform — as a single-node installation on a VMware virtual machine running Ubuntu Server, following Wazuh's official step-by-step installation guide from start to finish.

📄 **[Read the full guide (PDF)](./Wazuh_SingleNode_Installation_Guide.pdf)**

---

## Overview

This lab documents every stage of standing up Wazuh on a single Linux host, with all three core components installed on the same node:

- Provisioning the Ubuntu Server VM in VMware Workstation Pro
- Generating SSL/TLS certificates for secure inter-component communication
- Installing and configuring the **Wazuh Indexer** (OpenSearch-based data store)
- Installing the **Wazuh Server** and **Filebeat** (analysis engine + log shipper)
- Installing the **Wazuh Dashboard** (web UI)
- Starting and verifying each service through `systemd`
- Logging in and confirming the full stack is operational

Every command is documented with its purpose, and every step is backed by a screenshot from the actual deployment — no steps skipped or simplified.

## Lab Environment

| | |
|---|---|
| **Operating System** | Ubuntu Server 24.04 LTS |
| **Virtualization** | VMware Workstation Pro |
| **Wazuh Version** | 4.14 |
| **Components (single-node)** | Wazuh Indexer, Wazuh Server, Wazuh Dashboard |
| **Host IP (lab)** | 192.168.75.130 |

## Why This Project

Wazuh is one of the most widely deployed open-source SIEM and XDR platforms, combining log analysis, file integrity monitoring, vulnerability detection, and compliance auditing in a single stack. Deploying it manually — rather than through a quickstart script — builds a real understanding of how the Indexer, Server, and Dashboard components authenticate and communicate with each other, which is the same architecture used in production SOC environments.

This project is the first in an ongoing home SOC lab series, followed by a deployment of the **[Elastic Stack (ELK)](https://github.com/Khizar-malik97/elastic-stack-siem-deployment)**, with the goal of building hands-on, demonstrable experience across multiple SIEM platforms ahead of SOC Analyst / Junior Security Engineer roles.

## Next Steps

- Register endpoints as Wazuh agents for centralized monitoring
- Configure custom detection rules and alerting
- Enable vulnerability scanning and file integrity monitoring
- Explore built-in compliance dashboards (PCI DSS, HIPAA, NIST)

---

**Author:** Khizar Ul Islam (Malik)
BS Software Engineering — SZABIST Islamabad | CEH Certified
[LinkedIn](https://linkedin.com/in/khizarulislam79) · [GitHub](https://github.com/Khizar-malik97)
