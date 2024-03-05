# Enhanced SOC-Home-Lab-Wazuh-Shuffle-TheHive Documentation

This document serves as a comprehensive guide for setting up a home lab environment that mimics a Security Operations Center (SOC) using Wazuh for threat detection and monitoring, Shuffle for orchestrating workflows between tools, and TheHive as an incident response platform. This setup aims to replicate a professional SOC environment for educational and testing purposes.

## Objective

To create a scalable and replicable SOC environment within a home lab setting, facilitating the development and testing of cybersecurity practices, incident response workflows, and threat detection mechanisms. This setup is designed to handle logs and alerts from client devices, automate response workflows, and manage incident responses effectively.

## Components Overview

- **Clients (Windows Laptops)**: Source of logs and alerts simulating user activities and potential threat vectors.
- **Wazuh Server (Digital Ocean)**: Centralized security monitoring service for threat detection, data aggregation, and log analysis.
- **Shuffle Orchestrator (Digital Ocean)**: Automates and integrates workflows between the SOC tools, enhancing response times and efficiency.
- **TheHive (Digital Ocean)**: Incident response platform that provides a comprehensive case management solution for responding to security incidents.

## Architecture Diagram

```
    [ Clients (Windows Laptops) ]
        |   ^
        |   | (Logs and alerts)
        v   |
    [ Wazuh Server (Digital Ocean) ] --- (Threat detection, Monitoring)
        |
        | (Alerts for incidents)
        v
    [ Shuffle Orchestrator (Digital Ocean) ] --- (Automates workflows between tools)
        |
        | (Automated incident response workflows)
        v
    [ TheHive (Digital Ocean) ] --- (Incident Response Platform)
```

## Prerequisites

- **Digital Ocean Account**: Required to host the Wazuh Server, Shuffle Orchestrator, and TheHive.
- **Windows Laptops**: Client devices to monitor and from which logs and alerts will be collected.
- **Internet Connection**: Necessary for communication between components and access to Digital Ocean services.

## Setup Steps

1. **Wazuh Server Setup**:
    - Deploy a virtual server instance on Digital Ocean.
    - Install and configure Wazuh following the official Wazuh documentation.
    - Ensure proper log forwarding from Windows clients to the Wazuh server.

2. **Shuffle Orchestrator Setup**:
    - Deploy another virtual server instance on Digital Ocean.
    - Install Shuffle Orchestrator and configure it to communicate with the Wazuh server.
    - Define automated workflows for incident detection and response.

3. **TheHive Setup**:
    - Utilize a separate Digital Ocean instance for TheHive.
    - Install and configure TheHive to receive alerts from Shuffle Orchestrator.
    - Set up case management workflows for handling incidents reported by Wazuh.

## Useful Tips

1. **Monitoring Windows Services**:
    - To check running services: Go to Start, type "services".
    - To access application and service logs: Go to Start, type "event viewer", and click on "application and service logs".

2. **Identifying Public IP Address**:
    - To find out your public IP, visit [whatismyipaddress.com](https://whatismyipaddress.com).

