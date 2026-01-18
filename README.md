# ai-email-security-n8n
AI-powered Gmail security and priority automation built with n8n
<br>
<br>
# AI-Powered Email Security & Priority Automation (n8n)

This project is an AI-driven automation built using **n8n** that analyzes incoming Gmail messages and classifies them as **SCAM**, **IMPORTANT**, or **NORMAL**, then takes automated actions accordingly.

## 🚀 Features
- Detects phishing and scam emails using LLM reasoning
- Identifies important emails (interviews, exams, bank alerts)
- Automatically organizes normal emails
- Sends real-time WhatsApp alerts for scam and important emails
- Uses hybrid AI + rule-based decision logic

## 🧠 How It Works
1. Gmail trigger captures new incoming emails
2. Email content is extracted and normalized
3. LLM classifies the email (SCAM / IMPORTANT / NORMAL)
4. Output is normalized for reliability
5. Conditional routing handles actions:
   - Scam → Spam + WhatsApp alert
   - Important → Label + WhatsApp alert
   - Normal → Label + archive

## 🛠️ Tech Stack
- n8n (low-code automation)
- Large Language Models (LLMs)
- Gmail API
- WhatsApp API (Twilio)

## 📁 Repository Structure
