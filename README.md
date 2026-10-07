# 🤖 AI Job Application Agent

<p align="center">

<a href="https://n8n.io/" target="_blank">
<img src="https://img.shields.io/badge/N8N-WORKFLOW%20AUTOMATION-EA4B71?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n"/>
</a>

<a href="https://openai.com/" target="_blank">
<img src="https://img.shields.io/badge/OPENAI-AI%20AGENT-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI"/>
</a>

<a href="https://www.gmail.com/" target="_blank">
<img src="https://img.shields.io/badge/GMAIL-EMAIL%20AUTOMATION-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail"/>
</a>

<a href="https://slack.com/" target="_blank">
<img src="https://img.shields.io/badge/SLACK-NOTIFICATIONS-4A154B?style=for-the-badge&logo=slack&logoColor=white" alt="Slack"/>
</a>

<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank">
<img src="https://img.shields.io/badge/JAVASCRIPT-DATA%20PROCESSING-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
</a>

</p>

<p align="center">
  <strong>AI-powered job discovery, matching, scoring, and notification.</strong>
</p>

---

## 📌 Overview

**AI Job Application Agent** is an n8n workflow that automatically processes LinkedIn job alerts received through Gmail, analyzes each opportunity with an AI Agent, calculates a relevance score, and sends high-value matches to Slack.

Relevant jobs are also stored in a structured table for tracking and review.

---

## 🔄 How It Works

The workflow automatically moves each job opportunity through several stages:

```text
📧 Gmail
   ↓
🔍 Job Data Extraction
   ↓
🤖 AI Agent
   ↓
🎯 Relevance Scoring
   ↓
🔀 Score-Based Routing
   ↓
🔔 Slack Notification
   ↓
🗃️ Job Storage
```

The AI Agent evaluates each job based on your skills, technologies, experience, preferred roles, locations, and career goals.

---

## 🧠 AI Job Analysis

The AI Agent returns structured information for every analyzed job.

```json
{
  "score": 94,
  "relevance": "high",
  "job_title": "AI Automation Engineer",
  "company": "Example Company",
  "location": "Remote",
  "reason": "Strong match with n8n, AI agents, APIs and workflow automation.",
  "job_url": "https://www.linkedin.com/jobs/...",
  "recommended": true
}
```

The `score` represents how closely the job matches the configured profile.

### 🎯 Matching Criteria

```text
⚙️ n8n
🤖 AI Agents
🧠 RAG
🔌 APIs
🗄️ PostgreSQL
☁️ Supabase
🔄 Workflow Automation
```

### 📊 Match Score

```text
90 - 100  → 🟢 Excellent Match
70 - 89   → 🟢 Good Match
50 - 69   → 🟡 Medium Match
0 - 49    → 🔴 Low Match
```

---

## 🔔 Slack Notifications

When a job reaches the configured score threshold, the workflow sends a concise notification to Slack.

Example:

```text
🚀 NEW JOB MATCH

AI Automation Engineer
Company: Example Company
Location: Remote

🎯 Match Score: 94%

💡 Why:
Strong match with n8n, AI agents,
APIs and workflow automation.

🔗 Job URL
```

This makes it easier to identify high-quality opportunities without manually reviewing every job alert.

---

## 🗃️ Job Storage

Relevant opportunities are stored for later tracking and review.

| Field       | Example                    |
| ----------- | -------------------------- |
| Job Title   | AI Automation Engineer     |
| Company     | Example Company            |
| Location    | Remote                     |
| Match Score | 94                         |
| Relevance   | High                       |
| Reason      | Strong AI automation match |
| Job URL     | LinkedIn URL               |
| Source      | LinkedIn                   |
| Date        | 2026-10-07                 |

---

## 🛠️ Tech Stack

| Technology    | Role                               |
| ------------- | ---------------------------------- |
| ⚡ n8n         | Workflow automation                |
| 🤖 OpenAI     | AI-powered job analysis            |
| 📧 Gmail      | Job alert ingestion                |
| 🔔 Slack      | Job notifications                  |
| 💻 JavaScript | Data processing and transformation |
| 💼 LinkedIn   | Job opportunity source             |

---

## ✨ Key Features

* 📧 Automatic LinkedIn job alert processing
* 🤖 AI-powered job analysis
* 🎯 Personalized relevance scoring
* 🔀 Automatic score-based routing
* 🔔 Real-time Slack notifications
* 🗃️ Structured job storage
* ⚡ Fully automated workflow

---

## 🚀 Setup

### 1. Import the Workflow

Import the provided n8n workflow JSON into your n8n instance.

```text
n8n
→ Workflows
→ Import from File
```

### 2. Configure Credentials

Connect the required credentials:

```text
📧 Gmail OAuth
🤖 OpenAI API
🔔 Slack
```

### 3. Configure the AI Agent

Update the AI Agent instructions to match your own profile:

```text
Skills
Technologies
Experience
Preferred Roles
Locations
Career Goals
```

### 4. Set the Score Threshold

Configure the Switch node according to your preferred relevance level.

Example:

```text
Score >= 70
      ↓
🔔 Send to Slack
      ↓
🗃️ Store in Job Table
```

---

## 📁 Repository Structure

```text
ai-job-application-agent/
│
├── README.md
│
├── workflow/
│   └── ai-job-application-agent.json
│
├── prompts/
│   └── job-matching-prompt.md
│
├── examples/
│   └── example-job-output.json
│
├── screenshots/
│   └── workflow.png
│
├── .gitignore
└── LICENSE
```

---

## 📸 Workflow Preview

<p align="center">
  <img src="./screenshots/workflow.png"
       alt="AI Job Application Agent Workflow"
       width="100%"/>
</p>

---

## 🔐 Security

Never commit API keys, OAuth tokens, passwords, or other credentials to the repository.

Use n8n's credential management system instead.

```text
❌ Hardcoded credentials

OPENAI_API_KEY=xxxxxxxx
SLACK_TOKEN=xxxxxxxx

✅ n8n Credentials
```

---

## 🔮 Future Improvements

* 🔍 Duplicate job detection
* 📄 CV-to-job matching
* ✍️ Automated cover letter generation
* 📊 Application status tracking
* 📅 Daily job digest
* 🌐 Multi-source job monitoring
* 🎯 Advanced weighted scoring
* 📋 Automatic application tracking

---

## 🏁 Conclusion

This project combines **n8n automation and AI** to turn the traditional job-search process into an automated system.

Instead of manually checking every job alert, the workflow automatically **collects, analyzes, scores, filters, notifies, and stores** relevant opportunities.

<p align="center">
  <strong>🚀 Built with n8n, AI Agents, and automation.</strong>
</p>
