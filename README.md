# Onboarding Skill — More Conversions

Design a code-aware onboarding flow that turns new users into paying subscribers.

`onboarding-skill-more-conversions` is a Claude Code skill that analyzes your app and builds a high-converting onboarding architecture — from first impression to paywall — using proven conversion psychology and practical implementation guidance.

---

## Why this skill exists

Most onboarding flows are too short, too generic, and too disconnected from the product’s real value.

This skill fixes that by helping you:

- Increase activation intent before monetization
- Improve onboarding-to-paywall conversion quality
- Reduce drop-off with better sequencing and context
- Introduce product value earlier through real interaction

---

## What it does

Run this command in Claude Code:

```bash
/app-onboarding-optimization
```

The skill will:

1. Analyze your codebase and detect your current onboarding flow
2. Break the flow into phases and classify intent per screen
3. Identify your product core loop and value moment
4. Detect likely permission requirements from platform files
5. Propose a stronger onboarding sequence and transition logic
6. Ask only for the context it cannot infer from code (e.g., audience insights, user feedback)
7. Output an implementation-ready onboarding blueprint

---

## Conversion framework (adapted per app)

The skill uses a structured sequence inspired by high-performing subscription apps:

| # | Phase | Purpose |
|---|------|---------|
| 1 | Welcome Hook | Show desired end-state and create motivation |
| 2 | Goal Capture | Build commitment with explicit intent |
| 3 | Pain Discovery | Surface blockers and user relevance |
| 4 | Social Proof | Reduce skepticism with trust signals |
| 5 | Interactive Self-ID | Increase engagement via user participation |
| 6 | Personalized Mapping | Reflect pains and show tailored solution |
| 7 | Comparison (Optional) | Clarify value gap: with vs without app |
| 8 | Preferences | Collect lightweight customization |
| 9 | Permission Priming | Pre-frame native permissions with user benefit |
| 10 | Processing Moment | Build anticipation before value reveal |
| 11 | Functional Demo | Let the user perform a core product action |
| 12 | Value Delivery | Return a tangible result/output |
| 13 | Account Gate (Optional) | Save/unlock generated value |
| 14 | Paywall | Present pricing/trial with contextual value |

> Not every app needs every phase. The skill adapts to complexity, product model, and UX constraints.

---

## What makes this different

### 1) Code-aware, not template-only
Recommendations come from your repository structure and product flow, not generic copywriting prompts.

### 2) Demo-first onboarding logic
Instead of passive slides, the framework pushes for real user interaction before paywall.

### 3) Permission-aware sequencing
The skill checks files like `Info.plist` and `AndroidManifest.xml` to time permission prompts more intelligently.

### 4) Built for iteration
You can refine screen structure, copy, and conversion logic over multiple sessions.

---

## Installation

### Option A — Install locally in Claude skills directory

```bash
cd ~/.claude/skills
git clone git@github.com:albertomenen/onboarding-skill-more-conversions.git
```

### Option B — Add as dependency in project settings

`.claude/settings.json`

```json
{
  "skills": [
    "github:albertomenen/onboarding-skill-more-conversions"
  ]
}
```

---

## Usage

From your app project folder:

```bash
/app-onboarding-optimization
```

Expected workflow:

- Initial repository scan
- Structured diagnostic of current onboarding
- Gap analysis against conversion framework
- Interactive clarification questions
- Final onboarding blueprint with priorities

---

## Expected outputs

- Recommended onboarding sequence (ordered + rationale)
- Screen-by-screen objective and UX intent
- Personalization and branching opportunities
- Permission priming and timing strategy
- Functional demo concept tied to your core loop
- Paywall transition recommendations

---

## Scope and limitations

### In scope
- Onboarding architecture
- Conversion sequencing
- UX messaging strategy
- Permission pre-prompt planning
- Monetization handoff logic

### Not in scope
- Guaranteed conversion uplift
- Automatic production code deployment
- Full legal/compliance review
- Full localization strategy

> Results depend on product quality, traffic source quality, pricing model, and execution quality.

---

## License

MIT
