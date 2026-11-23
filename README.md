# make-n8n-dlq-error-handler

Production **n8n & Make.com** reliability patterns engineered by [NORA MEDIA](https://noramedia.pl):
- **Global Error Handler + Dead-Letter Queue (DLQ)** pattern to prevent silent webhook/API failures.
- **3 B2B Automation Blueprints**:
  1. `blueprints/01-pdf-order-to-erp.json` — Automated PDF order parsing (VAT ID, SKUs, totals) -> ERP/Subiekt API + validation gate.
  2. `blueprints/02-b2b-lead-qualification.json` — Instant B2B lead enrichment, scoring (`A-HOT` / `B-STANDARD`), CRM deal creation, and Telegram sales alert.
  3. `blueprints/03-inventory-sync-erp-store.json` — 15-min delta inventory sync (`ERP <-> Storefront`) with low-stock alerts.

## Security Note
All credentials, webhook URLs, and chat IDs are replaced with environment placeholders (`{{TELEGRAM_TOKEN}}`, `api.example-*.local`). Configure your own credentials in n8n before activating.
