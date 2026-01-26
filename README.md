# Living AI Support & Escalation System

## Overview

This project implements a **Living AI Support System** using **n8n** as the orchestration engine and **Gemini (LLM)** as the core intelligence layer. It simulates a scalable, production-grade support desk that:

• Qualifies incoming user requests  
• Uses a multi-agent AI Council for decision-making  
• Automatically resolves simple issues  
• Escalates complex or sensitive cases  
• Logs all activity for optimization  
• Self-improves using a feedback loop  
• Dynamically generates new workflows on demand  

The system is intentionally **industry-agnostic** and demonstrates how AI can be embedded into operational workflows with governance, human-in-the-loop safety, and continuous learning.

---

## System Architecture

The system is composed of **three independent but connected workflows**:

User
↓
[Core Support System]
├── Classifier
├── AI Council
├── Decision Engine
├── Auto-response
└── Escalation Actions
↓
[Metrics Logging]

[Self Optimizer] ←── reads metrics
↓
Improvement Suggestions
↓
Human Approval
↓
Rules Memory

[Workflow Generator] ←── triggered by user
↓
Workflow JSON Generation
↓
Validation
↓
Human Approval
↓
Registry


---

<!-- ## Architecture Diagram

> Placeholder: `/docs/architecture.png`  
> Placeholder: `/docs/architecture.drawio` -->

---

## Repository Structure

AI-Living-Support-System/
├── exports/
│ ├── core-support-system.json
│ ├── optimizer-workflow.json
│ └── generator-workflow.json
│
├── README.md
│
├── demo/
│ ├── demo-script.md
│ ├── test-prompts.txt
│ └── screenshots/
│
└── docs/
├── architecture.txt
└── system-thinking.md


---

## Workflow 1: Core Support System

### Purpose:
Handles real-time chat interactions, classifies issues, consults AI agents, and decides whether to auto-resolve or escalate.

---

### End-to-End Flow

User
↓
Chat Trigger (Streaming)
↓
Gemini Classifier
↓
Parse JSON
↓
├── Understanding Agent
├── Resolution Agent
└── Escalation Agent
↓
Merge (Combine Mode)
↓
Decision Brain
↓
├── Auto Response
└── Escalation Path
↓
Slack / HubSpot (placeholder)
↓
Google Sheets Logging



---

### AI Council Design

The system uses **three specialized AI agents**:

| Agent | Responsibility |
|------|---------------|
| Understanding Agent | Interprets user intent |
| Resolution Agent | Suggests best response |
| Escalation Agent | Decides if human intervention is required |

This simulates **committee-style reasoning** instead of a single black-box decision.

---

### Escalation Logic

Escalation is triggered only when:

• Billing or payments involved  
• Access or technical failure  
• User is urgent or angry  
• Legal / security risk  

This ensures conservative, human-in-the-loop safety.

---

## Workflow 2: Self-Optimizer

### Purpose
Creates a **living system** that continuously improves its own logic.

---

### Flow

Schedule Trigger
↓
Read Metrics (Google Sheets)
↓
Optimizer Agent (Gemini)
↓
Improvement Proposal
↓
Human Approval Gate
↓
Rules Memory (Sheets)


---

### What It Optimizes

• Response quality  
• Escalation thresholds  
• FAQ generation  
• Classification prompts  
• Decision logic  

This simulates **AI governance** and **continuous learning**.

---

## Workflow 3: Dynamic Workflow Generator

### Purpose
Allows the system to **create new workflows on demand** using AI.

---

### Flow

User Command
↓
Generator Agent
↓
Workflow JSON
↓
Validator
↓
Human Approval
↓
Registry
↓
Deployment Simulation


---

### Example Commands

• "Create a refund handling flow"  
• "Create a follow-up support workflow"  
• "Build an onboarding automation"  

---

## How to Run Locally

### Requirements

• n8n (self-hosted or cloud)  
• Gemini API key  
• Google Sheets OAuth  

---

### Importing Workflows

1. Open n8n
2. Click **Workflows**
3. Select **Import from File**
4. Import JSON from `/exports/`

---

### Credentials Setup

| Service | Status |
|--------|--------|
| Gemini | Required |
| Google Sheets | Required |
| Slack | Placeholder |
| HubSpot | Placeholder |

---

## Demo Instructions

See: `/demo/demo-script.md`

---

## Test Prompts

See: `/demo/test-prompts.txt`

---

## Governance & Safety

• No auto-deploy of generated workflows  
• Human approval gates  
• Conservative escalation  
• Full audit trail  
• Versioned improvements  

---

## Metrics Tracked

• Category  
• Urgency  
• Escalation rate  
• Priority  
• Message content  
• Resolution path  

These are stored in Google Sheets and used by the optimizer.

---

## JD Skill Mapping

| JD Requirement | Where Implemented |
|---------------|------------------|
Ecosystem Orchestration | n8n workflows
AI Councils | Multi-agent architecture
Dynamic Decisioning | Escalation agent
Self Optimization | Optimizer workflow
Governance | Approval gates
Scalability | Modular workflows
Deployment | JSON exports

---

<!-- ## Live Prototype

> Placeholder: Public n8n URL  
> Placeholder: Demo video  -->

---

## Future Extensions

• Real CRM integration  
• SLA tiers  
• Multi-tenant support  
• Cost-based routing  
• Regional failover  
• Analytics dashboard  

---

### PC: @Akshat Tripathi
