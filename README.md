# P1vs — Builderr Trading Round 2

Entrant: P1vs · Contact: Immutable1407@gmail.com

## Run

Install `requirements.txt` (`numpy==2.2.6`). The entry point is `decide(market_state, portfolio_state, cash)` in `agent.py`. It uses supplied historical bars and the real portfolio/cash only. No network calls, credentials, external data files or trained weight files are required. Python standard-library modules and NumPy are the only runtime dependencies.

The agent combines fixed four-stock expert baskets over the supplied stock universe, observed price/trend feedback, bounded exposure and sale-funded orders. When already invested it uses the R3 account-consistent policy. On an empty account R13 chooses among the original fixed expert set using historical paired medians subject to risk and continuation compatibility. Source modules are embedded as readable literal Python source, instantiated with standard-library `ModuleType`; their function/class ASTs are unchanged. `source_manifest.json` records module lineage and hashes. Original MIT attribution and LICENSE are retained.

## Checks and limits

The exact bundled agent passed the official public selfcheck, all four public sample safety checks, isolated/reloaded order equivalence, and the pinned actual public runner's daily requested orders, positions, cash and equity comparison on four <=2021 phase/cost paths (8,056 decisions, zero errors; equity difference under $0.0051 due to public cent rounding). This is local engineering verification, not an organizer installation acknowledgement.

A frozen competition comparison used fresh-cash nonoverlapping 15-session windows, with 16-session sensitivity, development 2006–2015 and validation 2016–2021, at 5/20bps. R13 was selected by the pre-registered worst-phase median excess criterion over the original submitted baseline. R3 performed better on the validation-only comparison. Prior strategy selection, survivor-universe bias and repeated use of historical data limit inference. Research cash-entry qualification failed and independent historical qualification has not been established. No future-return or competition-rank guarantee is claimed.

The original submitted baseline is retained in Git commit `3167218a7f4e317bc954d56918d9c4eb78eb6974`. `preview.py` and `selfcheck.py` are unchanged official public tools; their sample results do not constitute live scored results.
