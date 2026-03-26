# 🚀 My Ultimate Homelab (IaC Edition)

Este repositorio contiene la infraestructura completa de mi Homelab, gestionada mediante **Infraestructura como Código (IaC)**.

## 🛠️ Tecnologías
- **Virtualización:** VirtualBox (Ubuntu VM Detrás de pfSense).
- **Orquestación:** Docker & Docker Compose.
- **Automatización:** Ansible.
- **Monitoreo:** Prometheus + Grafana + cAdvisor + Node Exporter.

## 📂 Estructura del Proyecto
- `ansible/`: Playbooks para configurar el servidor y desplegar stacks.
- `stacks/monitoring/`: Stack de monitoreo profesional.
- `stacks/general/`: Otros servicios del homelab.

## 🚀 Cómo desplegar
Para poner todo en marcha tras un reinicio o cambio de configuración:
```bash
cd ansible
ansible-playbook -i inventory.ini deploy_stacks.yml --ask-become-pass