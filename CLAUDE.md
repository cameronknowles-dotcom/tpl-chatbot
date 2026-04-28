# [CLIENT NAME] — Chatbot Project

## Client
- Business: [CLIENT BUSINESS NAME]
- Industry: [INDUSTRY]
- Location: [CITY, COUNTRY]
- Website to embed on: [domain.com]
- Contact: [NAME — EMAIL]

## Chatbot Type
- [ ] Lead capture bot (Typebot — simple flow, collects name/email/phone)
- [ ] FAQ bot (Typebot + Claude API — answers questions about their business)
- [ ] RAG doc bot (Dify — trained on client documents/PDFs)
- [ ] WhatsApp bot (Twilio + n8n + Claude API)

## What the Bot Does
[Describe clearly — e.g. "Greet visitors, ask what they need, collect contact details, send to owner via WhatsApp"]

## Typebot Config (if flow bot)
- Typebot instance: Railway (https://typebot.8ai.dev)
- Flow name: [CLIENT NAME] - Lead Capture
- Embed type: [bubble / popup / inline]
- Embed position: [bottom-right / centre]
- Webhook on completion: n8n (POST /webhook/[client-chatbot])

## Dify Config (if RAG bot)
- Dify instance: Mac Mini (localhost:3000)
- Knowledge base: [list documents uploaded]
- Model: Claude Sonnet 4.6
- Embed as: iframe / web widget

## n8n Workflow
- Webhook receives: name, email, phone, message from Typebot
- Actions: [notify owner via WhatsApp / save to Supabase / send email]
- Workflow file: workflows/chatbot-handler.json

## WhatsApp (if WhatsApp bot)
- Twilio number: [+27...]
- Trigger word: [START / Hi / none]
- Handoff to human: [yes — after X messages / no]

## Notes for Claude Code
- Typebot flow exported to chatbot/flow.json (version controlled)
- n8n workflow exported to workflows/ directory
- Test embed on staging URL before going live
