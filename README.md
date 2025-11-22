# Hybrid Cloud SOC (Wazuh Implementation)

![Status](https://img.shields.io/badge/STATUS-ACTIVE-success?style=for-the-badge)
![Security](https://img.shields.io/badge/FOCUS-BLUE%20TEAM%20%2F%20SOC-blue?style=for-the-badge)
![Platform](https://img.shields.io/badge/PLATFORM-GCP%20%2B%20LINUX-orange?style=for-the-badge)

**[English]** | [Español](#español-abajo)

## About the Project
A practical implementation of a **SIEM/XDR system** deployed in a Hybrid Cloud environment. 
I configured a **Wazuh Server** on Google Cloud Platform (GCP) to monitor, detect, and generate alerts for security events occurring on a remote local machine (simulating a corporate endpoint).

**Goal:** Demonstrate proficiency in Cloud Infrastructure, Log Analysis, and Incident Response.

## Architecture & Network Flow

> **Cloud Server (Ubuntu):** Wazuh Manager + Elastic Stack  
> **Local Client (Windows/Linux):** Wazuh Agent

`[Local Endpoint]` --(Encrypted Port 1514)--> `[Internet]` --> `[GCP Firewall]` --> `[Wazuh Manager]`

## Tech Stack

| Component | Technology Used | Function |
| :--- | :--- | :--- |
| **SIEM / XDR** | Wazuh | Centralized Log Management & Threat Detection |
| **Cloud Provider** | Google Cloud Platform (Compute Engine) | Infrastructure Hosting (IaaS) |
| **OS (Server)** | Ubuntu Server 22.04 LTS | Host for the Manager |
| **Attack Tools** | Nmap / Hydra / Atomic Red Team | Simulating unauthorized access |

## Roadmap & Progress

- [ ] **Infrastructure:** Deploy Ubuntu instance on GCP (e2-medium).
- [ ] **Configuration:** Setup Firewall rules (Ingress/Egress) for ports 1514/55000.
- [ ] **Deployment:** Install Wazuh Manager & Filebeat.
- [ ] **Agent:** Connect local machine to the cloud server.
- [ ] **Testing:** Simulate Brute-force (SSH/RDP) and verify alerts on Dashboard.

---

<a name="español-abajo"></a>
# 🇪🇸 Implementación de SOC Híbrido (Wazuh)

## Sobre el Proyecto
Implementación práctica de un sistema **SIEM/XDR** desplegado en un entorno de Nube Híbrida.
Configuré un **Servidor Wazuh** en Google Cloud Platform (GCP) para monitorear, detectar y generar alertas de eventos de seguridad en una máquina local remota (simulando un endpoint corporativo).

**Objetivo:** Demostrar habilidades en Infraestructura Cloud, Análisis de Logs y Respuesta a Incidentes.

## Arquitectura

> **Servidor Cloud (Ubuntu):** Wazuh Manager + Elastic Stack  
> **Cliente Local (Windows/Linux):** Wazuh Agent

`[Endpoint Local]` --(Puerto Encriptado 1514)--> `[Internet]` --> `[Firewall GCP]` --> `[Wazuh Manager]`

## Tecnologías

| Componente | Tecnología | Función |
| :--- | :--- | :--- |
| **SIEM / XDR** | Wazuh | Gestión de logs y detección de amenazas |
| **Cloud Provider** | Google Cloud Platform | Alojamiento de infraestructura (IaaS) |
| **OS (Server)** | Ubuntu Server 22.04 LTS | Sistema base del servidor |
| **Herramientas** | Nmap / Hydra | Simulación de ataques controlados |

## Etapas y progreso del Proyecto

- [ ] **Infraestructura:** Desplegar instancia Ubuntu en GCP.
- [ ] **Configuración:** Reglas de Firewall para puertos 1514/55000.
- [ ] **Despliegue:** Instalación de Wazuh Manager.
- [ ] **Agente:** Conectar máquina local al servidor en la nube.
- [ ] **Pruebas:** Simular fuerza bruta y verificar alertas en el Dashboard.

---
*Created by [Tu Nombre/Usuario]*
