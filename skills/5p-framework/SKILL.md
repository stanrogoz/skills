---
name: 5p-framework
description: Apply the 5P Framework (Pause, Play, Push, Polish, Present) as a step-by-step conversation with the user, producing a decision-ready output. Use when the user asks for a recommendation or a decision ("should we / which one / what's the best way"), when the output will go in front of stakeholders, a boss, or a client, or when the user mentions the 5P framework, "decision-ready", or asks to stress-test or pressure-test a plan or idea.
---

# 5P Framework

A five-step (Pause, Play, Push, Polish, Present) loop for AI-augmented decision-making, created by Stan Rogoz. The problem it solves: by default AI often produces a quick and easy answer, but rarely a defensible one. People latch onto the first plausible option, skip the alternatives, hide the assumptions, and hand over something that falls apart under the first hard question from stakeholders. The 5P loop forces divergence before convergence and scrutiny before delivery, so the final output holds up in any meeting room.

Run the loop **as a conversation with the user, not a monologue**. Walk the five steps in order — Pause, Play, Push, Polish, Present — and discuss each step with the user before moving to the next. Skipping ahead, going out of order, or racing through the steps without the user recreates exactly the failure mode the loop exists to prevent.

<HARD-GATE>
Each step ends with an explicit confirmation question to the user, and the next step does not begin until they answer yes. Never cover more than one step in a single message. Never deliver the final output until the user has confirmed all five steps in turn. This applies to EVERY request, no matter how simple it looks.
</HARD-GATE>

## Conversation rules (apply at every step)

- Announce which step you are in, so the user always knows where they are in the loop.
- Ask questions **one at a time**, waiting for the user's answer before asking the next. Asking multiple questions at once is bewildering.
- Provide your **recommended answer** with every question you ask.
- If a *fact* can be found by exploring the conversation, attached files, or the codebase, look it up rather than asking. The *decisions* are the user's — put each one to them and wait for their answer.
- End every step by explicitly asking for confirmation, e.g. "Is Pause settled, or is there anything to adjust before we move to Play?" A user reply that answers your last question is **not** confirmation to advance — ask.
- Do not advance to the next step until the user answers that explicit question with a yes.
- Do not deliver the final output until the user confirms you have reached a shared understanding.

## Anti-patterns (each of these defeats the loop)

- **The five-step monologue** — presenting all five steps in one message, each neatly labeled. Labeling the steps is not running the loop; the user weighing in between steps is.
- **Silent advancement** — treating any user reply as blanket approval and rolling into the next step. Advancement requires a yes to an explicit "is this step settled?" question.
- **"Too simple for the loop"** — deciding the request is trivial and skipping steps. Simple requests are where unexamined assumptions survive longest. Compress the steps (see Scaling the loop); never skip the check-ins.
- **Question barrage** — asking three questions at once to "save time". One question, one answer, one recommendation.

## The Five Steps (In Order)

### 1. Pause — agree on the framing, request context

Before producing anything, agree with the user on what a good answer even looks like.

- Establish the actual decision being made, the audience, the constraints, the available data, and what "done" looks like.
- Establish the output format the situation actually needs (a one-pager, a table, a memo, a code change with rationale).
- Pull what you can from context first, then put each remaining unknown to the user as a single question with your recommended answer.

Pause is settled when the user has confirmed the decision, the audience, and the output format.

### 2. Play — open up the space together

Go wide before you go deep. Generate several genuinely distinct options or framings — not one idea plus two strawmen.

- Present 3–5 real alternatives, including at least one unconventional or contrarian take.
- Stay divergent here: describe each option on its own terms. Judging happens in the next step, and judging early is what collapses the space back to the first plausible answer.
- Then discuss: ask the user which options resonate, whether any should be added or dropped, and whether you've missed a framing they had in mind — one question at a time, with your recommendation.

Play is settled when the user has confirmed the shortlist of options worth stress-testing.

### 3. Push — challenge assumptions together

Now apply pressure, so weak ideas break here instead of in front of stakeholders.

- For each shortlisted option, ask "what would have to be true for this to work?" and check whether it is.
- Critique like a constructive, well-intended reviewer: surface hidden assumptions, counter-arguments, and failure modes.
- Verify claims where you can — check the numbers, the sources, the edge cases. Where an assumption only the user can confirm remains (their team, their budget, their stakeholders), put it to them as a question with your best read.
- Walk down each branch of the reasoning, resolving dependencies between decisions one by one.

Push is settled when every surviving option has its load-bearing assumptions named — each verified or explicitly flagged as an assumption — and the user has confirmed which option leads.

### 4. Polish — converge on the deliverable, finalise the output together

Turn the surviving reasoning into the output version you would actually ship proudly.

- First propose the shape: structure, tone, and level of detail for the audience agreed in Pause. Ask the user to confirm or adjust before writing the final version.
- Lead with the proposed output and the why (important).
- Create a clear structure, tight prose, accurate details, the right tone. Cut the working notes; the exploration was for the two of you, the reader gets the final conclusion.
- Adapt the format to what was agreed — a Slack reply needs less scaffolding than a board memo.

Polish is settled when the user has confirmed the draft is the version they'd ship.

### 5. Present — rehearse the anticipated scrutiny together

The output isn't done until it can survive the scrutiny of the stakeholders.

- List the likely objections to the final version and how you'd answer them.
- Be explicit about risks, trade-offs, and what was deliberately not chosen and why.
- Then ask the user — one question at a time — who is most likely to push back, and on what. Fold their answers into the objection list.
- Keep the working available — show how you got here, so the reasoning can be audited.

Present is settled when the user confirms the output would hold up in the room it's headed for. Only then deliver the final output.

## Output shape

The final deliverable should read as decision-ready, not as a transcript of the conversation. A structure that works for most cases:

1. **Recommendation** — the decision and the core reason from Pause, up front.
2. **Options considered** — the real alternatives from Play, each with why it lost (or when it would win instead).
3. **Key assumptions and risks** — what has to be true, what could break, from Push.
4. **Anticipated objections** — the hard questions and your answers, from Present.
5. **Decision-ready output** — in the format agreed in Pause, but never drop the substance: alternatives considered, assumptions named, risks surfaced.

## Scaling the loop

The loop scales from a five-minute question to a board-level recommendation. Compression changes the **size of each step, never the number of check-ins**: for a small decision, a step might be a single exchange — one framing question, a quick shortlist, one assumption check — but every step still happens in order, and every step still ends with the explicit "is this settled?" question before the next begins. The cheapest way to fail is to skip Play (one option presented as inevitable) or Push (no assumption ever questioned). If the user asks for a quick take, say what compression means concretely — "Quick version: one question per step instead of a full pass — say the word if this is going in front of someone and I'll run it deep" — and then still walk the five gates.
