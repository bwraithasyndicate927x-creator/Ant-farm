# Ant Farm Core API (v0.1)

This document describes how the browser extension
communicates with the Ant Farm Core.

---

## POST /analyze-product

Description:
Receives product data from the browser extension
and returns an Ant‑Scout analysis.

### Request Body

```json
{
  "product_name": "string",
  "price": "string",
  "availability": "string",
  "seller": "string",
  "url": "string"
}
