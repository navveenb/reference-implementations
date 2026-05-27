# SCI for AI — Reference Implementations

This directory holds reference implementations of the
[GSF SCI for AI specification](https://sci-for-ai.greensoftware.foundation/),
which extends ISO/IEC 21031:2024 (the base Software Carbon Intensity
specification) with AI-specific considerations: functional units suited
to ML and generative workloads, treatment of inference vs training, and
distinction between provider and consumer measurement boundaries.

Each implementation here demonstrates one way to apply the SCI for AI
specification to a specific workload class. They are educational
starting points, not production systems or recommended toolchains.

## Available implementations

### Maintained by GSF (`gsf/`)

| Implementation | Workload class | Highlights |
|---|---|---|
| [llm-inference](./gsf/llm-inference/) | LLM inference workloads | End-to-end Python implementation with adapters for major LLM provider SDKs; uses instrumentation tools for measured per-call energy; reports carbon, energy, and cost side by side; ships committed fixtures replayable without an API key. |

### Maintained by the community (`community/`)

No community implementations have been contributed yet. Contributions
covering other workload classes — model training, computer vision,
recommender systems, batch inference — or alternative approaches to
workload classes already covered, are explicitly welcome.

## What can a SCI for AI reference implementation cover?

The SCI for AI specification applies across the breadth of AI
workloads. Implementations here can cover any of:

- **Inference workloads** at different scales (single-request, batch,
  streaming, agentic).
- **Training workloads** including pretraining, fine-tuning, and
  reinforcement-learning loops.
- **Specialised AI workloads** such as computer vision, recommender
  systems, speech, embeddings, retrieval-augmented generation.
- **Different deployment patterns** — hosted API, self-hosted
  inference, on-device inference, edge inference.

Multiple implementations of the same workload class taking different
approaches (different measurement provider, different functional unit
choice, different language) are welcome.

## Contributing

See the top-level [CONTRIBUTING.md](../../CONTRIBUTING.md) for the
contribution process. New community implementations go under
`community/`; contributions to `gsf/` are handled by the foundation
directly.
