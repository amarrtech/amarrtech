<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/amarrtech/amarrtech/main/assets/banner-dark.svg">
  <img alt="Amar — Reliable inference. Observable systems. Measurable outcomes." src="https://raw.githubusercontent.com/amarrtech/amarrtech/main/assets/banner-light.svg" width="100%">
</picture>

**Software Engineer at Google · AI Infrastructure**

I build tools for understanding how AI systems behave under load—and what happens when they fail. My focus is the production layer around models: inference serving, request routing, observability, and reliability.

My foundation is network and infrastructure engineering: routing, load balancing, traffic engineering, and operational debugging. I bring that perspective to LLM systems, where a successful HTTP response can still hide a slow first token, a stalled stream, or an ineffective fallback.

## Selected projects

### [Inference Triage](https://github.com/amarrtech/inference-triage)
**From latency symptoms to an evidence-backed incident report.**

An investigation agent that combines serving telemetry, ranked hypotheses, diagnostic experiments, and explicit uncertainty. Includes Google ADK tools, read-only vLLM metrics collection, persistent investigation history, and a dashboard. A seeded simulator makes incident scenarios reproducible without a GPU.

*Engineering focus: diagnostic reasoning, telemetry contracts, and controlled comparisons. Simulator validation is distinct from live GPU-backed serving validation.*

### [LLM SLO Checker](https://github.com/amarrtech/llm-slo-checker)
**Turn streaming behavior into an operational verdict.**

Checks streaming endpoint behavior against configured service-level objectives, including time to first token and request outcomes. Produces PASS, FAIL, or INCONCLUSIVE verdicts for CI workflows, keeping insufficient evidence separate from a healthy result.

*Engineering focus: meaningful reliability checks, configurable thresholds, and actionable failure reporting.*

### [LLM Serving Systems Lab](https://github.com/amarrtech/llm-serving-systems-lab)
**Explore the mechanisms behind serving performance.**

A reproducible lab for scheduling, batching, KV-cache pressure, and the relationship between throughput and useful work delivered within latency targets. Pairs GPU-free simulations with a vLLM Colab companion for experiments against a real serving engine.

*Engineering focus: workload design and performance trade-offs. Simulated results and measured serving results are kept distinct.*

### [Reliable LLM Gateway Lab](https://github.com/amarrtech/reliable-llm-gateway-lab)
**Make failure handling observable and testable.**

A gateway sandbox for retries, deadlines, fallback routing, circuit breakers, and rate limiting. Mock services, load tests, and Prometheus metrics make it possible to examine how resilience controls interact under failure.

*Engineering focus: bounded failure handling and overload behavior. The lab uses simulated services rather than production model traffic.*

## Open-source contributions

I contribute fixes and tests to the systems around inference. A few examples:

**Merged**

- [LiteLLM #43959](https://github.com/BerriAI/litellm/pull/43959) — Resume synchronous streaming fallbacks without retrying the primary deployment.
- [Agent Router #2299](https://github.com/theagentrouter/agent-router/pull/2299) — Add OpenRouter real-provider data-plane test coverage.

**Under review** · status checked October 17, 2026

- [vLLM #59439](https://github.com/vllm-project/vllm/pull/59439) — Propagate SIGTERM during engine startup.
- [Triton Server #8987](https://github.com/triton-inference-server/server/pull/8987) — Preserve gRPC trace metadata length.
- [OpenTelemetry #640](https://github.com/open-telemetry/opentelemetry-python-genai/pull/640) — Improve LangChain token-usage fallbacks.

## What I’m exploring

Streaming latency · batching and KV-cache behavior · routing and fallbacks · overload protection · tracing and SLOs

For a smaller monitoring tool, see [LLM SLO Probe](https://github.com/amarrtech/llm-slo-probe): black-box streaming measurements and Prometheus textfile output.

I welcome technical discussion through issues and pull requests on these repositories—especially reproducible failures, measurement design, and serving reliability.
