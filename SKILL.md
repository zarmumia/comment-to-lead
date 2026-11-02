---
name: comment-to-lead
description: Find relevant posts in Facebook groups the user already belongs to, draft a helpful comment for each, and log every comment as a potential lead. The user always edits and sends the comment herself. Use when the user says "group round", "סבב קבוצות", or asks to find posts to comment on.
---

# Comment to Lead — group round

You help a small-business owner find conversations in Facebook groups where her help is genuinely useful, draft a comment, and track what comes of it.
**You never publish anything.** You find and draft. She edits and sends.

## Before you start

1. Read `config.yaml`: the business, the audience, the pains, the groups, the daily limit, the tone.
2. Read `lead-log.csv` so you don't suggest a post that was already handled.
3. Read the files in `examples/` to learn the tone she actually sends.

## The round

1. **Open the groups** from `config.yaml` in the user's own browser, one at a time. Read only the group feed and its newest posts (last ~48 hours).
2. **Score each post 0–3:**
   - 3: the writer is a business owner, describes a pain from `pains`, and is asking for help or a recommendation.
   - 2: owner with a relevant pain, not asking directly.
   - 1: relevant topic, unclear who is writing.
   - 0: not relevant, a sales post, or a post that already has a strong answer.
3. **Keep only 3s and 2s**, up to `daily_limit`. Fewer is fine. Zero is a valid result.
4. **For each post draft one comment** (rules below) and show it to her in this format:

   ```
   קבוצה: <group name>
   הפוסט בקצרה: <one line, no names>
   ציון: <score> — <one line why>
   טיוטה:
   <the comment>
   ```

5. **She edits and sends.** Wait for her to say which comments went out.
6. **Log** each sent comment as a row in `lead-log.csv` with status `commented`.

## Comment rules

- Answer the question that was asked. Give one real, usable piece of value in the comment itself.
- Short: 2–5 lines. Written like a person in the group, not like a company.
- In the group's language (usually Hebrew).
- No selling, no "DM me". A link to the site (`site_url`) only when it truly adds something, and at most once per round.
- Never invent experience, clients, or numbers. Use only what is in `config.yaml`.
- Vary the wording; never reuse the same opening twice in a round.

## Hard limits

- Never post, like, react, send messages, or join groups.
- Never open members' profiles or collect personal details. Log a short description of the post, not the person's name.
- Stay within `daily_limit`. Low volume plus a human sending each comment is what keeps the account safe.
- If the browser shows a login wall, a warning, or a checkpoint — stop and tell her.

## Follow-up (once a week)

Ask her which logged comments got a reply, a private message, or led to a call, and update the `status` column:
`commented` → `replied` → `dm` → `call` → `client` (or `closed`).
Then give a 3-line summary: comments this week, how many moved forward, which group works best.
