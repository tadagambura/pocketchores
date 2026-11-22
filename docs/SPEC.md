# PocketChores: Spec

**Chores and pocket money, sorted** · #28 of 33 in the build order · Harder · Revenue potential: Medium · Family, Pets & Plants · Source: New (Claude)

## One-liner

Parents set chores and rewards, kids tick them off, and PocketChores keeps the pocket-money tally and each child's savings goals. Starts as a single family device; separate kid devices come later.

## Problem / audience

- **Who it's for:** Parents of children aged roughly 5–14.
- **The problem it solves:** Chore charts on the fridge get ignored, and pocket-money maths causes arguments.
- **Example:** On Saturday a parent approves the week's ticked chores and sees each child's pocket money and savings progress.

## MVP features (ship with only these)

1. Chores with points or money values
2. Kids tick off; a parent approves
3. Weekly pocket-money total
4. Kids' savings goals
5. Family device mode (no child accounts)

## Not in MVP

- Separate kid devices (sync)
- Rewards shop
- Allowance history

## Monetisation

| Model | Detail |
|---|---|
| Free | 2 children, basic chores |
| Premium | £2.99/month: unlimited children, goals, history, kid devices |
| Ads | None (children may use it) |

Prices are starting points; test before committing.

## Retention: The Progression Loop

| Stage | Design |
|---|---|
| Cue | Weekly pocket-money day |
| Tiny win | Tick or approve a chore |
| Progress | Pocket money earned; savings goals |
| Share | Milestones shared by parents |
| Next step | Next week's chores |
| Cadence | Daily/weekly |

Follow the portfolio guardrails: no guilt-trip notifications, no fake urgency, progress is
never wiped, at most one notification a day by default.

## Platform & data

- **Platform:** Expo app; kid devices need Supabase.
- **Data:** On the device first; children's data kept to a minimum.
- **Stack:** shared portfolio foundation (Expo, PostHog, RevenueCat, AdMob, shared Progression Loop module).

## Growth engine

- **Content pillars:** Pocket money ideas; Chores by age; Teaching kids about money
- **Shareable output:** Milestones shared by parents

## Risks

Children may use it, so follow the UK Children's Code and app-store kids rules: no ads, minimal data, parent controls.

## Launch checklist

- [ ] Name checked on the App Store, Play Store and a trademark search
- [ ] MVP features done and tested
- [ ] Progression Loop wired (cue, tiny win, progress, milestone, next step)
- [ ] Privacy policy and terms
- [ ] Landing page
- [ ] Analytics wired (D1/D7/D30 retention)
- [ ] Payments / ads wired
- [ ] Added to growth-engine as an app config
