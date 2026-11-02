# comment-to-lead

**Find the conversations your clients are already having — and answer them like a person.**

A Claude skill for small-business owners who get clients from Facebook groups.
Claude goes through the groups you already belong to, finds posts where your help is genuinely useful, drafts a short comment, and keeps a lead log.
**You edit and send every comment yourself.** Nothing is ever posted automatically.

## Why a human sends every comment

- Comments that sound automated hurt your reputation in the group.
- Fully automated activity gets accounts restricted.
- Your edit is what makes the comment yours. The `examples/` folder shows the difference.

Low volume (2 comments a round), a real answer in every comment, a person behind every send.

## How it works

1. **Find** — Claude reads the newest posts in your groups, in your own browser session.
2. **Score** — each post gets 0–3 by your audience and pains. Only relevant posts move on.
3. **Draft** — a 2–5 line comment that answers the question. No selling.
4. **You send** — edit, post, done.
5. **Log** — every comment goes to `lead-log.csv`. Once a week, Claude asks what happened and tracks: commented → replied → DM → call → client.

After a few weeks you know which groups bring conversations, not just likes.

## Setup

1. Copy `config.example.yaml` to `config.yaml` and fill in your business, audience, pains and groups.
2. Add 2–3 comments you actually sent to `examples/` so Claude learns your voice.
3. Use the skill with Claude in Chrome and say: **"group round"**.

## Files

| File | What it is |
|---|---|
| `SKILL.md` | The method: scoring, comment rules, hard limits |
| `config.example.yaml` | Your business, audience, groups, daily limit |
| `lead-log.csv` | The lead log |
| `examples/` | Drafted vs. sent comments |

## Roadmap

Facebook groups first. The core (find → score → draft → human sends → log) is channel-agnostic; more channels will be added only if the numbers justify it.

---

## בעברית

**למצוא את השיחות שהלקוחות שלך כבר מנהלים, ולענות עליהן כמו בן אדם.**

סקיל ל־Claude לבעלי עסקים קטנים שמביאים לקוחות מקבוצות פייסבוק.
Claude עובר על הקבוצות שאת כבר חברה בהן ומוצא פוסטים שבהם העזרה שלך באמת מועילה. הוא מנסח תגובה קצרה ומנהל יומן לידים.
**כל תגובה את עורכת ושולחת בעצמך.** שום דבר לא מתפרסם אוטומטית.

**הזרימה:** מוצאים ← מדרגים ← מנסחים ← את שולחת ← נרשם ביומן. פעם בשבוע בודקים מה התקדם.

---

Built by [Zarmumia](https://zarmumia.co.il). The repo is free.
Zarmumia also runs it as a done-for-you service for small businesses in Israel: we set the audience and the groups, draft every round, and the owner approves.

License: MIT
