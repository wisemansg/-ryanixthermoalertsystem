#  Ryanix ThermoAlert System 🔥

<p align="center">
  <img src="https://img.shields.io/badge/n8n-EA4B71?logo=n8n&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white" />
  <img src="https://img.shields.io/badge/Gmail-EA4335?logo=gmail&logoColor=white" />
  <img src="https://img.shields.io/badge/Google%20Calendar-4285F4?logo=googlecalendar&logoColor=white" />
  <img src="https://img.shields.io/badge/Telegram-26A5E4?logo=telegram&logoColor=white" />
  <img src="https://img.shields.io/badge/PagerDuty-06AC38?logo=pagerduty&logoColor=white" />
  <img src="https://img.shields.io/badge/Discord-5865F2?logo=discord&logoColor=white" />
  <img src="https://img.shields.io/badge/Industrial%20Monitoring-B22222?logo=datadog&logoColor=white" />
  <img src="https://img.shields.io/badge/AI%20Automation-8A2BE2?logo=robotframework&logoColor=white" />
  <img src="https://img.shields.io/badge/Workflow%20Orchestration-FF6B00?logo=apacheairflow&logoColor=white" />
</p>

---
**Automated Critical Machine Monitoring & Multi-Channel Emergency Response Workflow**

The Ryanix ThermoAlert System is an automated workflow designed to monitor machine telemetry and respond to critical alerts, such as high temperatures. This system integrates AI-driven decision-making with multiple notification channels to ensure rapid response and prevent potential failures in industrial equipment. The name of the imaginary company is Ryanix Solutions.

## 🌟 Summary

This workflow activates on a scheduled trigger to check machine telemetry data, such as temperature and status. Upon detecting a critical condition (for example, 92°C on Machine ACME-01), it executes a series of actions:

- Sending professional email alerts via Gmail
- Scheduling urgent repairs in Google Calendar
- Dispatching push notifications through Telegram
- Creating high-priority incidents in PagerDuty
- Broadcasting team updates on Discord

An AI agent powered by OpenAI processes the telemetry and coordinates these tasks, with simple memory to retain context for ongoing monitoring.

## 👥 Intended Users

- Industrial maintenance teams that require immediate notifications for equipment issues
- Operations managers overseeing machinery in manufacturing or data centers
- IT administrators building automated alert systems for hardware monitoring

## ⚙️ Functionality and Operation

### ⏰ Trigger Activation  
A schedule trigger initiates the workflow at set intervals to review current machine telemetry (e.g., Machine ID: ACME-01, Temperature: 92°C, Status: Critical).

### 🤖 AI Processing  
The OpenAI Chat Model analyzes the telemetry data and generates tailored responses for each notification channel.

### 📧 Gmail Notification  
A formal email is sent to the manager, featuring:

- A proper salutation
- Structured paragraphs
- A section titled 'Immediate Actions Required' with five bulleted steps, such as emergency stop, cooling activation, and isolation procedures
  
![View](./ryanixassets/Email%20Response.jpeg)

### 🗓️ Google Calendar Scheduling  
An event is created with details including:

- **Title**: URGENT: Emergency Repair - Machine ACME-01
- **Description**: Critical temperature alert (92°C) detected. Maintenance required to prevent system failure.
- **Location**: Grünerløkka, Oslo, Norway

![View](./ryanixassets/Calendar%20Response%201.jpeg)
![View](./ryanixassets/Calendar%20Response%202.jpeg)

### 🚨 Telegram Notification  
A concise urgent message is sent:

- 'CRITICAL ALERT: Machine ACME-01 is at 92°C. Emergency repair scheduled. Check email for action steps.'

![View](./ryanixassets/Telegram%20Response.jpeg)

### 🔥 PagerDuty Incident Creation  
A high-priority incident is logged with:

- **Title**: [CRITICAL] ACME-01 Overheat (92°C)
- **Description**: Industrial telemetry indicates a critical temperature threshold has been exceeded.
- **Urgency**: High

![View](./ryanixassets/Pagerduty%20Response.jpeg)

### 💬 Discord Update  
A formatted message is posted to the team channel:

- CRITICAL SYSTEM ALERT
- Device: Machine ACME-01
- Condition: 92°C (Critical)
- Status: Emergency repair scheduled in Google Calendar. PagerDuty incident triggered.

![View](./ryanixassets/Discord%20Response.jpeg)

### 🧠 Memory Management  
Simple Memory stores recent telemetry context to support follow-up actions in subsequent runs.

## 🛠️ Setup Instructions

### 🚀 n8n Deployment  
Install n8n on a self-hosted server or through a cloud service like Coolify or Docker.

### 🔑 Credential Configuration  
Set up the following credentials in n8n:

- OAuth2 credentials for Gmail and Google Calendar via Google Cloud Console
- API keys for OpenAI, Telegram, PagerDuty, and Discord in the n8n credentials section

### 📥 Workflow Import  
In the n8n interface:

- Navigate to Workflows
- Select Import
- Insert the workflow JSON configuration
- Verify that all credential references align with the established IDs for Gmail, OpenAI, and other services

### 🧪 Testing Procedure  
- Activate the workflow manually or simulate telemetry data
- Observe logs to confirm notifications across channels and incident creation

![View](./ryanixassets/Ryanix%20Workflow.png)

## ✅ System Requirements

- n8n platform (self-hosted or cloud-based)
- Enabled APIs for Gmail, Google Calendar, and Google Cloud project
- OpenAI API access for chat and embedding models
- Telegram bot token for messaging
- PagerDuty account with API integration
- Discord webhook for channel postings

## 🔧 Customization Options

### ⏱️ Modify Trigger Schedule  
Adjust the Schedule Trigger node to change polling frequency, such as from daily to hourly.

### ✍️ Update Notification Content  
Edit the OpenAI Chat Model prompt to alter:

- Email structure
- Incident details
- Message phrasing

### 📊 Expand Telemetry Inputs  
Integrate additional data sources in the AI Agent node, such as:

- Humidity
- Vibration metrics
- Other relevant sensor data

### 🧬 Adjust Memory Settings  
Enhance the Simple Memory node to retain more historical data for complex monitoring scenarios.

### 🌐 Add Integration Nodes  
Incorporate extra n8n nodes for services like:

- Slack
- SMS
- Other notification platforms after the core actions to broaden alert distribution

---

Built with reliability and clarity in mind by Wiseman.S
