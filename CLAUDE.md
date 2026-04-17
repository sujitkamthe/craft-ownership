# Craft & Ownership — Project Context

## What This Is
A self-guided, multi-page website for **senior engineers who own features end-to-end**. It is a reference for engineers who take a feature from requirements through design, delivery, and tracking, and who champion engineering craft — clean code, testing, review quality, and observability — for the team.

Hosted on GitHub Pages. Built as static HTML/CSS/JS with no build step. Sibling to `../multiplier-playbook/` (Beyond IC), which covers the *next* step after this guide — becoming an engineering leader.

## Who It's For
Senior engineers who are not managers and are not chasing management. They are strong individual contributors ready to take feature-level ownership, raise the craft bar for their team, and mentor peers and juniors — without a leadership title. Years of experience is not a criterion — we don't gate seniority on tenure as an org.

## Tone — This Is Critical
This is a **learning resource**, not a job description. The tone must be:
- **Empowering and craft-oriented** — "here's what great senior engineers do" not "here's what you're lacking"
- **Mentor-like** — a wise colleague sharing frameworks, not a tech lead issuing rules
- **Respectful** — assume the reader is a skilled engineer who wants to get better
- **Practical** — every section should have actionable frameworks, not just theory
- **Ownership-forward** — the recurring frame is "the feature is your baby; make it land well and lift the team as you go"

### What to AVOID
- **Leader / manager language** — no "delegate", "manage", "team composition", "1:1s", "hiring", "firing", "performance management"
- **Persona words** — never "Catalyst", "Multiplier", "Artisan"
- **"Tech lead" framing** — the reader is a senior IC, not a team lead; don't imply they run a team
- Accusatory language ("you're not doing X", "this is broken")
- Singling out roles or experience levels
- "Truth bomb" framing — use "Key Insight" instead
- Team-specific internal references (named tech debt items, named people)

### What to DO
- **Use "you own the feature"** framing over "you lead the team"
- **Use "the team"** when referring to peers — engineer to engineer, not up-down
- Use reflective questions ("Ask yourself: am I doing X?")
- Frame as frameworks and techniques ("The 5 Whys on Requirements", "The Almost-Done Check")
- Include external references (books, videos, articles) so readers can go deeper
- Use "common pitfall" and "better approach" in the pitfall/better grid

### The "Why" Principle — This Is Critical
Every practice, framework, and convention in this guide MUST explain WHY it exists — not just WHAT to do. Senior engineers need to understand the reasoning so they can:
1. **Teach it to peers** — "We do X because Y" is far more effective than "the guide says so"
2. **Adapt it to context** — Understanding why lets you know when to bend the rule and when to hold firm
3. **Defend it in review** — "We invested in testing because last quarter we spent 140 hours on rework" beats "best practice says so"
4. **Build genuine buy-in** — People follow rules they understand; they resist rules that feel arbitrary

When writing or editing content: for every framework, convention, or recommendation, include the reasoning. What problem does it solve? What is the cost of NOT doing this?

## Design System
- **Theme:** "Plum & Parchment" — deep plum accent, parchment background, warm dark text
- **Fonts:** Source Sans 3 (serif-ish body) + Inter (sans-serif, headings/UI) via Google Fonts
- **Colors:** `#5A1D4D` accent, `#8B2F76` link, `#FAF6EE` background, `#2A1E28` text
- **Dark mode:** supported via `data-theme` attribute on html element, toggled with localStorage key `co-theme`
- **Layout:** max content width 720px, page width 960px, line-height 1.75
- **No emojis in prose** — only in path card icons and tip boxes

## File Structure
```
craft-ownership/
  index.html                    — Home page with "Choose Your Path" grid
  foundations.html              — Ownership Mindset, End-to-End Thinking, Proactive Mode, Craft Mindset, Time & Focus
  requirements-design.html      — Clarifying Requirements, Breaking Down Features, Design Docs, ADRs, Spikes, Estimation
  clean-code.html               — Readability, Naming, SOLID, Refactoring, Modern Features, Code Smells, Boundaries
  testing-observability.html    — Test Strategy, TDD, Testable Code, Observability, Security Mindset, Feature Flags
  code-reviews.html             — Self-Review, Writing Great MRs, Reviewing as Teaching, Review Pitfalls, Standards by Example
  delivery-ownership.html       — Tracking Progress, Almost-Done Check, Risk Flagging, Dogfooding, Incident Readiness, Handover
  mentoring-peers.html          — Pairing, Prompting Questions, Growing Juniors via Review, Knowledge Sharing, Peer Feedback
  influence-communication.html  — Written Artifacts, Status Updates, Saying No with Data, Disagreeing Well, When to Escalate
  resources.html                — Books, videos, podcasts, blogs, framework quick-reference
  self-assessment.html          — Interactive checklist with localStorage persistence (keys: co-check-sa-XX)
  css/styles.css                — Shared design system (plum palette)
  js/script.js                  — Shared interactivity (theme, nav, accordion, tabs, checklist, fade-in)
  CLAUDE.md                     — This file
  .nojekyll                     — GitHub Pages asset serving
```

