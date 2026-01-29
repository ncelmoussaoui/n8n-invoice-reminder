# n8n Invoice Reminder System (v1.0)

Automated invoice reminder workflow built with n8n.
Daily check of invoices in Google Sheets → send personalized emails via Resend → update tracking fields.

## Workflow
Schedule Trigger → Google Sheets (Get Rows) → JavaScript (due logic) → IF (overdue?) → HTTP Request (Resend) → Google Sheets (Update Row)

## Features
- Daily scheduled check
- Due date + overdue calculation (JavaScript)
- Personalized reminder emails (Resend)
- Status tracking in Google Sheets (status, last_sent, attempts)
- Error handling / notifications (optional)

## Setup
1. Import `n8n-invoice-reminder.json` into n8n
2. Add credentials:
   - Google Sheets
   - Resend API key (stored in n8n credentials)
3. Configure your Google Sheet columns (example):
   - invoice_id, customer_email, due_date, amount, status, last_sent, attempts
4. Activate the workflow

## Security
No API keys or secrets are included in this repository.
