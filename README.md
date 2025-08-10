# WhatsApp-Driven Google Drive Assistant (n8n Workflow)

## Overview

This n8n workflow enables controlling Google Drive via WhatsApp commands through Twilio Sandbox.  
You can list, delete, move, and get AI-powered summaries of files in your Google Drive folders using simple WhatsApp text commands.  
The workflow uses OpenAI GPT-4o for document summarization, Google Drive API for file management, and Twilio WhatsApp Sandbox for messaging.

---

## Features

- WhatsApp commands via Twilio Sandbox  
- Google Drive OAuth2 integration (user-scoped)  
- Supported commands:  
  - `LIST /folder`  
  - `DELETE /folder/file` (with confirmation keyword)  
  - `MOVE /folder/file /target-folder`  
  - `SUMMARY /folder` (AI-generated bullet summaries)  
- Audit logging of all actions  
- Safety checks to prevent accidental mass deletion  
- ngrok for local webhook tunneling

---

## Setup Instructions

### Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop) installed and running  
- [ngrok](https://ngrok.com/) account and installed CLI  
- Twilio account with WhatsApp Sandbox enabled  
- Google Cloud project with OAuth 2.0 credentials (Client ID & Secret)  
- OpenAI API key

---

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/whatsapp-google-drive-assistant.git
cd whatsapp-google-drive-assistant
