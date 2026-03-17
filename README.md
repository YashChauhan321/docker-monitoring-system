# Docker Monitoring & Alerting System on AWS

## Overview

This project implements a **Docker-based monitoring and alerting platform** deployed on an AWS EC2 instance using only **AWS Free Tier resources**.

The system monitors **Docker containers and host infrastructure metrics** in real time using **Prometheus, Grafana, cAdvisor, and Node Exporter**.

It provides **visual dashboards and alert rules** to help detect performance issues in containerized environments.

---

## Architecture

Docker Containers

* Nginx (Sample Application)
* cAdvisor (Container Metrics)
* Node Exporter (Host Metrics)
* Prometheus (Metrics Collection)
* Grafana (Visualization & Alerting)

Monitoring Flow:

Application Containers
↓
cAdvisor / Node Exporter
↓
Prometheus (Metrics Scraping)
↓
Grafana (Dashboards & Alerts)

---

## Technologies Used

* AWS EC2 (Free Tier)
* Docker
* Docker Compose
* Prometheus
* Grafana
* cAdvisor
* Node Exporter
* Linux (Ubuntu)

---

## Features

* Real-time Docker container monitoring
* Host infrastructure monitoring
* Prometheus metrics collection
* Grafana dashboards for visualization
* Alert rules for detecting high resource usage
* Fully containerized monitoring stack
* One-command deployment using Docker Compose

---

## Project Structure

docker-monitoring-system

* docker-compose.yml
* prometheus.yml
* alerts/

  * alert_rules.yml
* grafana/

  * provisioning/

    * datasource.yml
* README.md

---

## Setup Instructions

### 1 Clone the repository

git clone https://github.com/YOUR_USERNAME/docker-monitoring-system.git

cd docker-monitoring-system

---

### 2 Start the monitoring stack

docker-compose up -d

---

### 3 Verify running containers

docker ps

You should see the following containers running:

* nginx
* cadvisor
* node-exporter
* prometheus
* grafana

---

## Access the Services

Grafana Dashboard
http://SERVER_IP:3000

Prometheus Metrics
http://SERVER_IP:9090

cAdvisor Container Metrics
http://SERVER_IP:8080

---

## Grafana Login

Username: admin
Password: admin

---

## Monitoring Metrics

Prometheus collects metrics from:

* cAdvisor (Docker container metrics)
* Node Exporter (Host metrics)

Example monitored metrics:

* CPU usage
* Memory usage
* Container resource consumption
* Network activity
* Disk usage

---

## Alerting

Prometheus alert rules detect abnormal resource usage such as:

* High CPU usage
* High memory consumption

Alerts can be extended to integrate with:

* Email
* Slack
* Incident management systems

---

## Deployment Environment

This project was deployed on:

AWS EC2 (t3.micro – Free Tier)
Ubuntu 22.04
Docker Engine

---

## Future Improvements

* Add Alertmanager for alert routing
* Integrate Slack/email notifications
* Deploy monitoring stack on Kubernetes
* Add container auto-restart and self-healing

---

## Author

Yash Chauhan
