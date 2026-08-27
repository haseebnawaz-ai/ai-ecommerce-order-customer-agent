# 🛒 AI E-Commerce Order & Customer Management Agent

An enterprise-grade autonomous workflow engine built with **n8n**, **Claude AI (Anthropic)**, **Shopify/WooCommerce**, **Slack**, **Telegram**, and **WhatsApp Cloud API**. This system manages the complete lifecycle of e-commerce orders: performing real-time AI fraud analysis, verifying inventory stock, generating PDF invoices & shipping labels, routing customer support webhooks to Claude AI, and triggering error alerts to Telegram.

---

## 🎯 Key Capabilities

- **AI Fraud Analysis (Claude):** Extracts order & historical customer data from Google Sheets and streams it to Anthropic Claude to flag high-risk orders automatically.
- **Manual Review Workflows:** Routes high-fraud-risk transactions directly to Slack for human agent verification.
- **Dynamic Inventory & Supplier Logistics:** Checks inventory levels real-time; if out of stock, automatically emails suppliers to restock.
- **Automated Invoicing & Shipping:** Generates dynamic PDF invoices, waits for payment confirmation, generates shipping labels, and dispatches tracking info via WhatsApp & Email.
- **Automated Post-Delivery Engagement:** Waits 5 days post-delivery buffer before triggering automated customer review request emails.
- **24/7 AI Customer Support:** Catches incoming customer support webhooks, generates context-aware answers using Claude AI, and sends replies via WhatsApp.
- **Real-time Failure Monitoring:** Connected to an error trigger node that immediately alerts administrators via Telegram if any execution fails.

---

## 📐 Workflow Architecture

![System Architecture](./AI%20E-Commerce%20Order%20%26%20Customer%20Management%20Agent.jpg)

---

## 🛠️ Tech Stack & Integrations

- **Orchestration:** n8n Workflow Automation
- **AI Engine:** Anthropic Claude API (Fraud Detection & Customer Support Copy)
- **E-Commerce & Storage:** Shopify / WooCommerce Webhooks, Google Sheets
- **Notifications & Communication:** Slack, Telegram API, Meta WhatsApp Cloud API, Email (SMTP)
- **Document Processing:** PDF Invoice Generation & Shipping API integrations

---

## 🚀 How to Import & Run

1. Clone this repository or download the JSON workflow file.
2. Open your n8n workspace dashboard.
3. Click **Workflows** ➔ **Import from File** and select the `.json` file.
4. Set up credentials in n8n for:
   - Anthropic Claude API Key
   - Google Workspace / Sheets OAuth2
   - Slack App Bot Token
   - Telegram Bot Token
   - Meta WhatsApp Cloud API Token
5. Activate the webhook endpoints and set the workflow status to **Active**.
