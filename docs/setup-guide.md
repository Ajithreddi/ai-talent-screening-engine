# 📘 Setup Guide – AI Talent Screening Engine (AI-TSE)

This guide explains how to set up, configure, and run the AI Talent Screening Engine project.
It includes environment setup, workflow deployment, and integration steps for Telegram, Gmail, Google Sheets, and n8n.

🧱 1. Prerequisites

Before starting, ensure you have:

✔ n8n account (Cloud or Self-hosted)
✔ Telegram Bot Token
✔ Google Sheets API access
✔ Gmail App Password
✔ Google Gemini API key
✔ Git installed
✔ Conda or Python installed (optional for development)
📂 2. Project Folder Structure
AI-Talent-Screening-Engine/
│
├── README.md
├── LICENSE
├── .gitignore
├── CHANGELOG.md
│
├── n8n-workflows/
│   └── ai-tse-workflow.json
│
├── docs/
│   ├── setup-guide.md
│   ├── project-description.txt
│   ├── architecture.png
│   └── workflow-diagram.png
│
├── assets/
│   ├── ARSS_image.png
│   └── icons/
│
└── bot/
    └── BotLink.txt

🤖 3. Telegram Bot Setup
1. Open Telegram
2. Search for BotFather
3. Send command:
/newbot

4. Enter a name and username
5. Copy your Bot Token

Add it to your n8n Telegram Trigger node under:

Credentials → Telegram Bot API

📩 4. Gmail Setup (For Sending Emails)

Gmail does not allow password login from apps.
You must create an App Password.

Steps:

Go to Google Account → Security

Turn on 2-Step Verification

Go to App Passwords

Create a password for:

App: Mail
Device: Other (AI-TSE)


Save the generated 16-character password

Add it to Gmail credentials in n8n

📊 5. Google Sheets Setup
1. Create a Google Sheet

With two tabs:

Accepted
Rejected

2. Share it with your Google API service account (if applicable)
3. Add credentials inside n8n:
Google Sheets → OAuth2 / Service Account

🧠 6. Google Gemini API Setup
1. Go to Google AI Studio
2. Generate an API key
3. Add it to n8n → Gemini Node Credentials
4. Select Gemini model in your AI Screening nodes
🔧 7. Importing the Workflow in n8n
1. Open n8n
2. Go to Workflows
3. Click Import
4. Upload:
n8n-workflows/ai-tse-workflow.json

5. Verify all credentials inside nodes:

Telegram

Gmail

Google Sheets

Gemini API

🔁 8. Running the Workflow

Once imported:

✔ Enable the workflow
✔ Send a test resume to your Telegram Bot
✔ Monitor in n8n Executions
✔ Confirm:

Resume text extraction

AI evaluation

Acceptance/rejection

Email sent

Sheet updated

Telegram summary delivered

🧪 9. Testing

Test scenarios:

➤ Single PDF resume
➤ Multiple resumes in one message
➤ ZIP file containing resumes
➤ Invalid file
➤ Empty message
➤ Large resume (5 MB+)
➤ Unstructured resume

Make sure all branches behave correctly.

🚀 10. Deployment / Production Tips
✔ Keep a backup of your workflow JSON
✔ Enable logging in n8n
✔ Add error notifications (optional)
✔ Keep Sheets under size limit
✔ Use Gemini model with structured output
🎯 11. Updating the System

Whenever you update nodes:

git add .
git commit -m "Update workflow"
git push


Keep a version history in CHANGELOG.md.

📞 Support & Contact

For bot access:
🔗 https://t.me/chinn777bot

For development or help, contact your project maintainer.