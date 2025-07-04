# Ansible Project

This project is for experimenting and learning Ansible.

## What is Ansible?
Ansible is an open-source automation tool for IT tasks such as configuration management, application deployment, and task automation.

## Basic Ansible Commands

- **Check Ansible version:**
  ```
  ansible --version
  ```

- **Run a simple command on a remote host:**
  ```
  ansible all -i inventory -m ping
  ```

- **Run a playbook:**
  ```
  ansible-playbook -i inventory playbook.yml
  ```

## Getting Started

1. **Install Ansible:**  
   Follow the [official installation guide](https://docs.ansible.com/ansible/latest/installation_guide/index.html).

2. **Create an inventory file:**  
   List your servers in a file called `inventory`.

3. **Write a playbook:**  
   Create a YAML file (e.g., `playbook.yml`) to define your automation tasks.

## Example Inventory File

```
[webservers]
server1.example.com
server2.example.com
```

## Example Playbook

```yaml
---
- name: Install Apache on webservers
  hosts: webservers
  become: yes
  tasks:
    - name: Install Apache
      apt:
        name: apache2
        state: present
```

---

For more details, check the [Ansible documentation](https://docs.ansible.com/).