# Copywriting Improvement Plan — mugnimaestra.dev

## Context

- **Page type:** Portfolio / personal homepage (functions like a landing page)
- **Primary action:** Get visitors to email `iam@mugnimaestra.dev`
- **Audience:** Recruiters, hiring managers, potential collaborators, engineering leaders
- **Voice:** Professional but conversational. Technical but accessible. Confident, not boastful.
- **Traffic sources:** LinkedIn, GitHub, direct, Google search

---

## Priority 1: Kill the Redundancy

### Problem
The same 4 facts are repeated 3–5× across the site:
- "7+ years" → Hero badge area, hero desc, hero stats, terminal chat, about section
- "React, Next.js, React Native" → Hero desc, terminal chat, about section
- "1,500+ properties across 21 cities" → Terminal chat, about, experience, projects
- "Rukita" description → Terminal chat, about, experience

This makes the page feel repetitive when scrolled top to bottom. Each section should **earn its space** by adding new information.

### Plan
1. **Hero section** — Owns the "first impression" pitch. Gets the headline stats (7+ years, 297+ features, users served). Sets the tech stack once.
2. **Terminal Chat** — This is a **personality showcase**, NOT a facts section. Rewrite to show voice, humor, and unique angles that aren't covered elsewhere. Should feel like an actual conversation, not a rehashed bio.
3. **About section** — Owns the "how I work" narrative. No repeating stats. Focus on work philosophy, AI-assisted dev approach, and what makes Mugni different.
4. **Experience section** — Owns the detailed track record. This is the only place that mentions company details and bullet-point achievements.
5. **Projects section** — Owns the "what I built" portfolio. Brief, outcome-focused cards.

### Files to Edit
- `Hero.astro` (lines 8, 16–19, 30–44)
- `TerminalChat.astro` (lines 80–130 — conversation data)
- `About.astro` (lines 8–29)

### Key Principle (from Copywriting Skill)
> **One Idea Per Section** — Each section should advance one argument. Build a logical flow down the page.

---

## Priority 2: Rewrite Hero Description (Outcome-Focused)

### Problem
Current hero description is generic and jargon-heavy:
> "Building products people use every day — from real-time chat systems to cross-platform mobile apps. 7+ years shipping web and mobile experiences with React, Next.js, and React Native."

"Products people use every day" could describe any developer. "Shipping...experiences" is corporate speak.

### Plan
1. Replace hero badge text with something specific (not "Crafting great software")
2. Rewrite hero description to lead with **outcomes and proof** (platforms scaled, costs cut, users served)
3. Revise hero stats — replace "8 Products Built" with "30K+ Monthly Users" (more impressive, reader-centric)
4. Keep CTAs as-is ("Get in touch" / "View my work" are clear enough)

### Proposed Copy
```
Badge: "Full-stack · Web & Mobile"

Description: "I build and scale the platforms people rely on daily — from 
real-time chat systems that cut $15K in annual costs to mobile apps serving 
30K+ users across 21 cities."

Stats: 7+ Years | 297+ Features Delivered | 30K+ Monthly Users
```

### Files to Edit
- `Hero.astro` (lines 8, 16–19, 32–43)

### Key Principles
> **Specificity Over Vagueness** — "Cut $15K in costs" beats "building great software"
> **Benefits Over Features** — Reader cares about outcomes, not tech stack listing

---

## Priority 3: Add Metrics to Experience Bullets

### Problem
Several experience bullets use vague language with no numbers:
- "Optimized code to reduce bundle size" — by how much?
- "Accelerated internal operations" — by how much?
- "Improved user experience" — measured how?
- "address issues with the existing library" — what issues?

### Plan
1. **Rukita SE bullets** — Already have some metrics ($15K, 3 months, 15+ modules, 30K MAU, 4 apps). Clean up the language:
   - Lead with the metric/result, not the action
   - Remove filler like "collaborating with engineers, designers, and product managers"
   - Use active voice: "Led" not "Enabled...by leading"
2. **Rukita FE bullets** — Need metrics added. If exact numbers aren't available, use directional language ("2x faster", "halved load time") or note `[add metric]` as placeholders.
3. **Ciayo bullets** — Fix credit-claiming ("Contributed to...30M readers" → "Built for platform serving 30M readers"). Remove implementation details that don't prove impact.

### Proposed Rewrites (examples)
```
BEFORE: "Enabled Rukita's digital platform by leading web (Next.js) and mobile 
(React Native) platform rebuild, collaborating with engineers, designers, and 
product managers to deliver both products in 3 months for the company's expansion 
to 21 cities."

AFTER: "Led full web + mobile platform rebuild (Next.js, React Native) — shipped 
both products in 3 months to support expansion across 21 cities."
```

```
BEFORE: "Optimized code to reduce bundle size and minimize JavaScript downloads, 
ensuring the website loads quickly and efficiently."

AFTER: "Reduced JavaScript bundle size, cutting page load times for a platform 
serving 30K+ monthly users."
```

### Files to Edit
- `Experience.astro` (lines 2–39 — experience data array)