## Key CSS Classes
Same as Beyond IC — the component library is shared:
- `.framework` — bordered box for named frameworks and step-by-step processes
- `.key-insight` — accent-bordered box for important reflections (replaces "truth bomb")
- `.tip` — tinted box with icon for practical advice (variants: `.success-tip`, `.warning-tip`, `.danger-tip`, `.info-tip`, `.purple-tip`)
- `.pitfall` / `.better` — red/green comparison grid for "watch out for" vs "try this instead"
- `.checklist` — interactive checkbox lists with localStorage persistence (`co-check-*`)
- `.accordion` — expandable sections for detailed content (single-open)
- `.comparison` — side-by-side comparison tables
- `.card-grid` / `.card` — content cards in responsive grids
- `.page-toc` — in-page table of contents at top of each content page
- `.path-card` — home page navigation cards
- `.hero` — tall centered home-page section
- `.fade-in` — triggered by IntersectionObserver on scroll

## Content Themes (What Senior Engineers Need to Practice)

### Ownership & Foundations
1. **Ownership mindset** — "the feature is your baby" from requirements to operate
2. **End-to-end thinking** — don't stop at "my code is merged"
3. **Proactive mode** — anticipate, clarify, flag early
4. **Craft mindset** — why quality compounds and hacks decay
5. **Time & focus** — protecting maker time, context switching, deep work

### Requirements & Design
6. **Clarifying requirements** — 5 Whys on requirements, edge cases, done definition
7. **Asking good questions** — PMs, designers, stakeholders
8. **Breaking features into stories** — vertical slices, parallelisation, dependency mapping
9. **Lightweight design docs** — when to write, structure, length
10. **ADRs** — when a decision deserves a record
11. **Spikes vs build** — timeboxing unknowns
12. **Estimation** — reference stories, the 1.5x buffer, not over-committing

### Craft — Clean Code
13. **Readability first** — code is read 10x more than written
14. **Naming as a design decision** — naming smells, domain vs implementation
15. **SOLID in practice** — with multi-language examples (Java / TypeScript / Python)
16. **Refactoring as a habit** — Boy Scout rule, refactor-to-understand
17. **Modern language features** — using what the language gives you
18. **Code smells catalog** — duplication, long methods, feature envy, primitive obsession
19. **Boundaries & layering** — domain vs infra, dependency direction
20. **The 6-month test** — would you want to read this in 6 months?

### Testing, Observability, Security
21. **Test pyramid per layer** — unit / integration / contract / e2e — what each is for
22. **Writing testable code** — seams, dependency injection, pure functions
23. **TDD when it helps** — and when it doesn't
24. **Integration tests that aren't brittle** — test behavior not implementation
25. **Observability baked in** — logs, metrics, traces as part of the feature
26. **Security mindset** — input validation, OWASP basics, secret handling
27. **Feature flags for safe rollout** — dark launch, progressive delivery

### Code Reviews
28. **Self-review first** — review your own MR before requesting review
29. **Writing MRs others love** — small, scoped, described, screenshotted
30. **Reviewing as teaching** — ask questions, don't demand
31. **Review pitfalls** — nitpicks, "while you're there", ghosting the author
32. **Setting standards by example** — your reviews shape team norms
33. **Responding well to feedback** — disagree and commit, rework gracefully

### Delivery & Tracking
34. **Tracking progress without a PM hat** — simple signals: flow, burn, risks
35. **The "almost done" check** — what's left before demo
36. **Risk flagging early** — the 30% rule, no surprises
37. **Breaking-in-half when stuck** — split, pair, spike, escalate
38. **Dogfooding before ship** — you're the first user of your feature
39. **Incident readiness** — runbooks, dashboards, on-call handover
40. **Handover & runbooks** — what ops needs to know after you ship

### Mentoring Peers (Not Managing)
41. **Pairing well** — the 10-minute switch, driver/navigator
42. **Asking prompting questions** — help juniors find the answer
43. **Review feedback that grows people** — teach via review
44. **Knowledge sharing sessions** — lightning talks, lunch-and-learns
45. **Peer feedback (SBI)** — situation-behavior-impact, timely and specific
46. **Receiving feedback** — without defensiveness

### Influence & Communication
47. **Written artifacts** — design doc, RFC, ADR templates
48. **Status updates that say what matters** — risks, blockers, decisions
49. **Saying no with data** — push back with evidence, not opinion
50. **Disagreeing well** — disagree + commit, time-box debate
51. **When to escalate** — and how to escalate without burning bridges
52. **Building credibility through delivery** — the slow compound

