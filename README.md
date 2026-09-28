# AI Customer Feedback Triage Assistant

A small no-code / AI workflow prototype for Customer Success teams.

## What it does

The workflow takes a raw customer message and turns it into structured actions:

1. **Summarise the issue** in one sentence.
2. **Classify the category** (bug, feature request, billing, how-to, churn risk, positive feedback, or other).
3. **Estimate urgency** and sentiment.
4. **Recommend the next action** and suggested owner.
5. **Draft a concise customer response**.
6. **Flag escalation risk** when the message suggests churn, blocked usage, or business impact.

## Why I built it

Customer Success teams often receive feedback through different channels. The same message may need to be understood, prioritised, routed, answered, and later analysed for trends. I wanted to explore how AI could make that first triage step faster and more consistent while keeping a human in the loop.

## Demo

Open `index.html` in a browser. Paste a customer message and click **Run workflow**.

The browser demo uses transparent rule-based logic so it can be shared publicly without an API key. The underlying AI prompt design is documented in `PROMPT.md`, including the JSON output structure I would use when connecting the workflow to an LLM.

## Example

**Input**

> We have been unable to export our reports since yesterday and our finance team is blocked. If this is not fixed today we may need to move the process elsewhere.

**Expected AI output**

- Category: Bug / Churn Risk
- Urgency: High
- Sentiment: Negative
- Suggested owner: Support + Customer Success
- Next action: Acknowledge impact, escalate immediately, confirm ownership and update cadence
- Draft response: Short acknowledgement with clear next steps and no unsupported promises

## Human-in-the-loop principles

- AI proposes; a person decides.
- Do not invent timelines or technical fixes.
- Escalate messages with churn or material business impact.
- Keep customer-facing responses concise and specific.
- Store structured fields so recurring issues can later be analysed.

## What I would build next

- Connect the prompt to an LLM API.
- Send structured results to a CRM or support tool.
- Track repeated themes and customer health signals.
- Add confidence scores and human approval before any response is sent.
- Measure time-to-first-action and routing accuracy.

## Built by

Alondra Falcon

This project was created as a learning exercise in AI-assisted Customer Success workflows and process automation.
