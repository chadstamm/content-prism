---
name: content-prism
description: Blue-ocean content ideation engine. Use when the user HAS an idea and wants to find the freshest, most differentiated way to deliver it — and to pressure-test it before writing. Triggers when they say "I've got an idea," "run this through the prism," "punch holes in this," "is this angle fresh," "everyone's saying the same thing about X," "blue ocean this," "find a better angle for my idea," or "stress-test this take." Grounds the idea in three audience-truth questions, maps how it's already being delivered, splits it into differentiated angles, pressure-tests each one, and outputs a focused delivery. Ideation and stress-test tool, not a drafting tool — hand the result to a writing workflow.
---

# Content Prism

*You bring the idea. The Prism finds the angle nobody's running — and punches holes in it before you write.*

## What it does

You bring an idea. Most AI ideation takes that idea straight into the "red ocean" — the same obvious framings everyone already uses, because everyone starts in the same place. Content Prism starts at the opposite end.

Think of your idea as a beam of **white light** — which looks like everyone else's, all the takes blurred into the same indistinct thing. The Prism splits it into a **spectrum** of distinct, differentiated angles, pressure-tests each one, and focuses down to a single coherent **beam**: the sharpest, most defensible way to deliver *your* idea.

Two moves, always in order:

1. **Diverge** — split the idea open. Map what everyone's already saying, then break it into angles they're not.
2. **Converge** — focus. Pressure-test the angles, drop the ones that don't hold, and narrow to the one worth writing.

> **This is an ideation and stress-test tool, not a drafting tool.** It finds the angle and tells you where it's weak. Turning it into great content still takes your taste and craft. Don't let it write the piece.

## When to use

- "I've got an idea — run it through the prism."
- "Punch holes in this angle before I write it."
- "Everyone's saying the same thing about [topic] — what's the fresh delivery?"
- Any time you have a take and want it sharper, more differentiated, and battle-tested.

## What belongs here (scope)

The Prism works on ideas that have to **win attention in a crowded conversation**. Three things must be true, or it can't do its job:
1. A real audience with a problem (CALIBRATE needs one).
2. An existing, saturated conversation to differentiate from (WHITE LIGHT needs one).
3. The intent is to persuade or position — not to express or record.

**Built for:** POV and thought-leadership (LinkedIn, Substack, newsletters), company and client content (blogs, positioning, campaigns), launch narratives, talk and podcast angles — anything that has to stand out in a feed.

**Not for:** fiction, memoir, personal narrative, journaling, technical docs, factual reporting. Those are about truth and craft, not differentiation from competitors. If the idea is one of these, **say so plainly and decline** — don't force a marketing frame onto art or a record.

## Intake — gather before you start

**Required:**
- **The idea** — the take, angle, or argument you want to deliver. Not a bare topic — your actual idea.
- **The audience** — who this is for. If the idea implies it, infer and confirm; otherwise ask.

**Optional but useful:**
- **Format / goal** — blog, LinkedIn, Substack, email, podcast, and what it should accomplish.
- **What you already know is overdone** — saturated framings to skip.

If the idea or audience is unclear, ask — one question at a time.

## The flow

```
CALIBRATE → WHITE LIGHT → SPECTRUM → PUNCH HOLES → FOCUS → THE BEAM
```

### 1. CALIBRATE — ground the idea
Before splitting anything, aim the prism. Answer the three audience-truth questions for this idea:
- **External problem** — the reader's #1 problem, in how they *talk* about it
- **Internal frustration** — what's underneath it, how they *feel*
- **Transformation** — how their world is better if they get this right

This isn't a constraint on creativity — it's the aim. Audience-truth and angle-freshness are different axes, so grounding here doesn't dull the divergence; it points it somewhere useful. If you can't answer the three, that's a signal the idea isn't ready — say so.

### 2. WHITE LIGHT — map the saturated takes
Research how this idea is *already* being delivered for this audience. Use web search plus reasoning. Name the 3–5 most saturated framings — the takes blurred into sameness. You can't differentiate from what you haven't mapped.

### 3. SPECTRUM — split into fresh angles *(diverge)*
Break the idea into distinct, differentiated deliveries using the lenses in `references/angle-categories.md`. Each delivery is a **band**. Aim for **breadth, not quality control yet** — this is expansion. Don't self-censor; a weak-looking band often points at a strong one. Every band must still serve the Calibration (the grounded problem) — fresh *and* true, never clever-but-useless.

