🟢 Service 1 — WhatsApp Gateway (Separate Service)

Responsibilities:

Receive WhatsApp webhooks

Verify Meta signature

Normalize message format

Handle retries / idempotency

Send outgoing messages

Rate limiting

It should:

Call your Agent API

Receive response

Send to WhatsApp

It should NOT:

Run LangGraph

Call Ollama directly

Know business logic

🔵 Service 2 — Agent Orchestrator (This Repo)

Responsibilities:

Receive normalized message

Load session state

Run LangGraph

Call tools (Directus)

Call Ollama

Return structured response

This is the “brain”.

🟣 Service 3 — Directus Backend (Existing)

Source of truth:

Users

Assessments

Appointments

Chat module

Audit logs

Roles
