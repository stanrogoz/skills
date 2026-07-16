# Skills

A practical framework for turning AI inputs into **decision-ready outputs**.

Created by [Stan Rogoz](https://github.com/stanrogoz).

## Available skills

| Skill | Description |
| --- | --- |
| [`5p-framework`](skills/5p-framework/SKILL.md) | Apply the 5P Framework (Pause, Play, Push, Polish, Present) by Stan Rogoz to turn a request into a decision-ready output instead of a quick first-pass answer. The agent invokes this automatically when a request calls for a defensible decision. |

## Quickstart (30-second setup)

1. Run the skills.sh installer:

```bash
npx skills@latest add stanrogoz/skills
```

2. Pick the skills you want, and which coding agents you want to install them on.

3. Run `/5p-framework` in your agent (or let it trigger automatically when you ask for a decision). It will walk you through the 5 steps as a conversation — asking one question at a time, with a recommended answer, and confirming each step with you before moving on:

| Step | Goal |
|------|------|
| **Pause** | Plan the objective and add context before you prompt. |
| **Play** | Open up the space — explore options and alternatives. |
| **Push** | Challenge assumptions and stress-test the reasoning. |
| **Polish** | Finalise a clear, accurate, on-brand output. |
| **Present** | Prepare for scrutiny — surface risks, trade-offs, and objections. |

## More information

The 5P Framework guide is available at [stanrogoz.github.io/5p-framework](https://stanrogoz.github.io/5p-framework/).