## Tech Stack Context (for examples in content)
Examples reference Java (modern features up to Java 25), Spring Boot, TypeScript/Angular/React, Python, PostgreSQL, MongoDB, Kubernetes, AWS, Terraform, Docker, GitLab CI, Grafana, Prometheus. These are illustrative — not mandates for a specific team.

## Relationship to Beyond IC
- **Beyond IC** (`../multiplier-playbook/`) — for engineers becoming leaders (managing people, building teams)
- **Craft & Ownership** (this site) — for senior engineers owning features and raising craft, without a leadership role
- The two sites are deliberately disjoint in content: Craft & Ownership stops before delegation, hiring, team composition, performance management. Those live in Beyond IC.

## Pain Points This Guide Addresses
These are the real gaps this site is built to close. Every page should implicitly or explicitly push back on at least one of these. When writing or editing content, check: does this section address one of these?

1. **Thinking stops at story delivery.** The senior engineer closes their ticket and moves on. No sense of what the feature needs beyond "my code is merged."
2. **No sense of ownership of the feature or the product.** They treat the feature as someone else's problem once their part is done. They don't ask "is the whole thing landing?"
3. **No drive to fix problems they can see.** They notice the flaky test, the confusing log line, the slow endpoint, the awkward UX — and they walk past. "Not my story."
4. **No active scanning for pain points.** They are not in the habit of looking at the codebase, the observability dashboards, the product, or the ops runbook and asking "what hurts here, and how do I fix it?"
5. **No habit of proposing improvements.** Even when they see something worth improving, they don't raise it, don't write the proposal, don't volunteer to lead the fix.
6. **Initiatives start and stall.** When they do take something on, it drifts — because they treat it as a side project instead of a commitment. They don't drive it to completion.
7. **They do not hold a high bar for juniors.** They soften reviews, accept "it works," wave through hacks, and don't invest the extra minute to teach. They are kind at the cost of craft.
8. **They are not vocal about practices.** They know what good looks like but don't speak up when the team drifts. They assume someone else will say it.
9. **Passive in dev huddles.** They show up, half-listen, and wait for the leader to drive the conversation. The huddle should be the tech conversation — and **they should be the main voice**, not the audience.
10. **Leader's role is treated as push, not pull.** They wait for the leader to assign, nudge, remind, and chase. The right model is **pull-based**: the senior engineer pulls leader time only when genuinely needed; the leader trusts them to own the rest.
11. **Delivery excellence = on-time + no bugs.** That is a shallow definition. Real delivery excellence includes **quality of the code, performance, security, observability, accessibility, operability** — all as first-class outcomes, not afterthoughts.
12. **Blindness to waste in the dev loop.** Slow builds, slow pipelines, slow test runs, slow local startup, flaky CI — all treated as immutable facts of life instead of as problems the senior engineer should be hunting and killing.
13. **Blindness to CI/CD and release hygiene.** The release pipeline is treated as "someone else's responsibility." Broken stages, missing gates, fragile deploys, no rollback — noticed but not owned.
14. **Silent on missing observability or badly written code.** Walks past a service with no metrics, a module nobody wants to touch, a log line that never has enough context to debug with — and says nothing. Both the noticing *and* the saying are part of the job.
15. **Talking about problems without passion.** Raising an issue in a mumble at the end of a huddle, buried behind ten caveats. Senior engineers should **passionately and actively** name what's hurting the team — kindly, but clearly and often enough that it gets fixed.

### Content implications
- **Every chapter must push past "ticket closer".** The frame is always "the feature is yours, and so is everything around it."
- **Pull-based leadership** is an explicit topic in Foundations and Influence & Communication. Call it out by name.
- **Dev huddles** gets a full section in Influence & Communication: "you are the main voice in the room; the leader chips in on pull, not on push."
- **Delivery excellence** in Delivery & Ownership is defined as the full bundle: functional correctness + quality + performance + security + observability + operability.
- **Holding the bar for juniors** is a named section in Mentoring Peers and Code Reviews — kind is not the same as easy; a soft review is a disservice.
- **Finding and fixing pain points** is a named section in Foundations ("The Scan") and carries through into Delivery & Ownership and Influence & Communication (proposing improvements, driving them to done).
- **Initiative-to-completion** gets a framework: the ITC loop — notice → propose → commit → drive → land → report. Initiatives that stall are the canonical failure mode.
- **Waste in the dev loop** is a named section (in Foundations/The Scan and/or Delivery & Ownership): slow builds, slow tests, slow pipelines, slow local startup, flaky CI. "It's always been slow" is not an answer.
- **CI/CD and release hygiene** is an explicit topic (Delivery & Ownership): pipeline stages, gates, rollback, release cadence, deployment pain — the senior engineer keeps an eye on these and proposes fixes, not just for their feature but for the team's pipeline.
- **Passionate advocacy for quality** is a named habit (Influence & Communication / Dev Huddles): when observability is missing, when code is badly written, when a waste point keeps hurting — the senior engineer names it, repeatedly if needed, with warmth and clarity. Silence is the failure mode.

