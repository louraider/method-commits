# method-commits

Append-only daily hash commitments for the **Investor24 · Аналізатор** method portfolio.

On each weekday trading session, an automated job commits a canonical snapshot of the
method's **public BUY verdict-set + open positions + method version** (NOT NAV, NOT alpha)
together with its SHA-256 hash.

## What this proves — and what it does NOT

- **Proves:** the verdict-set published on a given date has not been altered since
  (third-party-timestamped, append-only Git history).
- **Does NOT prove:** that the method has predictive edge. It does not. This is a
  transparency / integrity record — evidence that a published verdict is not changed
  after the fact — not proof of alpha.

The chain is intentionally **sparse**: weekdays with a NAV row only. Weekend / holiday /
no-session gaps are expected, not breaks.

- Live record: https://investor24-analyst.vercel.app/uk/method-portfolio
- Pre-registered rule: https://investor24-analyst.vercel.app/uk/method-portfolio/rule