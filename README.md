# Petru Arakiss

**AI Engineering Lead. Staff/Principal AI product infrastructure: retrieval, agent runtimes, evals, observability, guardrails, and operator workflows.**

I work on the engineering around language models: retrieval systems, agent and workflow runtimes, guardrails, eval loops, traces, permissions, cost and latency controls, and the product screens that make failures visible.

Professional software work since 2006. Machine learning since 2015. Current work is inside regulated finance, so public detail has a boundary: I can name the systems and the engineering shape, but not expose private implementation details.

At Atlax360 I entered through product-platform ownership in 2021, then added a dedicated AI Engineering Lead mandate in Jan 2024. The AI work is now the primary current signal. The earlier platform role still matters because it is the foundation behind the operator screens, review paths, component systems, and workflow UX around those AI systems.

The strongest public proof is the recent Rust work. It shows how I think about agent infrastructure when the code is visible: deterministic guardrails, tamper-evident memory, append-only traces, local-first tooling, eval harnesses, and systems that fail in inspectable ways.

Most AI systems do not fail only on model quality. They fail on weak context boundaries, vague orchestration, missing evals, hidden cost, unclear permissions, and no owner when the model is wrong.

## Current private production context

I lead AI engineering across three systems at Atlax360, alongside an ongoing product-platform mandate. The implementations are private. The architecture class is public.

**BIFROST.** Document intelligence and retrieval for financial documents: ingestion quality gates, semantic and visual chunking, pgvector/HNSW search, caching, source-quality scoring, analytics, and explicit no-answer behavior when evidence is weak.

`Python` · `FastAPI` · `PostgreSQL` · `pgvector` · `Docling` · `PyTorch` · `Transformers`

**ORVIAN.** Multi-tenant AI workflow runtime for B2B operations: protected APIs, context assembly, durable memory, deterministic/cached/full-LLM execution tiers, run events, idempotency, queue processing, and human-review metadata when automation should stop.

`TypeScript` · `Hono` · `PostgreSQL` · `Drizzle` · `Supabase` · `queues`

**Polaris.** Internal AI assistant integrating BIFROST retrieval with MONARCH guardrails, cached safety-to-retrieval handoff, citations, streaming UX, query analytics, and suggestion revalidation.

`Next.js` · `Vercel AI SDK` · `BIFROST` · `MONARCH` · `Drizzle` · `PostgreSQL`

## Selected public work

These repos are not a complete production system. They are public pieces of the way I think about agentic engineering, observability, local tooling, and developer environments. The recent Rust repos are the clearest signal.

**Agent harness and governance**

- **[gommage](https://github.com/Arakiss/gommage)** (Rust): policy-as-code permission harness for AI coding agents. Deterministic allow, deny, and ask decisions with audit evidence.
- **[nahuali](https://github.com/Arakiss/nahuali)** (Rust): self-inspecting memory for AI agents. Evidence, provenance, health signals, and an optional Ed25519-signed tamper-evident ledger.
- **[slod](https://github.com/Arakiss/slod)** (Rust, formerly traceframe): local-first trace recorder for AI agent workflows. Append-only run evidence, hook ingestion, ledger indexing, reports, and CI gates.
- **[greco](https://github.com/Arakiss/greco)** (Rust): research harness for typed, layered, reversible coding-agent harness changes under operator-owned evals and budgets.

**Observability and local systems**

- **[vestig](https://github.com/Arakiss/vestig)** (TypeScript): runtime-agnostic structured logging with context propagation, observability primitives, and automatic PII sanitization.
- **[eldr](https://github.com/Arakiss/eldr)** (Rust): zero-dependency Apple Silicon hardware monitor and thermal watchdog: CPU/GPU/ANE power, per-core load, temperatures, fans, and battery without sudo.

**Developer environment**

- **[ghostty-warp](https://github.com/Arakiss/ghostty-warp)** (Shell): Ghostty terminal environment for Linux: themes, presets, fonts, tmux integration, and a config switcher for a Warp-like workflow.

## How I think about AI systems

I prefer systems whose behavior can be inspected. Retrieval should show its evidence. Agents should expose state and stopping conditions. Guardrails should be explicit. Cost and latency should be visible. Human review should be designed into the path, not patched on after a failure.

The useful public claim is simple: if a repo, source, trace, test, or product constraint supports a statement, link it. If the work is private, say where the public boundary is.

## Open to

Staff Software Engineer, Principal Software Engineer, AI Infrastructure, Product Infrastructure, Applied AI, Architect, and Forward Deployed roles where production AI is the core product work.

Madrid. Remote-first across the EU.

[petruarakiss.com](https://www.petruarakiss.com) · [LinkedIn](https://www.linkedin.com/in/petruarakiss/) · [GitHub](https://github.com/Arakiss) · [petruarakiss@gmail.com](mailto:petruarakiss@gmail.com)
