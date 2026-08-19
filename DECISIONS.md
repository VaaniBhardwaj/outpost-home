# DECISIONS.md — Outpost (Part 2: Premium Home Page)

## The pitch
**Outpost** — uptime and error monitoring for teams without a dedicated
on-call rotation. Invented product, honest copy: no fabricated user counts,
testimonials, or logos anywhere on the page. The one "live" number (the
"demo has been open for" counter) is explicitly labeled as a demo timer,
not usage data.

## 1. Why this approach over the obvious alternative
The obvious default for a "premium" marketing page in 2026 is a React +
Tailwind + Framer Motion stack scaffolded with a bundler. I rejected that
for a single self-contained `index.html` (vanilla CSS + a few dozen lines
of JS) because:
- Zero build step means zero deploy friction — drag the file onto Netlify
  or push it to a repo and enable Pages, and it's live. No dependency
  rot, no `npm install` failing in six months.
- The page has no state to manage beyond a theme toggle and a scroll
  observer. A component framework would be solving a problem this page
  doesn't have.
- It forces restraint: no component library to reach for, so every visual
  decision (the pulse-line motif, the mock dashboard, the type pairing)
  had to be made deliberately rather than picked from a kit.

**Trade-off of this choice:** it doesn't scale past one page. If Outpost
needed a pricing page, docs, and a blog next week, I'd reach for
Astro or Next.js instead — this is the right call for a single landing
page, not for a growing site.

## 2. One trade-off made under the time limit
I built one working dark/light theme pair via CSS custom properties
rather than testing the design against a real design system or a second
person's eyes. With a real week I'd: run the page past 2–3 people cold
and watch where their eyes go in the first three seconds; pull real
screenshots from an actual working alert-delivery flow instead of a
static mock dashboard; and add a genuine interactive demo (type a URL,
watch a fake check run) instead of the static service-list mock.

## 3. Where AI was used, and what I verified
I used Claude to generate the first draft of this page — including the copy, layout, HTML, CSS, and JavaScript — based on the assessment brief. Before submitting, I reviewed the complete `index.html`, opened the page in the browser, checked the responsive layout, tested the dark/light theme toggle and page interactions, and verified that the page does not use fabricated testimonials, user counts, or logos. I also reviewed the implementation of the demo timer, scroll-reveal behavior, pulse-line animation, and Konami-code easter egg so I could understand what each part does and explain the decisions during the follow-up discussion.


