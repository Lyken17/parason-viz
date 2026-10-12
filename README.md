# Parason: Subtask vs Trial Parallelism

Interactive visualization of the two kinds of parallel reasoning in
[Parason: Revealing Subtask- and Trial Parallelism in LLM Reasoning](https://arxiv.org/abs/2608.24658).

**Live page:** https://lyken17.github.io/parason-viz/

One problem uses both forms: find a^b + b^a, where a and b are the real roots of
x³ − 2x − 4 = 0 and x³ + x − 30 = 0.

- **Subtask parallelism (AND):** the two cubics are independent, and both roots are needed.
- **Trial parallelism (OR):** inside each subtask, five candidate roots are tested at once.
  One hits, and the dead ends stay in context.

The ablation replays the same trace four ways (sequential, subtask only, trial only, both)
and compares the token latency along the critical path. Token counts are illustrative.

The page is a single static `index.html` with no build step.
