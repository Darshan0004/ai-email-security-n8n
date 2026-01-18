# ai-email-security-n8n
AI-powered Gmail security and priority automation built with n8n
<br>
<br>
# AI-Powered Email Security & Priority Automation (n8n)

This project is a **production-style email automation system** built using **n8n** and **LLM-based intelligence**.  
It automatically analyzes incoming Gmail messages, classifies them, and takes appropriate actions to improve **security** and **productivity**.

The system focuses on **real-world phishing detection**, **important email prioritization**, and **automated inbox organization**.

---

## 🚀 Key Features

- AI-based phishing and scam detection  
- Identification of important emails (interviews, exams, bank alerts, deadlines)  
- Automatic organization of normal emails  
- Real-time WhatsApp notifications for:
  - Scam emails
  - Important emails  
- Hybrid **AI + rule-based decision logic**
- Fully automated, event-driven workflow

---

## 🧠 Problem This Solves

Modern inboxes suffer from:
- Phishing and scam emails disguised as jobs, banks, or official messages
- Important emails getting lost among newsletters and promotions
- Manual effort required to filter and monitor inboxes

This project solves these problems by **automating email understanding and action**, rather than just filtering by keywords.

---

## 🏗️ System Architecture

### High-Level Flow

Gmail Inbox
│
▼
Gmail Trigger (New Email)
│
▼
Extract & Normalize Email Data
(from, subject, snippet)
│
▼
LLM Classification
(SCAM / IMPORTANT / NORMAL)
│
▼
Normalize AI Output
(trim + uppercase)
│
▼
Decision Engine
├── SCAM
│ ├── Move to Spam
│ └── WhatsApp Alert
│
├── IMPORTANT
│ ├── Add Important Label
│ └── WhatsApp Alert
│
└── NORMAL
├── Add Normal Label
└── Archive


---

## 🔍 Design Decisions

### 1. LLM-Based Classification
Instead of keyword matching, the system uses an LLM to detect:
- Social engineering
- Urgency and fear tactics
- Impersonation attempts
- Fake job and internship scams

This significantly improves phishing detection accuracy.

---

### 2. Output Normalization
AI output is normalized using:


This prevents hidden characters (like newlines) from breaking automation logic and ensures **deterministic decision-making**.

---

### 3. Deterministic Routing
All decisions are handled using **IF nodes**, making the workflow:
- Transparent
- Debuggable
- Easy to extend

---

### 4. Event-Driven Automation
The system runs automatically on **new incoming emails**, without polling or manual triggers.

---

## 🛠️ Tech Stack

- **n8n** – Low-code workflow automation
- **LLMs** – Intelligent email classification
- **Gmail API** – Email ingestion and labeling
- **WhatsApp API (Twilio)** – Real-time notifications
- **Hybrid AI + rule-based logic**

---

## 📁 Repository Structure

ai-email-security-n8n/
│
├── workflows/
│ └── email_security_workflow.json
│
├── docs/
│ └── architecture.md
│
├── README.md
└── .gitignore
