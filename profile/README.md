<div align="center">

<img src="https://raw.githubusercontent.com/plurai-ai/.github/refs/heads/main/static/banner.png" alt="Plurai" />

# Plurai

**The recursive self-improvement layer for AI agents.**

Agentic world simulation and model post-training that continuously optimize intelligence and cost.

[Website](https://www.plurai.ai/) · [Docs](https://docs.plurai.ai/) · [Start free](https://simulation.plurai.ai/connect) · [Discord](https://discord.gg/bg34gh76uJ) · [LinkedIn](https://www.linkedin.com/company/plurai/) · [X](https://x.com/pluraiAI)

</div>

---

## Trust is a loop, not a launch

**Simulate → fix → post-train → repeat.**

- **[Plurai Simulation](https://www.plurai.ai/simulation)** finds where your agent breaks, and fixes it. It builds a digital twin of your agent in a sandboxed world of synthetic personas, synthetic documents and mocked services. Then it generates scenarios and evals, runs them, and traces every gap back to a code-level fix. It runs interactively from your coding agent, or headless.
- **[Post-training](https://www.plurai.ai/post-training)** turns an open-source model into a specialized model you own, at a fraction of frontier inference cost.

## Get started with Plurai Simulation

Install the plugin into your coding agent from the repo of the agent you want to test.

**Claude Code**

```text
/plugin marketplace add plurai-ai/plurai-plugins
/plugin install plurai-simulation@plurai-plugins
```

Restart Claude Code, then run `/simulate <path-to-your-agent>`.

**GitHub Copilot CLI**

```bash
copilot plugin marketplace add plurai-ai/plurai-plugins
copilot plugin install plurai-simulation@plurai-plugins
```

Then run `/plurai-simulation:simulate <path-to-your-agent>`.

**Codex CLI**

```bash
codex plugin marketplace add plurai-ai/plurai-plugins
codex plugin add plurai-simulation@plurai-plugins
```

Then run `$simulate <path-to-your-agent>`. See the [quickstart](https://docs.plurai.ai/quickstart) for the Codex config this needs.

### How it works

| Stage | What happens |
| --- | --- |
| **Wire** | Plurai reads your agent as built, maps its knowledge bases, and decides what stays live and what gets mocked. |
| **Suite** | It generates scenarios and auto-evals for your domain, including hard personas that push back, and weights them by real traffic. |
| **Run** | Each run is sandboxed and resets to the same state. Every scenario plays three times to separate real failures from flaky ones. |
| **Fixes** | Each gap is traced to a file and line with a proposed fix, ranked by severity. `/simulation-fixes --verify` re-checks it. |

Plurai Simulation works with LangGraph, LangChain, CrewAI, Claude Agent SDK, OpenAI Agents SDK, Google ADK, LlamaIndex, Strands Agents, Mastra and Vercel AI SDK. It can ground scenarios in production traces from LangSmith, Langfuse, Arize and Braintrust.

## Open source

| Repository | Description |
| --- | --- |
| [**intellagent**](https://github.com/plurai-ai/intellagent) | A framework for diagnosing and optimizing agents with simulated, realistic synthetic interactions. ([paper](https://arxiv.org/abs/2501.11067)) |
| [**plurai-plugins**](https://github.com/plurai-ai/plurai-plugins) | Plugin marketplace for Claude Code, Copilot CLI and Codex CLI, including `plurai-simulation`. |
| [**plurai-simulation-sdk**](https://github.com/plurai-ai/plurai-simulation-sdk) | Python SDK for Plurai agent simulation. |
| [**plurai-simulation**](https://github.com/plurai-ai/plurai-simulation) | The Plurai Simulation plugin for Claude Code. |
| [**plurai-mockenv**](https://github.com/plurai-ai/plurai-mockenv) | The mock engine behind Plurai Simulation. It serves the mocked tools your agent calls and keeps each session's world state. `pip install plurai-mockenv` |
| [**plurai-extract**](https://github.com/plurai-ai/plurai-extract) | Deterministic extraction of documents and records from your data sources, run locally with your own credentials. `pip install plurai-extract` |

> `plurai-simulation`, `plurai-simulation-sdk`, `plurai-mockenv` and `plurai-extract` are read-only mirrors. Please open issues, not pull requests.

## Research

We are AI researchers with a decade of background in autonomous driving, where you don't ship until you've simulated. Read our work at [plurai.ai/papers](https://www.plurai.ai/papers) and on the [blog](https://www.plurai.ai/blog).

## Get in touch

- Questions or bugs: open an issue on the relevant repo, join our [Discord](https://discord.gg/bg34gh76uJ), or email [support@plurai.ai](mailto:support@plurai.ai).
- Talk to us: [book a demo](https://www.plurai.ai/book-a-demo).
- Join us: [careers](https://www.plurai.ai/careers).
