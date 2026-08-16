# Trading Journal — Jameel Shaikh

Public summary of personal trading activity across NSE F&O, Currency F&O, MCX Commodity, and Equity. It separates lifetime broker-account reconciliation from historical public-series calculations that are reproducible from this repository but are not an authoritative continuous net-performance series.

**Live dashboards:** https://jams411.github.io/trading-journal/

## Canonical evidence status

The previously published **₹690,051.39** is retained only as broker-account adjusted lifetime net P&L across the available broker records. It is an accounting total, not a portfolio return or a continuous monthly performance series.

The public 25-observation series mixes Angel One net P&L with Zerodha gross P&L, does not allocate all Zerodha charges by month, cannot date Angel One's full controlling population, and omits April 2025. Its return, benchmark, risk, and drawdown outputs are therefore historical public-series calculations—not canonical verified performance metrics.

## Record-count grain

| Scope | Count | Source composition |
|---|---:|---|
| F&O realized-record entries | **4,523** | 4,292 Zerodha F&O tax-exit rows + 231 Angel One F&O FIFO closes |
| Available realized-record entries | **5,284+** | 5,053 Zerodha tax-exit rows + 231 Angel One F&O FIFO closes |

These are mixed-grain record counts, not uniform executions, orders, or trades.

## Strategy evidence

- Broker records support substantial NIFTY and BankNifty options/derivatives activity.
- Trading-process context includes options Greeks, implied volatility, open-interest analysis, position sizing, and structured trade review; these are not metrics reconstructed from the public series.
- Multi-leg options experience is retained as bounded strategy context with corroborating evidence from a limited execution subset. The records do not establish lifetime multi-leg prevalence or a lifetime short-premium/options-selling orientation.
- Currency F&O and MCX Commodity activity was discontinued after underperformance in those segments.

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

## Methodology and provenance

- **Public repository:** Provides summarized/analyzed trading data and reproduces the historical public-series calculations where applicable.
- **Private verification evidence:** Broker statements, tax-P&L reports, and trading exports were used to verify and reconcile the canonical record. Raw brokerage files are not published.
- **Reproducibility boundary:** A visitor can reproduce calculations from the embedded public arrays, but cannot reconstruct the complete broker record or a continuous combined monthly net series from this repository.
- **Accounting boundary:** Broker accounting bases and charge availability differ across sources; the private reconciliation controls canonical accounting definitions.
- **Date boundary:** The full Angel One controlling population does not contain realization dates, so no authoritative combined monthly series is currently available.

*Public summaries contain no raw brokerage statements, account numbers, or private transaction exports.*