## Writing Principles — How Every Page Should Be Written

These are not decoration; they are what makes this a **learning resource** instead of a manifesto. Every content page must meet all of these.

### 1. Always explain the WHY
For every practice, rule, framework, or recommendation, say *why* it exists. What problem does it solve? What happens when teams skip it? Without the why, the reader memorises rules they'll abandon the first time they're inconvenient. With the why, they build judgment — they know when to hold the rule firm and when to bend it.

The WHY is not optional. If a section says "do X" without saying why, it is incomplete.

### 2. Show, don't just tell — use concrete examples and scenarios
A tip like "name variables clearly" is almost useless. The tip becomes useful when it shows a scenario:
> *"You're reviewing a PR. You hit `const result = processData(data, true);`. You stop — what does `true` mean? You scroll to the function to find out. That stop cost you 15 seconds. Multiply by every reader forever. The fix: `processData(data, skipArchive: true)`."*

Every tip, framework, and pitfall/better box should be grounded in a scenario a senior engineer would recognise. Abstract advice is forgettable; a remembered scenario is a tool.

### 3. Frameworks should be referenceable and practice-able
Frameworks (the `.framework` boxes) should be:
- **Named** — a handle the reader can recall ("The ITC Loop", "The Six-Month Test", "The 3-Point Estimate").
- **Short** — 4–8 steps or bullets. Long frameworks don't get used.
- **Action-shaped** — each step is something you *do*, not something you believe.
- **Practice-able** — a reader could try it this week on a real piece of work.

If a framework is just a list of feelings, it's not a framework — it's a mood.

### 4. Feedback flows both ways
Timely, specific feedback is not a manager's job alone. Senior engineers must:
- **Give feedback up and sideways** — to peers and to their own leaders — in the moment, not saved for later.
- **Give feedback down** — to juniors — specifically, frequently, kindly, and promptly. Feedback that arrives two months late isn't feedback, it's a verdict.
- **Ask for feedback** — actively, not only in appraisals. "What's one thing I could do better?" is a senior-engineer-sized question.
- **Receive feedback well** — without defensiveness, without argument in the moment, with a later follow-up that shows you thought about it.

This is a named section in Mentoring Peers. Feedback is a growth tool for both the giver and the receiver — without it, juniors plateau and the senior engineer never finds out what they're blind to.

### 5. Exploration mindset — exploring libraries, tools, and approaches
Senior engineers are expected to actively explore: evaluate new libraries, try new tools, prototype alternate approaches to problems the team faces. They don't wait for the team to be told "use this." They try things, write up what they learned, and propose adoption when something actually helps.

The baseline: 1–2 hours a week spent reading, evaluating, or prototyping something outside the day's work. Include this in Foundations (Time & Focus) and in Influence & Communication (proposing adoption).

### 6. Reference material — book, videos, blogs, talks
Every major topic should cite 2–3 external references the reader can go to for depth. The site is a map, not the whole territory. Great references to include:
- **Coding & Craft:** *Clean Code* (Robert C. Martin), *The Pragmatic Programmer* (Hunt & Thomas), *Code Complete* (McConnell)
- **Clean code in practice:** *A Philosophy of Software Design* (John Ousterhout), *Refactoring* (Martin Fowler), *Working Effectively with Legacy Code* (Michael Feathers)
- **Design patterns:** *Design Patterns* (GoF), *Head First Design Patterns*, *Patterns of Enterprise Application Architecture* (Fowler)
- **Architecture & principles:** *Designing Data-Intensive Applications* (Kleppmann), *Clean Architecture* (Martin), *Building Evolutionary Architectures* (Ford et al.), *Fundamentals of Software Architecture* (Richards & Ford)
- **Testing:** *Growing Object-Oriented Software, Guided by Tests* (Freeman & Pryce), *Unit Testing Principles, Practices and Patterns* (Khorikov)
- **Delivery & career:** *Accelerate* (Forsgren, Humble, Kim), *The Staff Engineer's Path* (Tanya Reilly), *The Software Engineer's Guidebook* (Gergely Orosz)
- **Talks to watch:** Dan North on software design, Kent Beck on TDD, Sandi Metz on abstraction, Kevlin Henney on readability
- **Blogs:** Martin Fowler, Dan Luu, Julia Evans, Increment, The Pragmatic Engineer

The Resources page centralises these, and content pages can link out to specific ones where relevant.
