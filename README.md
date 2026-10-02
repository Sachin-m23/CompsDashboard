Comparable Company Analysis Dashboard

Developed a sector-aware comps screener using HTML, CSS and JavaScript. It pulls enterprise value, key metrics, ratios and financial statement data from the Financial Modelling Prep (FMP) API through asynchronous calls, covering all 503 S&P 500 constituents across the 11 GICS sectors and 64 industries.

Comparable company analysis values a business by benchmarking it against similar peers on a common valuation multiple. It assumes that businesses with similar risk, growth and margin profiles should trade at broadly similar multiples. It is a relative valuation approach rather than an intrinsic one, used to flag which names in a peer group look cheap or expensive versus the group, and why.

The application values each sector on the multiple most appropriate to its underlying economics rather than applying a single metric universally.

EV/EBITDA is the default valuation metric, applied to Information Technology, Communication Services, Consumer Discretionary, Consumer Staples, Health Care and Real Estate. It is capital-structure neutral and suits companies with established, comparable operating margins.

Two groups of sectors override this default:
Financials are valued on Price/Book, since leverage is intrinsic to the business model and EV-based multiples are distorted by balance-sheet debt.

Asset-intensive sectors (Industrials, Materials, Energy and Utilities) are valued on EV/EBIT, which charges each company for depreciation of its asset base. Using EBITDA would flatter companies that need continuous capex just to sustain operations, so EV/EBIT keeps that cost in the multiple. Real Estate is deliberately kept on EV/EBITDA: property depreciation is an accounting charge that tends to understate asset value, and EBITDA is the closest available proxy to FFO.

Each sector's primary multiple is paired with secondary multiples (e.g., EV/Sales, EV/FCF, EV/OCF) as cross-checks. P/E is applied in every sector as a common equity-level check. A quality metric is layered in to separate genuinely undervalued names from weaker businesses trading cheap for a reason. That metric is EBITDA margin for most sectors and ROE for Financials, set against a CAPM-derived cost of equity to show whether a bank earns its cost of capital.

Users can narrow any sector to a single industry (e.g., Aerospace & Defence within Industrials), recalculating medians, rankings and charts for a like-for-like peer set. An implied valuation module applies the peer median multiple (excluding the target) to a chosen company's latest full-year EBITDA, EBIT or book value. It bridges enterprise value to equity value, divides by shares outstanding, and shows the implied share price and upside against the current price.

Retrieved data is processed to compute peer medians, quartiles, percentile-based rankings and a blended 0–100 value score per company, with P/E and each sector's multiples weighted equally. Results are visualised through bar, scatter and grouped-bar charts and a sortable comparables table, giving a live view of relative valuation, dispersion and quality across each peer set.
