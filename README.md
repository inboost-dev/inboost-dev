# InBoost Technologies

InBoost builds developer tooling and local runtimes for coding assistants such as Claude Code, Cursor, and OpenHands. The tools handle structural code search, AST validation, traceback trimming, and inference routing on the local machine before patches are applied.

[Website](https://inboost.pro) • [GitHub Issue Demo](https://agent-demo.inboost.pro) • [Documentation](https://inboost-dev.github.io/inboost-longrun)

---

## Projects

* [`inboost-ai-longrun-runtime`](https://github.com/inboost-dev/inboost-ai-longrun-runtime): Local runtime and MCP server that handles AST indexing, traceback compression, and step verification for coding assistants. Available on NPM as `@inboost-pro/inboost-longrun`.
* [`agent-tool-parser`](https://github.com/inboost-dev/agent-tool-parser): Dual-engine parser in Rust and Python for tool calls and streaming JSON repair. Available on PyPI as `agent-tool-parser` and Crates.io as `agent-tool-parser-core`.
* [`inboost-ai-proxy-runtime`](https://github.com/inboost-dev/inboost-ai-proxy-runtime): Local inference proxy with prompt cache alignment and fallback routing across local and hosted models.

---

## Evaluation

On the full SWE-bench Verified benchmark (500 tasks, Docker evaluation harness), the LongRun runtime resolved 451 out of 500 tasks (90.20%) using MiniMax-M3, with zero 0-byte patches. Detailed evaluation logs and Docker reproduction steps are published in the [benchmark directory](https://github.com/inboost-dev/inboost-ai-longrun-runtime/tree/main/benchmarks).

---

## Quick start

Install the CLI and MCP server using npm:

```bash
npm install -g @inboost-pro/inboost-longrun
```

Or run directly without installation:

```bash
npx @inboost-pro/inboost-longrun --help
```

For Python environments, install the tool parser:

```bash
pip install agent-tool-parser
```
