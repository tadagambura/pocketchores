# PocketChores: Spec

**The Family Bank: chores, pocket money and real money lessons** · #10 of 32 · Wave 1: Daily keepers · Used: Daily · Harder · Revenue potential: Medium · Family, Pets & Plants · Source: New (Claude)

## One-liner

Turns the family into its own little nation. Parents are the government: they set chores, wages, prices in the family shop, and even the interest rate on savings. Kids are citizens with their own profile and a virtual bank card. They earn family money by doing chores, spend it in the family shop (screen time, treats, a later bedtime), save it to earn interest, or trade favours with siblings. All money in the app is virtual; parents pay real pocket money however they like outside the app.

## Problem / audience

- **Who it's for:** Parents of children aged roughly 5–14.
- **The problem it solves:** Chore charts on the fridge get ignored, and pocket-money maths causes arguments.
- **Example:** On Saturday a parent approves the week's chores; each child's card shows their earnings. One spends 50 on an extra hour of screen time, the other leaves 200 in savings and earns 10 in interest, then trades doing the dishes for their brother's Friday pudding.

## MVP features (ship with only these)

1. Family set-up: parents as 'government', kids as 'citizens' with profiles and virtual bank cards
2. Chores with wages; kids tick off, a parent approves, the money lands on their card
3. Family shop: parents set prices for rewards (screen time, treats, privileges)
4. Savings pot with parent-set interest, paid weekly
5. Favour swaps between siblings, approved by a parent

## Not in MVP

- Separate kid devices (sync)
- Family 'tax' and 'budget' lessons as kids get older
- Goals for big rewards
- Yearly family bank statement

## Monetisation

| Model | Detail |
|---|---|
| Free | One family, 2 children, basic chores and shop |
| Premium | £3.99/month per family: unlimited children, interest, favour swaps, kid devices, history |
| Ads | None (children use it) |

Prices are starting points; test before committing. **Portfolio premium promise:** no ads here because children use it; the free tier is limited instead, and premium adds cloud backup, sync across family devices and the extras.

## Retention: The Progression Loop

| Stage | Design |
|---|---|
| Cue | Daily chores and weekly pay day |
| Tiny win | Tick a chore; a parent taps approve |
| Progress | Card balance, savings growing with interest |
| Share | Parent-shared milestones |
| Next step | Saving goals and new chores as kids grow |
| Cadence | Daily |

Follow the portfolio guardrails: no guilt-trip notifications, no fake urgency, progress is
never wiped, at most one notification a day by default.

## Animation and tone: five signature animations

**Playful.** Celebrations, confetti, cute characters, satisfying sounds and mild comic reactions. Nothing tragic.

- Do the dishes: the stickman stacks plates, they wobble and crash, and it still counts
- Laundry: the stickman staggers under an overflowing basket as socks fly out
- Pay day: the kid's virtual card taps and coins rain into their bank
- Interest paid: the family money tree grows a new coin leaf
- Favour swap: two stickmen shake on it, then one ends up comically buried in the other's dishes

**Line we don't cross:** Children use it: celebrate, never shame. No drama when a chore isn't done.

## AI

**None.** Not needed. Plain code does everything this app does. (Portfolio rule: plain code first, code does the maths,
cheapest model, shared budget cap, premium-gated.)

## Platform & data

- **Platform:** Expo app; separate devices for kids need a shared backend (Supabase).
- **Data:** Virtual money only, no real bank connection. Children's data kept to a minimum.
- **Backend:** Device only on a family phone or tablet; shared data once kids get their own devices. Premium backup and sync use the shared portfolio backend (see the master repo's HOSTING.md).
- **Stack:** shared portfolio foundation (Expo, PostHog, RevenueCat, AdMob, shared Progression Loop module).

## Growth engine

- **Content pillars:** Pocket money ideas; Chores by age; Teaching kids about money
- **Shareable output:** Parent-shared milestones

## Risks

Keep all money virtual: linking real bank accounts or issuing real cards to children is regulated (that's what GoHenry and similar apps are licensed for). Children use it, so follow the UK Children's Code and app-store kids rules: no ads, minimal data, parent controls, no manipulative rewards.

## Launch checklist

- [ ] Name checked on the App Store, Play Store and a trademark search
- [ ] MVP features done and tested
- [ ] Progression Loop wired (cue, tiny win, progress, milestone, next step)
- [ ] Privacy policy and terms
- [ ] Landing page
- [ ] Analytics wired (D1/D7/D30 retention)
- [ ] Payments / ads wired
- [ ] Added to the Growth & Maintenance Engine as an app config
