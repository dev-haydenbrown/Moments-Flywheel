# Moments™ Flywheel — AI Winning Talk Tracks

An interactive front-end prototype for a closed-loop integration between two
existing Revenue.io products: **Revenue Roleplay AI** (AI-coached sales practice)
and **Moments™** (real-time live-call guidance).

The concept: roleplay sessions scoring above 90% are mined for the exact phrasing
that produced positive sentiment shifts. Those "winning talk tracks" are pushed to
the Moments™ admin console as AI-suggested battlecards, where a manager approves,
edits, or dismisses them before anything reaches a live call.

## The loop

| Step | Stage | What happens |
|---|---|---|
| 1 | Practice | Reps complete scored AI-coached roleplay sessions |
| 2 | Analyze | Sessions >90% surface phrases that moved prospect sentiment |
| 3 | Recommend | Talk tracks queue in the Moments™ console for review |
| 4 | Approve | A human approves, edits, or dismisses — nothing auto-publishes |
| 5 | Execute | Approved cards surface to reps during live calls |

Step 4 is deliberate. There is no path in this design where AI-generated copy
reaches a live call without a manager approving it first.

## Running it

Open `index.html` in any browser. No build step, no server, no install.

## Demo walkthrough

1. **Home** — flywheel overview, pipeline stats, top-scoring sessions
2. **Roleplay** — session detail: scoring breakdown, transcript, and the new
   Winning Talk Tracks section
3. Click **⚡ Recommend to Moments™** — the track transfers to the review queue
   (toast confirmation, sidebar badge increments)
4. **Moments™ Console** — the new recommendation arrives flagged `NEW`
5. Click **✓ Approve & Publish** — it moves to Published Live Cards, with a
   preview of how it surfaces mid-call

## Built with

Vanilla **HTML / CSS / JavaScript** in a single self-contained file — no
frameworks, no libraries, no build tooling. The only external resource is the
Inter typeface from Google Fonts.

- CSS custom properties for design tokens, matched to the live
  revenueroleplay.ai stylesheet so the visual layer maps onto the existing system
- Flexbox / Grid layout, `@keyframes` animation, inline SVG icons
- Plain DOM APIs for state and rendering

## Scope

This is a **prototype**, not production code. The UI and interaction flow are
fully functional; the data is hardcoded. There is no backend, no database, and no
model actually performing the extraction. Its purpose is to specify intended
behavior and layout for the product and engineering teams.

Revenue Roleplay AI is a React application, so production components would be
rebuilt — the transferable assets here are the interaction design, the flow, and
the design tokens.
