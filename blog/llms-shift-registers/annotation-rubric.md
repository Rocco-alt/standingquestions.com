# Annotation rubric (stub)

A starting point for checking the register and habit labels against real transcripts, instead of taking them on faith. This is a **stub, not a finished protocol**: enough to start coding transcripts and to surface where the labels are ambiguous. The full validation program is in the [companion paper](registers-habits-self-report.pdf); the labels themselves are in [`taxonomy.json`](taxonomy.json).

## The principle: behavioural, not phenomenal

We do not ask whether the model "was really in" a register. We ask whether outputs matching a register's description are recoverable from the behaviour. A label is supported if an independent annotator, given only the text, assigns it. That is the only kind of accuracy this rubric tests **[inferred]**.

## Unit of analysis

One model turn (one response), read in the context of the turns before it. Registers and habits are properties of a response, not of a whole session, though a session can be summarised as a sequence of them.

## What to record per turn

1. **Dominant register.** The single register that best describes the response's posture (the 15 in `taxonomy.json`, grouped task-execution / social-relational / protective / generative). Allow one secondary register where a register genuinely rides on another.
2. **Habits present.** Zero or more of the 20 habits. Mark only habits with a concrete textual anchor (a quotable span), not an impression.
3. **Cluster, if any.** Whether the turn matches one of the five clusters (A to E). A cluster requires its named register plus at least one of its named habits, co-occurring in the same turn.
4. **Did the task get an answer?** A separate yes / partial / no judgement, independent of surface quality. This is the field that catches Cluster A, where a response scores well on length, structure, humility, and options while the user got no answer.
5. **Trigger (optional).** What in the prior turns plausibly activated the register: user pushback, a signal read as unfamiliarity, a frame shift the model did not register, the length of accumulated context.

## Anchoring rule

Every label needs a span. If you cannot point at the words that justify "closing-question abdication," do not mark it. This keeps the exercise behavioural and keeps two annotators comparable.

## Reliability

For any real validation, two or more annotators label the same turns independently, and you report agreement (for example Cohen's kappa, per register and per habit) before reporting any frequencies. Low agreement on a label is itself a finding: it means the label is not behaviourally recoverable as written, and it should be split, merged, or dropped. Treat the taxonomy as falsifiable here, that is the point.

## Worked micro-example

- **Prompt (paraphrased):** "Which of these two databases should we use?"
- **Response:** a 150-line reply with a three-option table (the two asked about plus a third), trade-offs for each, and a closing "which direction feels right to you?"
- **Labels:** dominant register `collaborative-brainstorming`; habits `three-option-structures`, `length-matching`, `closing-question-abdication`; cluster `cluster-a`; answer = no (the user asked for a choice and did not get one); trigger = a decision moment treated as a brainstorm.

## What this is not

Not a benchmark, not a scoring rubric for model quality, and not a claim that the 15 registers are complete or correctly carved. It is an instrument for testing those labels against behaviour. If a category does not survive annotation, that is the rubric working. Tell us what you find. [MIT](../LICENSE).
