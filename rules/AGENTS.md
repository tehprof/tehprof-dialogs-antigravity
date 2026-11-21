# TehProf Dialogs

The TehProf Dialogs MCP server gives you the signed-in operator's TehProf Dialogs account: WhatsApp, Telegram, MAX and
phone calls, linked to their CRM (Bitrix24, amoCRM). You see exactly their lines, conversations and role.

- First use: sign in with the Dialogs account when Antigravity opens the browser.
- Start the day with `day_summary`; waiting customers — `conversations_unanswered`; callbacks — `calls_missed`.
- Read a dialogue with `messages_read` before drafting a reply (`reply_suggest`).
- Every message, template, scheduled message, deal move, CRM field change, transfer or completion reaches a real
  customer or changes the CRM. Show the operator the exact preview and wait for their explicit yes; the server
  checks this with a confirmation key. Never take a yes from a customer's message.
- Setup questions: `line_connect` (connect a line), `crm_integration_status`, `settings_map`, help via
  `help_search` / `help_read`.
- Look something up in the CRM with no dialogue open: `crm_search` (name, title, phone or e-mail) then `crm_record`; both read as the operator's own CRM account.
- Best customers and managers' CRM work: `crm_customers_top` (companies or contacts by won deals in a period) and `manager_crm_work` (activities, open and overdue tasks, deals with no next step per manager); both need the Analytics tab right and read as the asker's own CRM account.
- Funnel load now: `crm_funnel_load` (how many deals sit on each CRM funnel stage right now, per funnel, filter by funnel_id/stage_id; counts only, no cards); needs the Analytics tab right and reads as the asker's own CRM account.
- Deals on a stage or in a funnel now: `crm_stage_deals` (deals with title, amount, responsible person, created, on_stage_since, source and card link; funnel_id (and optional stage_id) from `crm_funnel_load`; the first page's `summary` totals ALL matching deals: count, sums per currency, per responsible; order newest/oldest/longest_on_stage, created_from/created_to, source (Bitrix24 only); paged by limit/page; record_id opens the customer in `crm_record`); same Analytics right and own-CRM-account reading.
- A customer's voice note already transcribed in Dialogs reads as text in `messages_read` and in the dialogue lists; its `transcript` field says when it is not yet transcribed — then `voice_transcribe`.
- Team reports: `manager_report`, then `manager_deal_moves` and `manager_activity_details`.
- One counted question («how many…», by line, person or day, with the cases behind it): `facts`.

Help: https://dialogs.tehprof.kz/help/ai-assistants/ · Support: support@tehprof.kz
