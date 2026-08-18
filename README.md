Comparable Company Analysis Dashboard

Developed a sector-aware comps screener using HTML, CSS and JavaScript, integrating with the Financial Modelling Prep (FMP) API via asynchronous calls to retrieve enterprise value, key metrics, ratios and financial statement data across a peer universe of 100+ equities spanning eight GICS-style sectors.

Comparable company analysis values a business by benchmarking it against similar peers on a common valuation multiple, on the assumption that businesses with similar risk, growth and margin profiles should trade at broadly similar multiples. It's a relative valuation approach rather than an intrinsic one, used to flag which names in a peer group look cheap or expensive versus the group, and why.

The application values each sector on the multiple most appropriate to its underlying economics rather than applying a single metric universally. 

EV/EBITDA is used as the default valuation metric, applied to Technology, Consumer Discretionary, Communication Services, Healthcare, Consumer Staples and Energy, as it is capital-structure neutral and suits companies with established, comparable operating margins.

Two sectors override this default: 

- Financials are valued on Price/Book, since leverage is intrinsic to the business model and EV-based multiples are distorted by balance-sheet debt; 

- Industrials are valued on EV/EBIT, which charges each company for depreciation of its asset base given the sector's capital intensity. Using EBITDA instead would flatter companies that need continuous capex just to sustain operations, so EV/EBIT is used instead to keep that cost in the multiple.

Each sector's primary multiple is paired with secondary multiples (e.g., EV/Sales and EV/FCF) as cross-checks, and a quality metric (EBITDA margin, or ROE for Financials) is layered in to distinguish genuinely undervalued names from weaker businesses trading cheap for a reason.

Retrieved data is processed to compute peer medians, quartiles, percentile-based rankings, and a blended 0–100 value score per company, then visualised dynamically through bar, scatter, and grouped-bar charts, and a sortable comparables table, providing a real-time view of relative valuation, dispersion, and quality across each sector's peer set.
