# Image Invoice Automation

An **AI-powered invoice extraction workflow** that receives invoice images through Telegram, analyzes them with a vision-capable language model, validates the structured output, and stores the extracted fields in Airtable.

## What it does

- Receives invoice images through a Telegram trigger.
- Downloads the highest-quality Telegram image available in the workflow input.
- Uses an AI agent with an image-capable model to extract invoice fields.
- Enforces a compact JSON schema for invoice ID, customer, email, amount, issue date, due date, and status.
- Parses the model output and maps the result into Airtable fields.
- Creates a structured invoice record for later reminders and reporting.

## Workflow architecture

`Telegram Trigger → Get file → AI invoice extraction → Parse JSON → Save invoice to Airtable`

## Integrations

- n8n
- Telegram
- Groq-compatible AI chat model
- Airtable
- JavaScript JSON parsing

## Setup

1. Import `IMAGEINVOICE.json` into n8n.
2. Configure the Telegram bot credential and Airtable connection.
3. Configure the AI model credential and verify image passthrough support.
4. Align the Airtable field names with the mapping in the workflow.
5. Test with representative invoice images and confirm extracted values before production use.

The exported workflow contains placeholders and should be reviewed for field-name consistency before activation.
