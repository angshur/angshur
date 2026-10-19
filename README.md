# Angshuman Rudra

Product leader for data and AI platforms. Former backend and data engineer (Adobe, Yahoo). MBA, Cornell.

**What I work on:** making AI agents trustworthy on real business data. That comes down to three questions: is the number right, is the agent allowed to do this, and does it still hold when many agents run at once. Each repo below takes one of them, ships with an eval, and lists what it does not prove.

## Start here: one definition, every surface
**[measurement-md](https://github.com/angshur/measurement-md)** defines each business metric once, in a plain file, and serves that definition to every place a number gets produced:

| Surface | What it does |
|---|---|
| MCP server | Claude, ChatGPT and other agents look up the governed definition before they write SQL |
| Query gate | Refuses an agent's query that breaks a definition and names the clause (62 of 62 planted mistakes caught) |
| CLI | `lint`, `explain`, `check`, `export` from a terminal or CI |
| Snowflake | Compiles to a semantic view YAML for Cortex Analyst: aliases become synonyms, anti-patterns become SQL-generation rules |

## The three questions

| Question | Repo | Evidence |
|---|---|---|
| **Is the number right?** | [measurement-md](https://github.com/angshur/measurement-md) | Linter: 360 of 360 planted defects. Gate: 117 of 117 correct requests allowed |
| | [data-layer-interop-checker](https://github.com/angshur/data-layer-interop-checker) | Finds broken joins in a marketing data stack: 100% planted-defect detection, 0 false alarms |
| **Is the agent allowed to do this?** | [warrant](https://github.com/angshur/warrant) | Scoped, revocable authority for agents: 16 of 16 attacks denied for the expected reason |
| | [agent-ledger](https://github.com/angshur/agent-ledger) | An audit trail of what an agent did and on whose authority |
| **Does it hold at scale?** | [quorum](https://github.com/angshur/quorum) | Four agents, no faults, 384 lost updates. With the runtime fixes: 0 |
| **Is the platform ready for agents?** | [agent-readiness-scanner](https://github.com/angshur/agent-readiness-scanner) | Scores a platform on APIs, permissions and docs, with a calibration eval |
| **Did the change help?** | [prompt-bench-cli](https://github.com/angshur/prompt-bench-cli) | Golden-set harness with paired statistical comparison and a regression gate |

## How I build
- **Eval first.** Every repo has planted defects and clean controls. A clean control that fails means the harness is wrong, not the code.
- **Limits in the README.** Synthetic data says so. Untested assumptions say so.
- **Standard library only** where possible, so anyone can run it in a minute.

These are independent projects on synthetic data. · [LinkedIn](https://www.linkedin.com/in/angshumanrudra)
