# Angshuman Rudra

Product leader for data and AI platforms. Former backend and data engineer (Adobe, Yahoo). MBA, Cornell.

I build small, tested tools to work through ideas about AI agents: what they're allowed to do, whether the numbers they report are right, and what breaks when many of them run at once. Each project has an eval with a results table and a plain list of what it does not prove.

### Trust and authority for agents
- **[warrant](https://github.com/angshur/warrant)**: permission tokens for agents acting on a person's behalf (spend limits, scoped accounts, expiry, delegation to sub-agents, revocation). 16 of 16 attacks denied for the expected reason; 0 violations across 10,000 random delegation chains.
- **[agent-ledger](https://github.com/angshur/agent-ledger)**: an audit trail of what an agent did, on whose authority, with what result.

### Correct numbers from agents
- **[measurement-md](https://github.com/angshur/measurement-md)**: a spec for metric definitions, a 12-rule linter, and a query gate that refuses an agent's query when it breaks a definition. 62 of 62 planted mistakes refused with the exact rule.
- **[data-layer-interop-checker](https://github.com/angshur/data-layer-interop-checker)**: finds broken connections in a marketing data stack. 100% planted-defect detection, 0 false alarms.

### Reliability of agent fleets
- **[quorum](https://github.com/angshur/quorum)**: a chaos harness that breaks a simulated agent fleet, and the runtime fixes (idempotency, checkpoints, compare-and-set, dead-letter queues) that take duplicates, lost updates and silent drops to zero.

### Readiness and evaluation
- **[agent-readiness-scanner](https://github.com/angshur/agent-readiness-scanner)**: scores how ready a marketing platform is for AI agents, with a calibration eval.
- **[prompt-bench-cli](https://github.com/angshur/prompt-bench-cli)**: a golden-set harness for prompt and model changes, with paired statistical comparison and a regression gate.

These are independent projects on synthetic data.

[LinkedIn](https://www.linkedin.com/in/angshumanrudra)
