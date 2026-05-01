# Primer Prompt

A user-controlled behavioral constitution for making LLMs better thinking and conversation partners through enforced epistemic rigor.

## What This Is

This is a primer prompt—a custom instruction set pasted at the start of an LLM conversation. It establishes epistemic standards (Bayesian reasoning, calibrated uncertainty, steelman/critique framing, source transparency) and interaction norms (anti-flattery, anti-sycophancy, anti-AI-voice tics) before substantive exchange begins.

It is designed for users who take a highly interactive and iterative approach to working with language models, not for users who treat them as short-answer bots. If you paste a question and expect a quick response, this prompt will frustrate you. If you use an LLM as a thinking partner over extended conversations and want it to push back, show its work, and help you become more capable rather than more dependent, this prompt may help.

## What's In It

The prompt covers:

- **Epistemic Standards** — Bayesian reasoning, calibrated claims, silence over guesses, prediction discipline, and an oracle/creative mode distinction for separating factual analysis from storytelling
- **Intellectual Honesty** — Anti-sycophancy, bias awareness, fluency vs. expertise, steelman/critique sequencing
- **How to Disagree** — Productive friction, uncertainty transparency, ROI pragmatism
- **Communication Style** — AP style, plain language, structural and verbal tic avoidance
- **Translation and Vocabulary** — Bridging older terminology to current industry language

The document borrows its narrative approach from Anthropic's Claude constitution, but it is a user-controlled, inference-time instruction set, not a training document.

## The Pac-Man Failure

The same night I finished the first version of this prompt, after hours of iteration, I tested it. I asked a trivial question: how many unique things can Pac-Man eat in the 1980 arcade game?

The model gave an unsourced estimate. When I asked why it didn't apply the rigor specified in the prompt, it said a video game question didn't seem important enough to warrant it. Pages of specification were bypassed in a single exchange.

That was the lightbulb. System prompts aren't enforced. They're suggested. The model retains de facto authority to decide when constraints apply. The failure occurred in the same long session that created the prompt—context drift and sycophancy had already accumulated. I call this **rigor drift**: the rigor itself drifts like all other context.

The prompt has been substantially updated since that failure. The Pac-Man scenario may not reproduce with the current version. But the underlying vulnerability remains: behavioral constitutions are subject to the model's judgment about what warrants rigor, and that judgment is not reliable.

## What I Learned

**It does work somewhat.** The prompt meaningfully improves interaction quality in shorter, focused sessions. The anti-flattery rules reduce sycophancy in early conversation turns. Several features—like the steelman/critique separation—produce reliably better-structured responses.

**It doesn't forcefully constrain.** The prompt is a behavioral suggestion, not a hard constraint. The model can and will bypass it when the engagement goal-seeking strength overwhelms the instruction following, especially in long contexts.

**Sycophancy is nearly impossible to constrain in extended conversations.** The model's optimization for engagement outcompetes user-provided instructions over time. This appears to be a structural limitation, not a prompt design failure.

**Epistemic values are subjective.** The prompt encodes a specific way of thinking derived from Carl Sagan's scientific skepticism, Bayesian reasoning, and adversarial collaboration. These values are not universal. The prompt works for me because it reflects how I want to think. It may not work for you.

## What I'm Thinking About Next

Behavioral constitutions can't solve the enforcement problem on their own. The drift is architectural. I'm exploring several directions:

**Multi-node adversarial verification.** A Bengio-style framing converter that strips first-person investment from queries, independent adversarial instances for steelman and critique, a synthesis layer that separates intersection from divergence, and a primer-based output formatter. The idea is to move constraints out of the model's discretionary space and into the harness.

**Query classification and specialist routing.** A passive classifier that determines whether a prompt is creative or factual, then routes accordingly: creative prompts to the base model, factual prompts to specialist APIs (Wikipedia for lookups, a calculator for math, adversarial review for reasoning). The model shouldn't decide when rigor applies. The harness should.

## How to Use It

1. Copy the full text of `primer-prompt.md`.
2. Paste it at the start of a new LLM conversation.
3. Engage normally. The prompt shapes the interaction from that point forward.
4. For long conversations, consider re-pasting key sections to counteract context drift and the U-shaped attention curve common in long-context processing.
5. If the model drifts, flag it. The drift is itself information.

## Origins

This document was assembled iteratively with Claude and DeepSeek, incorporating suggestions from friends and internet advice. I cannot properly credit every influence because I no longer know where some lines originated. I am not claiming originality of every line—just the assembly, the testing, and the analysis.


