# Marketplace N · Systems Analysis

Analysis artifacts from the Marketplace N project, a marketplace where small brands and independent makers sell jewelry. All data is anonymized.

| Module | Artifact | What's inside |
| --- | --- | --- |
| Order payment | [Technical use case: YooKassa integration](payment-use-case/README.md) | Main and alternative flows, field mapping, order statuses, errors and timeouts, idempotency, webhooks, request and response examples, UML Sequence |
| Seller applications | [Module API contract](seller-verification/README.md) | OpenAPI 3.1: 8 operations (paginated list, create, get, update via PATCH, submit, decision, archive and restore), business errors with examples. AsyncAPI 2.6: Kafka event. ReDoc documentation, Prism mock server |
   | AI pilot (n8n) | [AI triage of student queries](ai-pilot-n8n/README.md) | Pilot in n8n: form → Claude → Google Sheets → Gmail draft with human review. Tested on 10 queries: 10/10 correctly categorized. Case written in Czech. |

## How to view

- The use case reads directly on GitHub: tables and the Mermaid diagram render automatically.
- The seller applications module runs locally, see its [README](seller-verification/README.md#how-to-run).

## Structure

```
.
├── README.md
├── payment-use-case/
│   └── README.md            # technical use case for payment
└── seller-verification/      # seller applications module API contract
    ├── openapi/
    ├── asyncapi/
    ├── schemas/
    ├── examples/
    └── README.md
```

