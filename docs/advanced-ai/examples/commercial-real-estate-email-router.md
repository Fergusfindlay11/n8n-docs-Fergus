---
contentType: howto
title: Route commercial real estate email leads automatically
description: Automate Outlook triage, Airtable enrichment, and AI-assisted replies for commercial property enquiries.
---

# Route commercial real estate email leads automatically

Use n8n to triage inbound property enquiries, route them into the right Outlook folders, and follow up automatically. This workflow polls Microsoft 365 Outlook, deduplicates messages, uses a mix of rules and LLM classification, enriches leads with Airtable data, then drafts or sends responses and follow-up nudges.

[[ workflowDemo("file:///advanced-ai/examples/commercial_real_estate_email_router.json") ]]

## Key features

This workflow uses:

* [Cron node](/integrations/builtin/core-nodes/n8n-nodes-base.cron/index.md): schedules inbox polling and nightly clean-up.
* [Microsoft Outlook node](/integrations/builtin/app-nodes/n8n-nodes-base.microsoftoutlook/index.md): fetches, files, moves, and replies to messages.
* [Function node](/integrations/builtin/core-nodes/n8n-nodes-base.function/index.md): deduplicates messages, applies routing logic, and orchestrates follow-up rules.
* [OpenAI Chat Model](/integrations/builtin/cluster-nodes/sub-nodes/n8n-nodes-langchain.lmchatopenai.md): classifies ambiguous emails and drafts responses.
* [Airtable node](/integrations/builtin/app-nodes/n8n-nodes-base.airtable/index.md): matches enquiries to known buildings, fetches template data, and logs interactions.

## Using the example

--8<-- "_snippets/examples-color-key.md"
