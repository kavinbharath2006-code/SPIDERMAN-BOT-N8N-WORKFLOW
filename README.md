# SPIDERMAN-BOT-N8N-WORKFLOW
Angie: The AI Personal Assistant (n8n Workflow)
Angie is a sophisticated personal assistant workflow built in n8n, designed to live inside your Telegram. She doesn't just chat—she manages your life by connecting your voice and text messages to your email, calendar, and task databases.

🚀 Overview
This workflow transforms a Telegram bot into a secure, context-aware executive assistant. By leveraging LangChain and OpenAI, Angie can process voice notes, summarize your unread emails, check your schedule, and update your tasks in Baserow.

🧠 Key Features
Multimodal Interaction: Send text or voice notes. The workflow automatically detects audio, transcribes it via OpenAI Whisper, and processes the intent.

Decentralized Task Management: Integrated with Baserow for task tracking and contact management.

Smart Productivity: * Gmail: Fetches and summarizes unread emails (filtering out promotions).

Google Calendar: Retrieves events and answers questions about your schedule.

Security Built-in: Features an AllowList filter to ensure the bot only responds to authorized Telegram User IDs.

Memory-Aware: Uses a Window Buffer Memory so Angie remembers the context of your previous messages in the conversation.

🛠️ The Tech Stack
Orchestration: n8n

AI Engine: OpenAI (GPT-4o & Whisper)

Framework: LangChain (Agent & Memory)

Interface: Telegram Bot API

Database/CRM: Baserow

Productivity: Google Calendar & Gmail

🏗️ Workflow Architecture
The workflow follows a logical 4-step process:

Security Gate: Checks the incoming Telegram ID against a predefined AllowList.

Input Processing: Determines if the input is text or a voice file (which is then transcribed).

The Agent (Angie): A LangChain Agent uses the provided tools to decide whether she needs to check your calendar, read your emails, or query your task list.

Response: Results are formatted in clean Markdown and sent back to your Telegram chat.

⚙️ Setup Instructions
Import the JSON: Copy the provided workflow JSON into your n8n instance.

Credentials: Connect your credentials for:

Telegram Bot API

OpenAI

Google (Calendar & Gmail)

Baserow

Configuration: * Update the AllowList node with your specific Telegram User ID.

Ensure the databaseId and tableId in the Baserow nodes match your workspace.
