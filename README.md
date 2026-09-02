# Moments™ Flywheel — AI Winning Talk Tracks

### Product Walkthrough

https://github.com/user-attachments/assets/15aa6e6e-7e0a-491e-a19c-20b896d8160d

*Watch the video above for a full walkthrough of how top roleplay sessions turn into real-time call guidence.

An interactive front-end prototype for a closed-loop integration between two
existing Revenue.io products: **Revenue Roleplay AI** (AI-coached sales practice)
and **Moments™** (real-time live-call guidance).

## What it does

**Revenue Roleplay AI** is an AI-powered sales practice tool. Reps complete scored roleplay sessions where they practice objection handling, discovery, and positioning against a prospect persona. The AI grades them on methodology, objection handling, sentiment, and discovery depth.

**Moments™** is a live-call guidance platform that surfaces real-time coaching cards to reps during actual customer calls. When specific triggers fire—a competitor mention, a pricing objection, a discovery question—the system surfaces the right guidance at the exact moment the rep needs it.

**The Flywheel connects them:** Roleplay sessions scoring above 90% are mined for the exact phrasing that produced positive sentiment shifts. Those "winning talk tracks" flow into the Moments™ console as AI-suggested battlecards, where a manager approves them before anything reaches a live call.

Open `index.html` in any browser.

## How Moments™ triggers work

When a prospect says a keyword during a live call—for example, mentions a competitor like Gong—the AI recognizes it as an objection trigger. Moments™ surfaces the corresponding guidance card in real time. In this prototype, when "Gong" is mentioned, the system acknowledges it's a competitor objection and surfaces the winning talk track that was proven effective in roleplay.

## The loop

| Step | Stage | What happens |
|---|---|---|
| 1 | Practice | Reps complete scored AI-coached roleplay sessions |
| 2 | Analyze | Sessions >90% surface phrases that moved prospect sentiment |
| 3 | Recommend | Talk tracks queue in the Moments™ console for review |
| 4 | Approve | A human approves, edits, or dismisses — nothing auto-publishes |
| 5 | Execute | Approved cards surface to reps during live calls when triggers fire |

Step 4 is deliberate. There is no path in this design where AI-generated copy reaches a live call without a manager approving it first.

## Built with

Vanilla **HTML / CSS / JavaScript** in a single self-contained file. No frameworks, no libraries, no build tooling. The only external resource is the Inter typeface from Google Fonts.

- CSS custom properties for design tokens, matched to the live revenueroleplay.ai stylesheet
- Flexbox and Grid layout with `@keyframes` animation and inline SVG icons
- Plain DOM APIs for state and rendering

## Scope

This is a **prototype**, not production code. The UI and interaction flow are fully functional; the data is hardcoded. There is no backend, no database, and no model actually performing the extraction. Its purpose is to specify intended behavior and layout for the product and engineering teams.

Revenue Roleplay AI is a React application, so production components would be rebuilt. The transferable assets here are the interaction design, the flow, and the design tokens.
