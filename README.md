## AI Talent Screening Engine (AI-TSE)

### Your smart HR assistant for resume analysis.
🔗 Telegram Bot: https://t.me/chinn777bot



🚀 Overview

AI Talent Screening Engine (AI-TSE) is a fully automated hiring assistant that processes resumes, extracts structured information, evaluates candidates using AI, and classifies them as Accepted or Rejected.
It eliminates manual resume screening and significantly speeds up the IT recruitment cycle.

This system integrates:

*  Telegram bot for resume uploads 
*  n8n workflow automation 
*  Google Gemini LLM for AI evaluation 
*  Google Sheets for storing results 
*  Gmail for acceptance/rejection notifications 


🧠 Features

✔ Automated Resume Intake

Upload resumes directly through Telegram.

✔ Multi-file Support

Supports PDF, DOCX, ZIP, and multi-resume uploads.

✔ Resume Processing

Automated routing, decompression, splitting, and text extraction.

✔ AI Screening

Gemini LLM analyzes each resume and extracts:

*  Skills 
*  Experience 
*  Summary 
*  Strengths & weaknesses 
*  Match score 
*  Final recommendation 

✔ Automated Decision Logic

System classifies candidates into Accepted or Rejected.

✔ Notifications

Sends acceptance or rejection emails and Telegram summaries.

✔ Google Sheets Storage

Stores Accepted and Rejected candidates separately for HR tracking.




🧱 Architecture Layers

🔵 1. Input Layer

Manages candidate messages and resume uploads.

*  Telegram Intake Trigger 
*  Message Type Check 
*  Default Reply to User 


🟠 2. Resume Processing Layer

Handles all file operations.

*  Resume File Router 
*  Resume File Decompressor 
*  Resume Splitter 
*  Resume Text Extractor 
*  Multi-Resume Loop Processor 


🟣 3. AI Screening Layer

Core intelligence of the system.

*  AI Screening Agents 
*  Gemini Models 
*  Structured Output Parsers 
*  Normalized Resume Fields 


🟢 4. Decision Logic Layer

Applies acceptance or rejection logic.

*  Candidate Decision Check 
*  Accepted Candidates Sheet 
*  Rejected Candidates Sheet 


🟦 5. Notification Layer

Sends final outputs and updates storage.

*  Send Acceptance Email 
*  Send Rejection Email 
*  Combine Candidate Results 
*  Send Final Screening Result 
*  Process Sleep Timer 


📂 Workflow Summary

Input → Processing → AI Screening → Decision → Notification

1.  User uploads resume 
2.  Resume processed and text extracted 
3.  AI evaluates candidate 
4.  System applies decision rules 
5.  Emails sent and Google Sheets updated 
6.  Telegram final summary delivered 


🧩 Technologies Used

*  n8n (Orchestration) 
*  Google Gemini (AI Model) 
*  Telegram Bot API 
*  Google Sheets API 
*  Gmail API 
*  PDF/DOCX extractors 


🧪 Testing Instructions

1.  Send a resume to the Telegram bot 
2.  Monitor workflow execution in n8n 
3.  Confirm AI evaluation results 
4.  Verify acceptance/rejection decision 
5.  Check Google Sheets entry 
6.  Check email + Telegram summary 



🛠 Future Enhancements

*  Job Description (JD) based scoring 
*  Interview question generator 
*  Personality & soft-skill scoring 
*  ATS integration (Zoho, Workday, BambooHR) 
*  Analytics dashboard (PowerBI / Looker Studio) 
*  Multi-language resume support 


📜 License

Internal use for HR/IT recruitment automation.
