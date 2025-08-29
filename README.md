# prototype
AI Receptionist / AI Employee platform for service businesses
AI Receptionist / AI Employee platform for service businesses. The system must handle inbound calls and SMS for natural conversations, and integrate with whatever booking/payment system each client already uses (e.g., Square, Calendly, Stripe, Fresha). Core features include booking creation, SMS confirmations with payment links, + auto SMS, an admin dashboard (business configs, services, logs, metrics), and multi-tenant support. I’ve prepared a full specification document that clearly outlines all requirements, tech stack, deliverables, and timeline 
 

 
⚡ Project Overview
·       Build an AI Receptionist / AI Employee Platform for service businesses.
·       MUST handle inbound calls + SMS.
·       MUST support intents: Booking, Price, Hours, Speak-to-Human, Fallback.
·       Integrate with ANY booking/payment system (Square, Calendly, Fresha, Stripe, etc.).
·       Fallback: lightweight internal scheduler + payment link generator if no system.
·       Send SMS confirmations with service details + deposit/payment link.
·       Multi-tenant: support multiple businesses with separate configs.
·       Compliance: call recording disclosure, SMS STOP/HELP handling.
✅ Acceptance Criteria
·       Answer calls in <1.5s.
·       Correctly handle all 5 intents.
·       Create bookings in client’s existing system (2 integrations at launch).
·       Send SMS confirmation with payment link.
·       Closed hours → voicemail + SMS reply.
·       Admin app with business setup, service CRUD, logs, metrics.
·       Multi-tenant separation for businesses.
·       Structured logs, webhook retries, health endpoint.
·       Deployment to staging + production with documentation.
📞 Core Features & Flows
·       Voice Flow: Greeting → Intent detection → Booking/FAQ/Human/Fallback.
·       Booking: confirm service/time → book in provider → payment link → SMS.
·       Pricing/Hours: retrieve from KB → respond → offer booking.
·       Speak to Human: forward call → voicemail if unavailable.
·       Fallback: clarify once → DTMF menu.
·       Closed hours: voicemail + SMS auto-reply.
·       SMS Flow: inbound parse → respond; outbound confirmations, reminders.
·       Admin: Business onboarding, CRUD services, logs, metrics dashboard.


💬 Conversation Contract
·       Intents: book, price, hours, speak_to_human, fallback
·       Entities: service_name, date, time
·       Guardrails: No card data, concise answers, escalate when unclear
·       Tone: polite, concise, professional
🔒 Compliance & Privacy
·       Call recording disclosure (configurable).
·       Respect STOP/HELP SMS compliance.
·       No card details stored; only payment links + statuses.
·       Transcript retention configurable (default 90 days).
📊 Observability
·       Structured logs with correlation IDs.
·       Alerts: webhook failures, booking errors, SMS failures.
·       Health endpoint monitoring.
📦 Deliverables
·       Running app in staging + production.
·       Source repo: Dockerfile, migrations, CI/CD, OpenAPI spec, Postman collection.
·       Architecture + sequence diagrams.
·       Setup documentation + runbooks.
·       Demo video or live walkthrough.
📅 Timeline (6 weeks)
·       Week 1–2: Twilio + OpenAI call flow + SMS
·       Week 3: Booking/payment integrations (2 providers)
·       Week 4: Admin dashboard
·       Week 5: Multi-tenant, voicemail, escalation
·       Week 6: Testing, docs, handover
📜 Ownership 
·       All IP and code owned by client.
·       Source code + infra credentials must be delivered.
 
