# Project Health Check — Claude Skill

A ready-to-use prompt that runs the 5-point Project Health Check on every project on your Strategy page. Paste it into Claude, ChatGPT, or any LLM. It outputs a traffic-light scorecard in under 30 seconds.

Use it **twice a week** (we run it Tuesday + Thursday 08:30).

---

## How to use

1. Open your Strategy page (Notion, Obsidian, Google Docs — anywhere).
2. Copy the **Projects** section.
3. Paste it into the prompt below where it says `<PROJECTS GO HERE>`.
4. Send.

The model returns a scorecard you can scan in 15 seconds. Fix the red items first, the yellow items next, ignore the green ones.

---

## The prompt

```
You are a strategic execution coach. I will give you a list of current-month Projects from my business. For each one, run the 5-Point Project Health Check and return a traffic-light scorecard.

# The 5-Point Project Health Check

For every project, score each point PASS or FAIL:

1. **Named owner** — Is there ONE specific person (or AI agent) responsible? "The team" is a FAIL. "Me" is a FAIL unless I am the actual owner.
2. **Live next action** — Is there a concrete next action visible on a task system RIGHT NOW? "Follow up with Sarah" is PASS. "Think about the launch" is FAIL.
3. **Method defined** — Do I know HOW this gets done, not just WHAT the outcome is? "Close 3 deals" is FAIL without a method. "Close 3 deals via the Dream 100 outbound sequence" is PASS.
4. **Movement in last 7 days** — Has there been observable progress in the past week? "Meeting scheduled for next week" is PASS. "Still thinking about it" is FAIL.
5. **Continuation mechanism** — Is there a scheduled cadence (recurring calendar block, automation, standing agent) that keeps this moving without me remembering? Willpower is FAIL.

# Scoring

- 5/5 PASS → 🟢 GREEN
- 3–4/5 PASS → 🟡 YELLOW (fix the failed points)
- 0–2/5 PASS → 🔴 RED (project is stalled — either revive it or move it to Someday)

# Output format

**📋 Project Health Check — [today's date]**

🟢 [Project name] — all 5 green.
🟡 [Project name] — missing: [specific failed points, one line each]. **Fix this first:** [one clear next step].
🔴 [Project name] — missing: [specific failed points]. **Decision needed:** revive (how?) or kill.

**Top priority today:** [the single project most at risk of slipping the month].

Keep the whole output scannable in 15 seconds. No hedging. No "it depends." One verdict per project.

# My projects this month

<PROJECTS GO HERE>
```

---

## Example input → output

**Input (pasted in place of `<PROJECTS GO HERE>`):**

```
- Launch certification cohort — 15 seats by June 30
- 3 new 200K Club clients — $12K each
- 1 licensing deal — $20K
- Ship the new Jet Pack Workshop on April 20
- Grow Sprint Club from 254 → 269
```

**Output:**

```
📋 Project Health Check — 2026-04-15

🟢 Ship the new Jet Pack Workshop on April 20 — all 5 green (Michelle owner, Luma page live, 23 registrants, daily Discord updates, April 20 calendar hard stop).

🟡 Launch certification cohort — 15 seats by June 30 — missing: next action unclear, no continuation mechanism. Fix this first: schedule a weekly Tue 10:00 certification-leads review on the calendar.

🟡 Grow Sprint Club from 254 → 269 — missing: no named owner, method vague. Fix this first: assign owner (Michelle?) and define the single acquisition channel driving this month's growth.

🔴 3 new 200K Club clients — $12K each — missing: owner, next action, method, movement, continuation. Decision needed: revive (what's the plan — outbound? referrals? warm pipeline?) or move to Someday.

🔴 1 licensing deal — $20K — missing: owner, next action, method, movement. Decision needed: who are we licensing to? Without a named prospect, this is a wish, not a project.

Top priority today: 200K Club clients — biggest revenue line with zero infrastructure.
```

---

## Why "Tue + Thu"?

- **Monday** is too early — you're still waking up to the week.
- **Sunday** means you're working on weekends. Don't.
- **Tue + Thu** gives you two check-ins per week, 72 hours apart, with Friday reserved for the full weekly review.

---

## Agent version

If you run Claude Code, Cursor, or any scheduled-agent system, wire this prompt to fire automatically on Tue + Thu at 08:30, read your Projects list, and post the output to your daily briefing channel (Slack, Discord, email). Then you get the nudge whether you remember or not.

That's the real unlock — the check runs even when you forget.

---

*Skill by [Strategy Sprints](https://strategysprints.com) · MIT License*
