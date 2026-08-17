# Trading Journal — Jameel Shaikh

Public summary of personal trading activity across NSE F&O, Currency F&O, MCX Commodity, and Equity. It separates lifetime broker-account reconciliation from historical public-series calculations that are reproducible from this repository but are not an authoritative continuous net-performance series.

**Live dashboards:** https://jams411.github.io/trading-journal/

## Canonical evidence status

Three distinct, non-interchangeable lifetime accounting figures are reported, each with a precise definition:

| Definition | Value | Meaning |
|---|---:|---|
| Gross Trading P&L | ₹9,98,843.30 | Before any brokerage or statutory trading charge |
| Trading Net P&L | ₹6,96,036.76 | After brokerage and statutory/exchange trading charges only |
| **Broker-account adjusted lifetime net P&L** | **₹6,87,291.37** | After trading charges **and** legitimate non-trading account debits at both brokers (AMC, DP charges, pledge/unpledge charges, and similar account-maintenance items) |

**The headline figure is ₹6,87,291.37** (displayed publicly as ₹6,87,291). This corrects the previously published ₹6,90,051.39: the prior figure netted out only Zerodha's non-trading account debits (₹5,985.37). A subsequent audit found an equivalent, previously-omitted category on the Angel One side — ₹2,760.02 in DP charges, account-maintenance charges, pledge/unpledge charges, and one subscription purchase, all sourced from the Angel One broking ledger — which had not been deducted. Applying the same accounting treatment to both brokers reduces the lifetime adjusted net by ₹2,760.02, to ₹6,87,291.37. This is a broker-account non-trading debit correction, not a change to any trade's recorded P&L.

The public 25-observation series mixes Angel One net P&L with Zerodha gross P&L, does not allocate all Zerodha charges by month, cannot date Angel One's full controlling population, and omits April 2025. Its return, benchmark, risk, and drawdown outputs are therefore historical public-series calculations—not canonical verified performance metrics. See "Historical public-series calculations" below; this treatment is unchanged and remains correct as currently disclosed.

## Record-count grain

Record counts use several distinct, non-interchangeable grains. They are never combined into one "trade count."

| Scope | Count | Source composition |
|---|---:|---|
| F&O realized-record entries | **4,523** | 4,292 Zerodha F&O tax-exit rows (FIFO-matched closed lots) + 231 Angel One F&O FIFO closes |
| Available realized-record entries | **5,284+** | 5,053 Zerodha tax-exit rows + 231 Angel One F&O FIFO closes |

**On the 231 figure:** this is the exact row count of Angel One's "Trading Insights" dated F&O export — a FIFO-matched, entry/exit-dated closed-trade subset that is structurally distinct from Angel's controlling P&L aggregate (which has no realization dates at all). It is intentionally narrower than Angel's full F&O record population and is retained specifically because it is the only dated Angel F&O subset available; it should not be read as "total Angel F&O trades," which is a different, undated, broker-aggregate figure not published here at record-count grain.

## Segment attribution

Directly charge-adjusted net P&L by segment (both brokers combined):

| Segment | Net P&L | Note |
|---|---:|---|
| Index Options | **+₹7,43,483.16** | Dominant profit engine — 106.8% of Trading Net P&L; every other segment combined was a net drag |
| Equity Options | +₹6,470.06 | |
| Cash-Equity Delivery | +₹82,401.24 | |
| Cash-Equity Intraday | −₹757.92 | |
| Currency F&O | −₹49,333.90 | Futures −₹31,497.36 · Options ≈ −₹17,836.54 |
| Commodity/MCX | −₹82,163.13 | Futures −₹61,947.25 · Options ≈ −₹20,215.88 |

Currency F&O and MCX Commodity activity was discontinued after underperformance in those segments. **Futures activity note:** no index or equity futures were traded on either broker (all index/stock derivatives activity is options); currency and commodity futures did occur, totaling −₹93,444.61 net combined.

## Strategy evidence

- Broker records support substantial NIFTY and BankNifty options/derivatives activity, with index options the dominant contributor to net P&L.
- Trading-process context includes options Greeks, implied volatility, open-interest analysis, position sizing, and structured trade review; these are not metrics reconstructed from the public series.
- Multi-leg options activity is directly evidenced only within a narrow ~2.5-month Angel One execution window: 46 of 49 trading sessions in that window contained 2 or more distinct option contracts, and 28 of those 46 contained both a net-long and a net-short leg simultaneously. This does not establish multi-leg prevalence across the account's full history, which is outside that window.
- Short-premium orientation is **not verified**, and neither is long-premium orientation — the available direction-flagged execution data shows a near-even buy/sell split. A superficially direction-like label on some Angel One contract records is confirmed **not** to be a reliable buy/sell indicator and was not used as evidence either way.

## Dashboards

| Dashboard | Description |
|---|---|
| [Overall Portfolio](combined.html) | Historical 25-observation public series, benchmark comparison, and reproducible calculations—with noncanonical status disclosed |
| [Zerodha](zerodha.html) | Broker-specific summaries based on Zerodha tax-P&L rows and fiscal charge controls |
| [Angel One](angelone.html) | Broker-specific summaries; complete controlling aggregates lack realization dates |

## Historical public-series calculations

The repository still reproduces the following outputs from its embedded 25 selected observations so prior public analysis remains inspectable. None is an authoritative combined net-performance claim:

| Historical calculation | Output | Status |
|---|---:|---|
| Portfolio return | +39.48% | Noncanonical mixed-basis selected series |
| Nifty 50 return | +23.02% | Noncontinuous selected-month chain |
| Difference | +16.46 percentage points | Noncanonical comparison |
| Profit factor | 2.05 | Noncanonical mixed-basis calculation |
| Sharpe ratio | 0.42 | Noncanonical mixed-basis calculation |
| Calmar ratio | 0.75 | Noncanonical mixed-basis calculation |
| Maximum drawdown | −31.48% | Noncanonical synthetic-series calculation |

**16 of 25 selected public-series observations were positive.** This is not a continuous monthly hit rate or a canonical portfolio-performance statistic.

**On the −31.48% maximum drawdown above:** this is a return-based drawdown computed on the synthetic 25-observation equity curve and is unrelated to the canonical absolute-rupee drawdown below. A separate, canonical **absolute P&L drawdown of −₹7,10,690.85** occurred in Zerodha's derivatives (F&O) activity, computed on the daily-aggregated realized net P&L curve (trough dated 2025-01-06). It is a rupee peak-to-trough figure, not a percentage, and is not interchangeable with the −31.48% historical series figure above.

## Methodology and provenance

- **Public repository:** Provides summarized/analyzed trading data and reproduces the historical public-series calculations where applicable.
- **Private verification evidence:** Broker statements, tax-P&L reports, and trading exports were used to verify and reconcile the canonical record. Raw brokerage files are not published.
- **Reproducibility boundary:** A visitor can reproduce calculations from the embedded public arrays, but cannot reconstruct the complete broker record or a continuous combined monthly net series from this repository.
- **Accounting boundary:** Broker accounting bases and charge availability differ across sources; the private reconciliation controls canonical accounting definitions. Trading Net P&L, Broker-Account Adjusted Net P&L, and Gross Trading P&L are kept as three distinct, separately labeled figures throughout this repository and are never used interchangeably.
- **Date boundary:** The full Angel One controlling population does not contain realization dates, so no authoritative combined monthly series is currently available.
- **Record-count boundary:** Zerodha tax-exit rows, Angel One dated FIFO closes, and any other record count are reported at their own grain and are never summed into a single "trade count" across grains.

*Public summaries contain no raw brokerage statements, account numbers, or private transaction exports.*
