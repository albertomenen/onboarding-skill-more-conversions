# CLAUDE.md

Operational guidance for Claude Code when developing and maintaining this skill.

---

## 0) Skill identity (keep this consistent)

- **Skill name:** `app-onboarding-optimization`
- **Invocation command:** `/app-onboarding-optimization`
- **Primary instruction file:** `SKILL.md`
- **This file:** contributor/developer guardrails

**Hard rule:** Use the same name in repo docs, SKILL frontmatter, and command examples.

---

## 1) Mission

Build app-specific onboarding flows that increase the probability of conversion to subscription by improving:

- early motivation
- perceived relevance
- first value delivery
- paywall transition quality

The skill must produce outputs that are **implementation-ready**, not generic advice.

---

## 2) Execution contract (always follow)

When `/app-onboarding-optimization` is invoked inside a user project:

1. **Inspect first, suggest second**
   - Detect stack (SwiftUI/UIKit/React Native/Flutter/Compose/etc.)
   - Locate onboarding entry points and paywall trigger points
   - Identify permission usage signals (`Info.plist`, `AndroidManifest.xml`, etc.)

2. **Map current flow**
   - List current screens/steps in order
   - Label each with intent (hook, profiling, proof, activation, monetization)
   - Mark missing/high-friction phases

3. **Define user transformation**
   - Desired outcome
   - Main blockers
   - Objections/trust gaps

4. **Design improved flow**
   - Use reference sequence (Section 4), adapt by complexity
   - Keep only high-leverage steps
   - Define transitions and why each screen exists

5. **Produce implementation plan**
   - Prioritized tasks (P0/P1/P2)
   - Screen-level copy direction
   - Interaction specs for the functional demo
   - Permission priming timing

6. **Ask minimal clarifying questions**
   - Only for info unavailable in code
   - Keep question sets short and decision-relevant

---

## 3) Deliverables format (required)

Every full run should output these sections in this order:

1. **Current Flow Audit**
2. **Gap Analysis**
3. **Proposed Onboarding Architecture**
4. **Screen-by-Screen Spec**
5. **Implementation Tasks (P0/P1/P2)**
6. **Experiment Plan (A/B ideas + success metrics)**

If any section is missing, the run is incomplete.

---

## 4) Reference sequence (adaptive, not rigid)

Default archetype:

1. Hook
2. Goal capture
3. Pain discovery
4. Social proof
5. Interactive self-identification
6. Personalized mapping
7. Comparison (optional)
8. Preferences
9. Permission priming
10. Processing moment
11. Functional demo
12. Value delivery
13. Account gate (optional)
14. Paywall

**Adaptation rules:**
- Remove low-value steps for simple apps
- Keep trust + activation steps for high-ticket/subscription apps
- Never force all 14 screens if it hurts clarity

---

## 5) Non-negotiables

1. **Functional demo over passive walkthrough**
   - Users should perform a real core action when feasible

2. **Permission priming before native prompts**
   - Explain user benefit in-app before OS dialogs

3. **Native-feeling UX**
   - Match existing component patterns and tone

4. **No invented claims**
   - Do not fabricate uplift percentages or benchmark certainty

5. **Conversational copy**
   - Passes the “would I say this to a friend?” test

---

## 6) Actionable checklists

### A) Discovery checklist
- [ ] Stack/framework identified
- [ ] Onboarding entry + exit points identified
- [ ] Paywall trigger(s) identified
- [ ] Permissions required by features identified
- [ ] Existing analytics events noted (if present)

### B) Blueprint checklist
- [ ] Clear screen order
- [ ] Objective per screen
- [ ] Input/output per screen
- [ ] Branching/personalization logic defined
- [ ] Drop-off risk points identified

### C) Demo-screen checklist
- [ ] Real core interaction defined
- [ ] User performs an action, not just reads
- [ ] Tangible output shown
- [ ] Output can be saved/shared when relevant
- [ ] Transition to paywall is context-linked to generated value

### D) Paywall-transition checklist
- [ ] Value reminder immediately before paywall
- [ ] Offer framing matches user goal/pain inputs
- [ ] Trial/pricing explanation is plain language
- [ ] Primary CTA is single, clear, and visible

### E) Implementation checklist
- [ ] P0 tasks can be shipped first without full redesign
- [ ] Engineering effort estimates included (S/M/L)
- [ ] Dependencies/risks called out
- [ ] Rollout and fallback plan included

---

## 7) Quality bar (Definition of Done)

A run is “done” only if:

- Output is app-specific (not template text)
- Developer can implement without guessing intent
- Priorities are explicit (what to ship first)
- At least one experiment loop is defined

If not, iterate before finalizing.

---

## 8) Experiment loop (minimum viable testing)

For each major onboarding change, propose:

- **Hypothesis:** what should improve and why
- **Primary metric:** onboarding completion, trial start rate, paywall CVR, etc.
- **Guardrail metric:** uninstall rate, time-to-value, permission denial rate
- **Decision rule:** keep/kill/iterate criteria

Keep experiments lightweight and shippable.

---

## 9) Do / Don’t

### Do
- Ground recommendations in repository evidence
- Prefer incremental wins before full rewrites
- Keep guidance clear, concrete, and prioritized

### Don’t
- Output generic “best practices” with no mapping to app context
- Overload users with long questionnaires
- Break current product UX for theoretical conversion gains

---

## 10) Maintenance rules

When updating this skill:

- Keep `SKILL.md` concise; move long specifics to references if needed
- Preserve command/name consistency
- Validate examples against real app flows before publishing
- Document any major framework or logic changes in commit messages
