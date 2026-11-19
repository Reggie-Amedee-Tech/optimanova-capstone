# Saturday Volunteer Planner: OptimaNova AI Capstone

An AI helper that drafts the Saturday volunteer plan for **Linden Street Community Partners**, a community pantry. It drafts, and people decide: nothing goes out until the Operations & Finance Manager approves it and sends it herself.

All names and data in this repo are made up for the capstone.

**Demo video:** [Watch the client demo on Loom](https://www.loom.com/share/9a6fa8f784104e539049fd33b8eb7ca2)

## The problem

Gloria Ortiz, Operations & Finance Manager, runs Saturday volunteer scheduling from a paper sign-up sheet and group texts on her personal phone.

- She spends "about four hours every week" scheduling, confirming, and sending reminders, on top of finance, facilities, and technology.
- Last month about 5 of the usual 25 Saturday volunteers didn't show. She spent the morning texting people last-minute while the families' line formed outside.
- When the pantry is short-handed on a Saturday, morning prep can be set back 30 to 45 minutes, which delays opening for families. Programs Director Marcus Bell confirmed that empty volunteer spots delay setup.
- Her success measure: a reliable roster, and a tool "simple and accessible enough that our volunteers will actually use it."

Evidence and workflow maps are in [01-discover](01-discover/README.md).

## The build

A Gemini Gem (an assistant, not an automation) called the Saturday Volunteer Planner. Gloria pastes in first names, shifts, and preferred languages. The Planner:

1. Asks about anything missing instead of guessing.
2. Drafts a starting plan across four jobs: unloading, packing bags, check-in, and handing food out.
3. Lists coverage gaps against about 25 volunteers.
4. Drafts an orientation notice under 120 words, signed from Gloria.
5. When Gloria says who didn't show, suggests same-shift moves for her to approve.

It does not send messages, store the volunteer list, move anyone to a shift they didn't choose, or make final placements. Version 1 does not take texting off Gloria's personal phone.

Gem instructions and the 9-test log (made-up data only) are in the Build section of the Capstone Package. Handoff and training are in [05-enable](05-enable/handoff.md).

## The human check

- **Gloria Ortiz** reads and approves every plan and notice before anything is shared, and sends every message herself.
- **Marcus Bell or the floor lead** makes the final placements on Saturday morning.
- **A fluent staff member** reviews any Spanish or Haitian Creole text before it goes out. The Planner labels it "Needs fluent review."
- **The Four Checks** on every draft: **Source** (does every name and shift match the sheet?), **Specifics** (names, shifts, dates, arrival times), **Sense** (does it fit how Saturday works?), **Sensitivity** (nothing private).

During testing, one run listed two volunteers under a shift they hadn't chosen. Checking names against shifts caught it. The handoff rule applies: don't share the draft, correct it, and tell the Planner what was wrong.

Real volunteer data does not go in until the OptimaNova Advisor and Linden Street approve it. See [bright-line flags](01-discover/bright-line-flags.md).

## Before and after

| | Number | Basis |
|---|---|---|
| Today | About 4 hours a week scheduling, confirming, and reminding | Gloria's own estimate |
| With the Planner | About 50 minutes a week back, about 3.5 hours a month | **Estimate, not a measured result.** Assumes about 1 of Gloria's 4 weekly hours is planning and orientation details. An eight-person test took about 4.5 minutes including review; for 25 volunteers we estimate about 10 minutes a week. |

How we'll know: for four weeks, Gloria tracks weekly scheduling time, Saturday no-shows, minutes spent rearranging on Saturday morning, and how late the doors open.

## Screenshots

![The Planner asks about job targets before drafting](assets/screenshots/01-asks-for-targets.png)
![Starting plan, labeled as a starting plan](assets/screenshots/02-starting-plan.png)
![A shift error caught by the Specifics check](assets/screenshots/03-duplicate-shift-error.png)
![Translated text labeled Needs fluent review](assets/screenshots/04-needs-fluent-review.png)
![Same-shift moves after a no-show](assets/screenshots/05-no-show-revision.png)

## My part and the team's parts

This was a team capstone, and each teammate posts their own copy.

| Phase | Owner |
|---|---|
| Discover | **Reginald Amedee (this repo's author)** |
| Enable (handoff doc, training video, transcript) | **Reginald Amedee** |
| Diagnose (readiness findings) | Dwayne Saxton |
| Build (documented build and test log) | Dwayne Saxton |
| Governance one-pager | Dwayne Saxton |
| Design (roadmap and solution spec); original Planner Gem | Enrique Quezada |

## Repo layout

```
README.md
01-discover/      evidence table, workflow maps, bright-line flags
05-enable/        handoff doc, training script, training transcript
assets/           screenshots
```

## AI use

AI helped draft these materials. All quotes and numbers in Discover were checked against the source interview transcripts, and all Planner tests used made-up data.
