# Resume Reader v2

## Overview

A webhook-based resume file upload endpoint that receives a PDF file via POST, uploads it to PDF.co for processing, and returns the result. This is a simplified version of the resume reading pipeline that handles the file upload step via webhook and PDF.co API.

## How It Works

```
Webhook (POST with PDF file) -> PDF.co (upload file) -> Respond with upload result
```

### Workflow Diagram

```mermaid
flowchart TD
    A["Webhook\nPOST with PDF"] --> B["PDF.co\nUpload File"]
    B --> C["Respond\nwith Result"]

    style A fill:#1B3A4B,color:#fff
    style B fill:#2C5F7C,color:#fff
    style C fill:#274C36,color:#fff
```

## Integrations

- **PDF.co** - PDF file upload and processing

## Setup

1. Import `Resume_Reader_v2.json` into your n8n instance.
2. Update the PDF.co API key.
3. Activate the workflow and send POST requests with PDF files.
