# Homelab Monitoring Stack 📊

Este repositorio contiene un stack de monitoreo profesional y modular, basado en **Prometheus**, **Grafana** y **cAdvisor**, diseñado para la observabilidad completa de un entorno de microservicios Docker.

## 🛠️ Desafíos Técnicos y Soluciones (Troubleshooting)

Este proyecto destaca por la resolución de problemas reales de integración:

1. **Resolución de Metadatos (Name vs ID):**
   - **Problema:** cAdvisor reportaba únicamente IDs de cgroup, lo que impedía el uso de dashboards estándar.
   - **Solución:** Se configuró cAdvisor con modo `privileged: true` y acceso al kernel via `/dev/kmsg`.
2. **Normalización de Variables:**
   - **Solución:** Se reconfiguraron las variables dinámicas en Grafana usando `label_values(container_last_seen, name)` para asegurar un filtrado amigable.

## 📦 Despliegue
1. Clonar el repositorio.
2. Ejecutar: `docker compose up -d`
3. Importar el archivo `monitor-dashboard.json` en Grafana.
