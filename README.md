# Building an AI Cybersecurity Agent with n8n & Wazuh (Agentic AI Security)

## Overview

This project demonstrates how to build an **AI-powered Cybersecurity Agent** using n8n, Wazuh, and Agentic AI concepts. The agent automatically monitors security logs, detects anomalies, analyzes threats using AI, and performs automated response actions.

The goal is to create an **intelligent, automated Security Operations Center (SOC) assistant** that reduces manual work and improves threat detection speed.

---

## Objectives

* Automate security monitoring using Wazuh SIEM
* Use n8n to orchestrate workflows and automation
* Integrate AI to analyze and classify threats
* Detect anomalies in logs automatically
* Trigger automated alerts and responses
* Build an Agentic AI system that can make security decisions

---

## Architecture

```
Wazuh Agent → Wazuh Manager → n8n Workflow → AI Model → Decision Engine → Alert / Response
```

### Components

1. **Wazuh Agent**

   * Collects logs from endpoints
   * Sends security events to Wazuh Manager

2. **Wazuh Manager**

   * Processes logs
   * Detects threats and generates alerts

3. **n8n Automation**

   * Receives alerts from Wazuh
   * Sends data to AI model
   * Executes automated workflows

4. **AI Agent**

   * Analyzes alerts
   * Classifies threat severity
   * Suggests or executes response actions

5. **Response System**

   * Sends alerts via Email / Telegram / Slack
   * Logs incidents
   * Can trigger automated defense actions

---

## Features

* Real-time threat monitoring
* AI-based anomaly detection
* Automated incident response
* Workflow automation using n8n
* Integration with Wazuh SIEM
* Agentic AI decision making
* Scalable and customizable architecture

---

## Technologies Used

* Wazuh (SIEM & XDR)
* n8n (Workflow Automation)
* AI / LLM (OpenAI or local model)
* Python (optional for AI processing)
* REST API
* JSON
* Linux / Windows Endpoint

---

## Installation

### Step 1: Install Wazuh

Install Wazuh Manager and Agent:

```
https://documentation.wazuh.com/current/installation-guide/index.html
```

Install agent on endpoint and connect to manager.

---

### Step 2: Install n8n

Using npm:

```bash
npm install -g n8n
n8n start
```

Or using Docker:

```bash
docker run -it --rm \
-p 5678:5678 \
n8nio/n8n
```

---

### Step 3: Configure Wazuh Integration with n8n

* Use webhook in n8n
* Configure Wazuh to send alerts via webhook
* Parse alert JSON

---

### Step 4: Add AI Processing

Use AI via:

* OpenAI API
  or
* Local AI model

Example logic:

* Input: Alert log
* Output: Threat level (Low / Medium / High)

---

### Step 5: Create Automated Response

Example actions:

* Send Email alert
* Send Telegram alert
* Log incident
* Block IP (optional)

---

## Workflow Example

1. Wazuh detects suspicious activity
2. Alert sent to n8n webhook
3. n8n sends alert to AI
4. AI analyzes threat
5. n8n decides action
6. Alert sent to security team

---

## Project Structure

```
AI-Cybersecurity-Agent/
│
├── workflows/
│   └── n8n-workflow.json
│
├── scripts/
│   └── ai-analysis.py
│
├── docs/
│   └── architecture.png
│
├── README.md
└── config/
    └── wazuh-config.json
```

---

## Use Cases

* SOC automation
* Threat detection automation
* AI-powered SIEM
* Incident response automation
* Security monitoring

---

## Future Improvements

* Add automatic IP blocking
* Train custom AI model
* Add dashboard visualization
* Integrate with more SIEM tools
* Add self-learning AI agent

---

## Requirements

* Wazuh installed
* n8n installed
* Node.js
* AI API key (optional)
* Linux or Windows system

---

## Author

Mayur Pawar
Cybersecurity Student | AI Security Enthusiast

GitHub: https://github.com/yourusername

---

## License

This project is for educational purposes.
