# comment-to-lead

**Find the conversations your clients are already having — and answer them like a person.**

A Claude skill for small-business owners who get clients from Facebook groups.
Claude goes through the groups you already belong to, finds posts where your help is genuinely useful, drafts a short comment, and keeps a lead log.
**You edit and send every comment yourself.** Nothing is ever posted automatically.


https://github.com/user-attachments/assets/22692644-6b14-4a2f-a7c6-ee9335d8e193


## Why a human — always

1. **Speed converts.** When someone replies, the lead is warm for minutes, not days. You answer right away, in the moment.
2. **Replies come from everywhere.** A reply in the thread, a private message, WhatsApp, a phone call. Only you see the whole conversation, so only you can move it forward.
3. **Your voice, end to end.** The person who wrote the comment is the person they will talk to. No gap between the comment and you.

Claude does the searching, scoring and drafting. You do what makes it convert.
(And yes — low volume with a person behind every send also keeps your account safe.)

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

**למה תמיד אדם:**
1. **מהירות ממירה.** כשמישהו עונה, הליד חם לדקות, לא לימים. את עונה מיד.
2. **התגובות מגיעות מכל מקום:** בשרשור, בהודעה פרטית, בוואטסאפ, בטלפון. רק את רואה את כל השיחה.
3. **הקול שלך מההתחלה עד הסוף.** מי שכתבה את התגובה היא מי שהם ידברו איתה. אין פער בין האדם למכונה.

---

Built by [Zarmumia](https://zarmumia.co.il). The repo is free.
Zarmumia also runs it as a done-for-you service for small businesses in Israel: we set the audience and the groups, draft every round, and the owner approves.

License: MIT
