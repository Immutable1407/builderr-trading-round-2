# P1vs — Builderr Trading Round 2

Initial entry by P1vs for https://builderr.ai/trading-v0.

## Strategy

This entry uses the official MIT-licensed `baseline.py`, copied unchanged to
`agent.py`. It buys SPY, QQQ, XLK and XLV at approximately 25% each and then holds.
It uses only the supplied bars, requires no network or credentials, and has no
third-party Python dependencies. This is a baseline entry, not an original
strategy or a claim of competitive performance.

Upstream: https://github.com/builderr-ai/builderr-trading-template

Source commit: `f7461da1f6ed4b76c73d87166ec4d79b6e592ae7`

The official preview, smoke test and public sample data are included unchanged.
The upstream MIT license is preserved in LICENSE.

## Run locally

```sh
python3 preview.py
python3 selfcheck.py
```

Local validation on 2026-10-15 passed all preview safety checks and the smoke test.
Peak gross exposure: 1.00x; peak concentration: 27%; worst sample drawdown: 29.9%.
These are public sample checks, not official admission or live ranking results.
Official admission is determined by Builderr's hidden validation.

Entry point: `decide(market_state, portfolio_state, cash)` in `agent.py`.