### Key Principles
> **Specificity Over Vagueness** — "Cut your weekly reporting from 4 hours to 15 minutes"
> **Active Over Passive** — "We generate reports" not "Reports are generated"
> **Show Over Tell** — Describe the outcome instead of using adverbs

---

## Priority 4: Rewrite Terminal Chat Conversation

### Problem
The terminal chat currently rehashes the same bio from Hero + About. It's the most creative UI element on the site but the copy is generic and self-promotional ("The kind of dev who obsesses over...", "Wherever there's code that needs to be better, he's there").

### Plan
The terminal chat should serve a **unique purpose**: showing personality and providing info NOT available elsewhere. Think of it as the "conversation you'd have at a coffee chat."

1. **Q1 "who is mugni?"** — Keep short. Add personality/humor. Don't repeat the full bio.
2. **Q2 "what's his stack?"** — Focus on the AI-assisted dev angle (this is his differentiator). Don't just list technologies.
3. **Q3 "what's he building right now?"** — Give a specific, interesting current project detail — not just "Rukita description." What's the latest thing he shipped?
4. **Q4 "can I work with him?"** — Make the CTA warmer and more specific. "He reads every email" is good but the surrounding copy is weak.

### Proposed Conversation
```js
// Q1
"who is mugni?"
→ "Full-stack engineer from Jakarta. 7 years in, still gets excited about 
a clean API response and a smooth scroll animation. Currently building 
at Rukita."

// Q2
"how does he work?"
→ "Pairs with AI (Claude Code, Copilot) to move fast, but every PR still 
gets proper test coverage. His philosophy: AI is a multiplier, not a 
shortcut. Stack: React, Next.js, React Native, TypeScript."

// Q3
"what has he shipped recently?"
→ "Built Rukita's in-house chat system from scratch — replaced Salesforce, 
saved $15K/year, now handles customer service across web, mobile, and 
WhatsApp. Before that, led a full platform rebuild in 3 months."

// Q4
"can I work with him?"
→ "Always open to interesting engineering problems. Reach out at 
iam@mugnimaestra.dev — he responds to every message."
```

### Files to Edit
- `TerminalChat.astro` (lines 80–130 — conversation array)

### Key Principles
> **Be Direct** — Get to the point. Don't bury the value in qualifications.
> **Customer Language Over Company Language** — Write like a human, not a press release.

---

## Priority 5: Strengthen CTAs and Meta Description

### Problem
- Meta description is generic ("Software Engineer with 7+ years building...")
- "Say hello →" is a weak CTA (not action-oriented)
- Contact section copy uses buzzwords ("meaningful work", "great software")

### Plan
1. **Meta title** — Add specificity: include "React/Next.js" for SEO
2. **Meta description** — Lead with proof (297+ features, 30K users), not just years
3. **Contact heading** — Change from cliché "Let's build something together" to direct question
4. **Contact description** — Tell the reader WHY to contact, not just that you "enjoy connecting"
5. **Contact CTA** — Change "Say hello →" to something action-oriented
6. **Footer** — Add GitHub source link (portfolio = portfolio piece)

### Proposed Copy
```
Meta Title: "Mugni Hadi — Full-Stack Engineer · React, Next.js, React Native"
Meta Desc: "Full-stack engineer with 7+ years and 297+ features shipped across 
8 products. Scaled platforms to 30K+ monthly users. Based in Jakarta."

Contact Heading: "Want to work together?"
Contact Desc: "I'm open to new roles, contract work, and interesting engineering 
challenges. Tell me what you're building."
Contact CTA: "Send me an email →"

Footer: "Built with Astro · View source on GitHub"
```

### Files to Edit
- `Layout.astro` (lines 8–9 — title and description)
- `Contact.astro` (lines 8–17 — heading, desc, CTA)
- `Contact.astro` (lines 36–42 — footer)

### Key Principles
> **Strong CTAs** — [Action Verb] + [What They Get]
> **Specificity Over Vagueness** — Concrete beats abstract

---

## Execution Order

| Step | Priority | Files | Est. Effort |
|------|----------|-------|-------------|
| 1 | P2: Hero rewrite | `Hero.astro` | Small |
| 2 | P4: Terminal chat rewrite | `TerminalChat.astro` | Medium |
| 3 | P1: About section (de-duplicate) | `About.astro` | Small |
| 4 | P3: Experience bullet cleanup | `Experience.astro` | Medium |
| 5 | P5: CTAs + Meta + Contact + Footer | `Layout.astro`, `Contact.astro` | Small |

**Total files touched:** 5
**Sections affected:** 6 (Hero, Terminal, About, Experience, Contact, Layout/Meta)

---

## Quality Checklist (from Copywriting Skill)

After implementation, verify:
- [ ] No jargon that could confuse a non-technical hiring manager
- [ ] No sentences trying to do too much
- [ ] No passive voice constructions
- [ ] No exclamation points
- [ ] No marketing buzzwords without substance
- [ ] Each section advances ONE argument
- [ ] Every CTA follows [Action Verb] + [What They Get] formula
- [ ] Consistent voice throughout (professional-conversational)