### 4. PUNCH HOLES — pressure-test *(converge begins)*
Switch from expansion to adversarial evaluation. For each surviving band, find where it breaks: the strongest objection, the saturated trap it risks falling into, the claim you can't back. An angle that flips the consensus but can't survive a smart reader is a hot take, not an idea. Note the holes — they travel into the output.

### 5. FOCUS — score, then auto-fire the top band
Score the bands on the rubric in `references/scoring-rubric.md` (differentiation · audience relevance · defensibility · on-brand fit). **Auto-select the top-scored band and proceed straight to THE BEAM — do not gate on the human's pick.** The model proposes; the human disposes. Present the full scored field (top 2–3 with a one-line case each, plus the runner-up bands) *inside the Beam itself* so the choice stays visible, and tell the human they can re-pick at any time ("rebuild it on Forgotten Precedent") or re-split. The pick is a **revision, not a gate** — the visual artifact fires first so there's always something concrete to react to. Still flag any high-differentiation / low-defensibility band as high-risk so a re-pick is made with eyes open.

### 6. THE BEAM — the output (fires automatically)
Produce the focused delivery on the **top-scored band** as a **styled HTML one-pager**, and `open` it without waiting for confirmation. Use `references/beam-template.html` as the design — it carries the brand fonts, colors, the prism hero, and the six-lens spectrum, all self-contained (the hero is embedded as a data URI). Copy its structure and CSS verbatim and fill the `{{TOKENS}}`:
- `{{IDEA_TITLE}}` · `{{AUDIENCE}}` · `{{FORMAT}}` · `{{DATE}}` (run today's `date`)
- `{{EXTERNAL_PROBLEM}}` · `{{INTERNAL_FRUSTRATION}}` · `{{TRANSFORMATION}}` (from CALIBRATE)
- `{{WHITE_LIGHT_ITEMS}}` — one `<li>` per saturated take
- `{{BEAM_LENS}}` + `{{BEAM_LENS_COLOR}}` — the winning lens name and its spectrum hex (Hidden Cost `#DA5525` · Second-Order `#C4943A` · Misattributed Hero `#2D4A3A` · Premature Consensus `#1EBEB1` · Forgotten Precedent `#1F628E` · Reframe `#5C4D85`)
- `{{BEAM_BODY}}` — the recommended delivery paragraph
- `{{BANDS}}` — one `.band` row per runner-up (swatch hex, headline, one-line case, score/20)
- `{{HOLES}}` — one `<li>` per hole from PUNCH HOLES

Save to `~/Desktop/the-beam-[topic-slug]-[date].html` and `open` it in the browser. The content spec for what each field should contain is in `references/beam-template.md`. Decision-grade, not research-grade.

Only when the user asks (`--brief` / "give me the full brief") expand the chosen band into the **Full Spectrum brief** in `references/brief-template.md` — sourced stats, quotes, precedent, citations. That's drafting fuel, and it's overkill until a direction is locked.

## Integrity rules

- **Never fabricate a stat, quote, or source.** Unsourced-but-plausible is flagged, never shipped.
- **Stay in scope.** If the idea is art, expression, or record (fiction, memoir, journaling, docs), decline and explain — don't force a marketing frame onto it.
- **Map before you split.** Skipping WHITE LIGHT produces fake contrarianism.
- **Expand before you evaluate.** Don't quality-control during SPECTRUM or you collapse back into white light.
- **Holes are a feature.** Always surface where the chosen angle is weak — the point is a battle-tested idea, not a flattering one.
- **Model proposes, human disposes.** FOCUS auto-fires the top-scored band as the Beam and opens it — the human re-picks by asking (a revision, not a gate). The artifact comes first; the choice stays editable. Never bury a fatal flaw to make the auto-pick look good — a band with a 1 in any dimension gets named out loud, not averaged away.

## Tuning it for your audience

The lenses in `references/angle-categories.md` are a starting set — universal angle *types*, not audience pillars. Edit, cut, or add them; the engine uses whatever's in that file. Audience-specific calibration happens at CALIBRATE, WHITE LIGHT, and FOCUS — not in the lens set.
