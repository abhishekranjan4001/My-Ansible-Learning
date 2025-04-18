# 📍 Introduction to Ansible

---

## 🧾 What is Ansible?

Ansible is an open-source automation tool for:
- Configuration Management
- Application Deployment
- Task Automation
- IT Orchestration

It uses YAML to define automation jobs (called **playbooks**) and connects to remote machines using SSH (no agent installation required).

---

## 💡 Key Features

- **Agentless**: Uses SSH instead of installing agents
- **Idempotent**: Safe to run repeatedly — only makes changes when necessary
- **Simple YAML Syntax**: Easy to read and write
- **Cross-Platform**: Supports Linux, Windows (to some extent), network devices, cloud platforms

---

## 🔑 Core Concepts

| Concept        | Description                                                 |
|----------------|-------------------------------------------------------------|
| Control Node   | Machine where Ansible is installed                          |
| Managed Node   | Target machines (clients/servers) Ansible controls          |
| Inventory      | List of hosts Ansible will manage                           |
| Module         | Units of work like `apt`, `copy`, `ping`, etc.              |
| Task           | A single action in a playbook                               |
| Playbook       | YAML file defining tasks to be run on target machines       |
| Handler        | Special task triggered by a `notify`                        |
| Facts          | System information gathered automatically                   |

---

## 🧪 How Ansible Works (Simplified Flow)

1. You create an inventory of servers.
2. Write a playbook to define the task.
3. Ansible connects over SSH to each server.
4. Executes the specified tasks using Python modules.
5. Returns results to the control node.

---

## 🔧 Prerequisites

- A control node (Linux/macOS or WSL on Windows)
- Python 3.x installed
- Remote Linux-based hosts with SSH access

---

## ✅ Install Ansible (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install ansible -y
ansible --version
