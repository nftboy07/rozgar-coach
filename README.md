# Rozgar Coach — Agentic AI Career Coach for India's Youth

> **Code for India · Code for a Billion — Bharat Agentic-AI Hackathon 2026**
> **Track 10: Tech Employment for Youth** · Solo entry · MIT Licence
> *Rozgar* = livelihood / employment. A coach, not just a course list.

**Live demo:** deploy this repo on GitHub Pages (Settings → Pages → `main` / root) — the app is a single static `index.html`, no build step. Also works by simply opening `index.html`, and offline after first load.
**Video demo:** see the 60–90 second script below (the event accepts a 2–3 min video *or* a live link — extend the script with the Interview + Tracker sections for a full 2–3 min cut).

---

## The problem (judging: size + severity)

India produces lakhs of first-time tech job seekers every year — engineering and degree graduates, diploma holders, and self-taught learners, most of them outside the metros. The Government's own Independence Day pledge — training **1 crore young people in AI skills within a year** — signals the scale. Yet campus placement help concentrates in top-tier institutions. For a learner in a Tier-2/3 town or a government college, the failure mode is rarely talent:

1. **No sequence** — they don't know which skill to learn *next* for a specific role, so effort scatters across random tutorials.
2. **Undersold proof** — real project work gets written as *"worked on a project using HTML"* and is filtered out before a human ever sees it.
3. **First exposure at the worst moment** — they meet standard interview questions for the first time *inside* the interview.
4. **No pipeline discipline** — applications live across WhatsApp, email and memory; follow-ups never happen; silence gets misread as personal failure.

Paid coaching fixes this for those who can pay. Rozgar Coach is the same system — planning, polishing, rehearsal, tracking — free, private, and phone-friendly.

## The solution — four agents, one goal: your offer letter

Rozgar Coach is a **single-file agentic web app** (vanilla HTML/CSS/JS, zero dependencies, zero backend). Four cooperating agents share one user goal:

| Agent | What it does |
|---|---|
| 🗺️ **Planner Agent** | Takes target role + current skills + hours/day, runs a gap analysis against the role's core-skill set, and sequences an 8-phase curriculum (3 phases × portfolio projects) into a 4/8/12-week checklist roadmap. |
| 📝 **Resume Agent** | Rule-based bullet rewriter: detects weak openers ("worked on", "responsible for", "helped"), upgrades verbs, restructures to *action + build + result*, and produces 3 versions (Strong / Quantified / Concise+Tech) with an explicit honesty rule — placeholders, never invented numbers. |
| 🎤 **Interview Agent** | Role-specific Q&A bank (8 roles × 5 questions: concepts, practical, HR) with reveal-after-thinking model points and saved self-ratings that feed the readiness score. |
| 📌 **Tracker Agent** | Full application funnel in `localStorage` — add, status-update (Wishlist → Applied → Assessment → Interview → Offer), delete, live funnel stats. |

A live **Job-Readiness Score** (roadmap completion 70% + interview confidence 15% + application pipeline 15%) turns four separate tools into one agentic loop: the agents' outputs feed each other, and the user always sees the single next thing that moves the score.

### Why "agentic" and why local-first
Each agent perceives (form/tracker state), decides (gap analysis, rewrite rules, question selection), and acts (roadmap, bullets, drills, funnel) toward the shared goal — the classic agent loop, implemented transparently in the browser with an on-screen agent log so judges and users can *see* the reasoning steps. Local-first is a deliberate impact choice: no sign-up, no API key, no server cost, no personal data leaving the device — so it works for a learner on a shared phone and a ₹0/month hosting budget, forever.

## Tracks & event fit
- **Impact area:** #10 Tech Employment for Youth — job discovery readiness, portfolio building, apprenticeship/internship preparation, hiring signal for first-time coders.
- **Deployed:** static site → GitHub Pages (any cloud satisfies the event rule).
- **Open source:** MIT (see `LICENSE` note below — add the standard MIT text when publishing).

## Run it
```bash
# Option A: just open the file
open index.html        # or double-click it

# Option B: local server
python3 -m http.server 8000   # → http://localhost:8000

# Option C: GitHub Pages — push repo, Settings → Pages → Deploy from branch (main, / root)
```

## Files
| File | Purpose |
|---|---|
| `index.html` | The entire app (UI + all four agents + knowledge base) |
| `README.md` | This file — submission description + demo script |
| `SUBMISSION.md` | Draft answers for the GitHub submission form |
| `REQUIREMENTS.md` | Researched official event requirements (source: codeforindia.org/hackathon) |

## Honest limitations & roadmap
- Rewriting and roadmaps are **rule/knowledge-based**, not an LLM call — chosen for ₹0 cost, offline use and privacy. The agent interfaces are deliberately shaped so an LLM (e.g. via AgentFoundry) can slot behind the same Planner/Resume agents later without UI changes.
- Question bank covers 8 roles × 5 questions; expanding to Hindi/regional-language UI and vernacular explanations is the top roadmap item, followed by apprenticeship/internship listing feeds and mentor review of capstone projects.
- **Proven impact (so far):** the deliverable is the deployed app itself plus its built-in readiness/funnel instrumentation for the *user's own* outcomes. No user numbers are claimed in this submission — any metrics added later will be real counts from voluntary user sharing.

---

## 🎬 Demo script (60–90 seconds; extend to 2–3 min for the event video)

**[0:00–0:12 — Problem]** *(screen: hero)*
"Every year, lakhs of young Indians finish a degree or a course and then stall — not for lack of talent, but for lack of a system. This is Rozgar Coach, a free agentic career coach built for Code for India's Tech Employment for Youth track."

**[0:12–0:35 — Planner Agent]** *(click "Load a demo profile", then "Generate my roadmap"; let the agent log play)*
"Ananya wants to be a frontend developer and has two hours a day. The Planner Agent checks her skills against the role, finds her gaps, and builds an eight-week roadmap — every phase ends with a portfolio project she can actually show a recruiter. As she ticks tasks off, her job-readiness score climbs."

**[0:35–0:55 — Resume Agent]** *(go to Resume, click "Try an example", then "Improve my bullet")*
"Her resume says 'worked on a college project.' The Resume Agent rewrites it three ways — strong verb, quantified result, concise with tech — and reminds her to use only true numbers. Same work, finally visible."

**[0:55–1:15 — Interview + Tracker]** *(Interview: reveal one answer; Tracker: add one application)*
"The Interview Agent drills the questions panels actually ask, with model points she rates herself against. And every application she sends lives in the Tracker — no more lost follow-ups. *(close on the readiness score)* Four agents, one goal: her offer letter. Rozgar Coach — free, private, and open source."

**For a 2–3 min event cut:** add 30s on the problem's scale/severity, 30s walking one full roadmap phase, and 20s on the local-first/privacy design decision.

---

*Built solo by Jacku P (GitHub: nftboy07) for Code for a Billion. Deploy by 15 Nov 2026; winners announced 5 Dec 2026.*
