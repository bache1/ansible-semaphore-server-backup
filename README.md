# Centralized Server Backup Automation & Orchestration
> An automated backup orchestration system for applications, databases, and virtual machines using Ansible Playbooks, Semaphore UI, and Proxmox Backup Server (PBS), integrated with real-time Discord notifications.

---

##  Project Overview
In a data center environment, maintaining data availability and service reliability is critical. This project addresses the challenge of decentralized backup execution by implementing a centralized orchestration mechanism at the Department of Communication, Informatics, Statistics, and Code of Bekasi City (Diskominfostandi). 

Using **Ansible** and **Semaphore UI**, the system standardizes and automates the backup workflow across multiple servers, reducing manual effort and minimizing human error

---

##  Tech Stack & Tools
* **Orchestration Engine:** Ansible (Playbooks, Agentless architecture).
* **Management UI:** Semaphore UI (Web-based task execution, scheduling, and history logs).
* **Virtualization & Backup:** Proxmox VE, Proxmox Backup Server (PBS).
* **Secure Communication:** Secure Shell (SSH).
* **Alerting System:** Discord Webhook Notifications.
* **Operating System:** Linux Server (Ubuntu).

---

## Architecture & Workflow
1. **Trigger / Schedule:** The administrator initiates or schedules a backup task via the **Semaphore UI** dashboard.
2. **Execution:** Semaphore UI triggers the respective **Ansible Playbook** on the management server.
3. **Secure Connection:** Ansible connects securely via **SSH** to target App/DB servers and Proxmox VE nodes.
4. **Backup Process:** 
   * Application files and databases are compressed and stored securely.
   * Virtual Machines (VMs) are snapshotted and backed up directly to **Proxmox Backup Server (PBS)**.
5. **Monitoring & Alerting:** Execution logs are tracked on Semaphore UI, and automated success/failure status messages are instantly dispatched to a dedicated **Discord** channel.

---

## Repository Structure
```text
ansible-semaphore-server-backup/
├── playbooks/
│   ├── backup_app.yml          # Playbook for application backups
│   ├── backup_db.yml           # Playbook for database backups
│   └── proxmox_backup.yml      # Playbook for Proxmox VM backups to PBS
├── inventory/
│   └── hosts.ini               # Target servers inventory group
└── README.md                   # Project documentation
```

## Key Features
- **Centralized Management:** Control all server backups from a single web-based interface.
- **Reusable & Consistent Playbooks:** Modular Ansible YAML configurations ensuring uniform backup execution.
- **Automated Alerting:** Real-time feedback loop via Discord webhooks to monitor backup health without manual log checking.

## Author
**Salsabila Bachtiar**
- Informatics Student | Aspiring DevOps & Cloud Engineer  
[LinkedIn](https://www.linkedin.com/in/salsabila-bachtiar-30161724a) | [GitHub](https://github.com/bache1)
