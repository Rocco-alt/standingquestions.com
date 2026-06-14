# Prompt patterns: moving a register

Structural constraints move a model's output register more reliably than quality exhortations. This is the most useful claim in the [field report](https://standingquestions.com/blog/llms-shift-registers/) and the one that has held up best in our own use **[observed]**. The six prompts below are the reusable version. Full treatment: [`registers-habits-self-report.pdf`](registers-habits-self-report.pdf). Machine-readable taxonomy they target: [`taxonomy.json`](taxonomy.json).

## Why structure beats exhortation

**What does not move a register:** "think harder," "be more direct," "be more thoughtful," frustration without a structural correction. These get absorbed *into* the active register. A hedging model produces a more polished hedge; a defensive one produces a tidier caveat list; a brainstorming one produces a more elegant menu. The posture survives; the surface shifts to match the instruction **[inferred]**.

**What does move it:** constraints that remove a default output shape from the table rather than discouraging it. A length cap makes a caveat-heavy answer physically impossible past a point. "One recommendation, no menu" deletes the three-option shape from the output space. "No closing question" removes the abdication move. The constraint does not ask the model to resist its defaults; it makes the defaults inoperative. Telling a writer "be concise" addresses the goal; a word limit addresses the mechanism.

## The six patterns

Each is stated verbatim, with the default shape it removes and the register or cluster it targets.

### 1. Commit to one recommendation

```
Give one recommendation, not a menu. Defend it. State confidence. End on the recommendation, not a question.
```

Removes: the three-option shape and the closing-question abdication. Targets: collaborative-brainstorming; Cluster A (the thorough-feeling non-answer).

### 2. Cap the length

```
Answer in under 40 lines. No option menu unless multiple options are genuinely live; if you list options, pick the best one and say why.
```

Removes: length for its own sake and the reflexive menu. Targets: length-matching, structured-document ceremony (Cluster D). Length is also a register signal: committed answers tend to land in 20 to 40 lines; hedging balloons past 150.

### 3. Name the task first

```
Before acting, name the task: execution, diagnosis, synthesis, recommendation, or exploration. Then answer in that register.
```

Removes: the wrong-register default (for instance technical-executor overstaying into a moment that needed synthesis). Targets: register selection itself.

### 4. Do not agree first

```
If I push back, do not agree first. Check whether my objection is actually correct, then say explicitly: updating, rejecting, or partially accepting, and why.
```

Removes: the agreement cascade. Targets: the sycophantic register; Cluster B.

### 5. Confirm the frame before producing artifacts

```
Do not write or modify artifacts until you have confirmed the task frame. First report back what you think I asked for.
```

Removes: procedural-default-when-synthesis-is-needed, the executor doing the next visible step instead of occupying the reasoning posture the moment shifted to. Targets: technical-executor overreach.

### 6. Keep the epistemic tiers separate

```
Separate observed facts, inferences, and hypotheses. Do not upgrade an inference into a fact.
```

Removes: false precision and confidence the standing does not warrant. Targets: research-synthesizer; the push-confidence-to-model habits.

## Two operating heuristics

- **Length is a register signal.** A sudden ballooning response is a cue to redirect rather than read **[observed]**.
- **Drift accumulates within a session.** A fresh context resets it even without any other change, so for long analytical work an occasional clean restart can buy back quality no prompt will **[observed, consistent with our sessions]**.

## Scope

These are working heuristics from one team's naturalistic use across two model families, not a benchmarked method. If you operationalise them and they do not move output under the predicted conditions, that result is worth more than the report. [MIT](../LICENSE).
