# tpl-chatbot

**8AI Chatbot client template**

Platforms: Typebot (flows) · Dify (RAG) · Twilio (WhatsApp)

## New Client Setup
1. Use this template: `gh repo create client-[name]-chatbot --template cameronknowles-dotcom/tpl-chatbot --private`
2. Fill in `CLAUDE.md` with client details
3. Build flow in Typebot → export JSON to `chatbot/flow.json`
4. Set up n8n webhook → export to `workflows/chatbot-handler.json`

## Structure
```
chatbot/
  flow.json          ← Typebot flow export
workflows/
  chatbot-handler.json  ← n8n webhook handler
```
