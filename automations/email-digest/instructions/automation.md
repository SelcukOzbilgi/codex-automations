# Email Digest — Automation Setup

This automation runs the `email-digest` skill on a daily schedule. Before setting this up, make sure you have installed the skill first — see `skill.md`.

---

## Prerequisites

- `email-digest` skill installed in Codex ✓
- Gmail connected via Composio ✓
- Composio tools enabled: `GMAIL_FETCH_EMAILS`, `GMAIL_ADD_LABEL_TO_EMAIL`, `GMAIL_CREATE_EMAIL_LABEL`, `GMAIL_SEND_EMAIL` ✓

---

## Setup

**1. Open Codex and go to Automations**

**2. Create a new automation**

**3. Paste the automation prompt below into the prompt editor**

**4. Fill in your three variables**

**5. Set the schedule** — recommended: daily at 08:00

**6. Save and run once manually to test**

---

## Automation Prompt

```
Run the email-digest skill with the following inputs:

SOURCE_KEYWORDS = ""
# What to search for in email subject or body.
# Separate multiple keywords with commas.
# Example: "newsletter, weekly update, community digest"

SOURCE_LABEL = ""
# Gmail label applied to every matching email.
# Example: "Newsletter"

DIGEST_LABEL = ""
# Gmail label applied to the digest email sent to your inbox.
# Example: "Newsletter Essential"
```

---

## Tips

- **Keywords too broad?** You'll get too many matches. Start narrow and expand if needed.
- **No digest arriving?** Check that your keywords actually appear in today's emails. Run manually once to debug.
- **Want multiple digests?** Create separate automations with different SOURCE_KEYWORDS and labels for each source.
- **Language** — the digest is written in the same language as the source emails automatically.
