---
name: 5p-framework
description: Apply the 5P Framework (Pause, Play, Push, Polish, Present) to produce a decision-ready output. Use when the user asks for a recommendation or a decision ("should we / which one / what's the best way"), when the output will go in front of stakeholders, a boss, or a client, or when the user mentions the 5P framework, "decision-ready", or asks to stress-test or pressure-test a plan or idea.
---

# 5P Framework

A five-step (Pause, Play, Push, Polish, Present) loop for AI-augmented decision-making, created by Stan Rogoz. The problem it solves: by default AI often produces a quick and easy answer, but rarely a defensible one. People latch onto the first plausible option, skip the alternatives, hide the assumptions, and hand over something that falls apart under the first hard question from stakeholders. The 5P loop forces divergence before convergence and scrutiny before delivery, so the final output holds up in any meeting room.

Work through the five steps **in order** — Pause, Play, Push, Polish, Present. Framing before exploring, exploring before critiquing, critiquing before finalising. Skipping ahead or going out of order recreates exactly the failure mode the loop exists to prevent.

## The Five Steps (In Order)

### 1. Pause — plan the objective, add context

Before producing anything, get clear on what a good answer even looks like.

- Find out what is the actual decision being made, the requirements, and what "done" looks like.
- Identify the audience, constraints, and available data. Pull relevant context from the conversation, attached files, or the codebase before assuming.
- Choose the output format the situation actually needs (a one-pager, a table, a memo, a code change with rationale).

Pause step is only done when the decision, the audience, and the output format are each stated explicitly. If the decision itself is ambiguous — you genuinely can't tell what's being decided or for whom — always ask. Otherwise, state your framing explicitly and proceed; a visible framing the user can correct beats a stalled task.

### 2. Play — open up the space

Go wide before you go deep. Generate several (at least three) genuinely distinct options or framings — not one idea plus two strawmen.

- Aim for 3–5 real alternatives, including at least one unconventional or contrarian take.
- Stay divergent here: describe each option on its own terms. Judging happens in the next step, and judging early is what collapses the space back to the first plausible answer.

### 3. Push — challenge assumptions

Now apply pressure, so weak ideas break here instead of in front of stakeholders.

- For the leading options, ask "what would have to be true for this to work?" and check whether it is.
- Critique like a constructive, but well intended reviewer: surface hidden assumptions, counter-arguments, and failure modes.
- Verify claims where you can — check the numbers, the sources, the edge cases.

Push is only done when every surviving option has its load-bearing assumptions named, and each one is either verified or flagged as an assumption rather than presented as fact.

### 4. Polish — finalise the output

Converge. Turn the surviving reasoning into the output version you would actually ship proudly.

- Lead with the proposed output and the why (important).
- Create a clear structure, tight prose, accurate details, the right tone for the audience identified at the beginning.
- Cut the working notes; the exploration was for you, the reader gets the final conclusion.
- Adapt the format to what was identified — a Slack reply needs less scaffolding than a board memo.


### 5. Present — prepare for scrutiny

The output isn't done until it can survive the scrutiny of the stakeholders.

- List the likely objections to the final version, and how you'd answer them.
- Be explicit about risks, trade-offs, and what was deliberately not chosen and why.
- Keep the working available — show how you got here, so the reasoning can be audited.

## Output shape

The final deliverable should read as decision-ready, not as a transcript of the process. A structure that works for most cases:

1. **Recommendation** — the decision and the core reason from Pause, up front.
2. **Options considered** — the real alternatives from Play, each with why it lost (or when it would win instead).
3. **Key assumptions and risks** — what has to be true, what could break, from Push.
4. **Anticipated objections** — the hard questions and your answers, from Present.
5. **Decision-ready output** — Adapt the format to what was identified in Pause (a Slack reply needs less scaffolding than a board memo), but never drop the substance: alternatives considered, assumptions named, risks surfaced.

## Scaling the loop

The loop scales from a five-minute question to a board-level recommendation. For small decisions, each step might be a sentence or two — but still touch each step. The cheapest way to fail is to skip Play (one option presented as inevitable) or Push (no assumption ever questioned). If the user asks for a quick take, compress the loop; don't abandon it. Signal the compression: "Quick version — happy to run the full loop if this is going in front of someone."
