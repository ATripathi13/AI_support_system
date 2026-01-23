# Demo Script — Living AI Support & Escalation System

## Purpose of Demo

This demo showcases an end-to-end intelligent support workflow that:

• Accepts real-time user input  
• Classifies intent using an LLM  
• Uses a multi-agent AI Council  
• Makes escalation decisions  
• Logs metrics  
• Self-optimizes  
• Generates workflows dynamically

**Provides real time user growth**

This demonstrates **decision intelligence**, **automation**, **AI governance**, and **scalable system design**.

---

## Demo Setup Checklist

Before recording or presenting:

✔ n8n is running  
✔ Core workflow is active  
✔ Gemini API is connected  
✔ Google Sheets is connected  
✔ Chat Trigger is public  
✔ Sheets logging is visible  

---

## Demo Flow (Step-by-Step)

---

## Step 1 — Open the Chat UI

Open the public Chat Trigger URL.

Say:

> “This is the AI Support System. I’ll now ask a few questions.”

---

## Step 2 — Test Auto-Resolution (No Escalation)

### Prompt:

What are your working hours?


### Expected Behavior:
• Classified as `General`  
• Low urgency  
• Auto-response generated  
• NOT escalated  
• Logged to Sheets  

### Say:
> “This is a simple informational query. The system classifies it, uses the AI council, and automatically responds without escalation.”

---

## Step 3 — Test Technical Escalation

### Prompt:

I cannot log into my account and need urgent help.


### Expected Behavior:
• Classified as `Technical`  
• High urgency  
• Escalation triggered  
• Slack alert (placeholder)  
• HubSpot ticket (placeholder)  
• Logged to Sheets  

### Say:
> “This is a critical access issue. The escalation agent flags it for human review.”

---

## Step 4 — Test Billing Escalation

### Prompt:

Create a workflow for handling refund requests.


### Expected Behavior:
• Generator agent produces workflow JSON  
• Validator checks syntax  
• Approval gate appears  

### Say:
> “This shows how the system can design new workflows on demand.”

---

## Step 8 — Wrap-Up

### Say:

> “This system demonstrates how AI can be embedded into operations, not just as a chatbot, but as a living, adaptive, and governed system.”

---

## What This Demo Proves

✔ End-to-end automation  
✔ AI-driven decisioning  
✔ Multi-agent reasoning  
✔ Governance and safety  
✔ Continuous learning  
✔ Scalable design  

---
