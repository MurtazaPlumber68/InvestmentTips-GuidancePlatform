# Investment Tips and Guidance Platform


An open‑source Python toolkit and companion database for transparent, consistent, and comprehensive financial analysis across equities, options, currencies, crypto, ETFs, bonds, commodities, and more.

## 🚀 Features

- **Transparent Calculations**  
  150+ financial ratios, indicators, and performance/risk measures with fully disclosed formulas (no hidden methods).

- **Multi‑Asset Support**  
  Equities, Options, Currencies, Cryptocurrencies, ETFs, Mutual Funds, Indices, Money Markets, Commodities, Economic Indicators, and more.

- **Streamlined Workflow**  
  Fetch historical data, financial statements, ratios, models (e.g., extended DuPont), options greeks, performance metrics, risk measures, technical indicators, and fixed income yields—all with a single API.

- **Jupyter Notebooks & How‑To Guides**  
  Interactive examples from basic usage to custom ratio creation and advanced portfolio analytics.

## 📦 Installation

```bash


# Initialize for Apple & Microsoft
companies = Toolkit(
    tickers=["AAPL", "MSFT"],
    api_key=API_KEY,
    start_date="2017-12-31"
)

# Historical data (OHLC, volumes, dividends, returns)
historical = companies.get_historical_data()

# Financial statements (Income, Balance Sheet)
income_stmt = companies.get_income_statement()

# Profitability ratios
profit_ratios = companies.ratios.collect_profitability_ratios()

# Extended DuPont analysis
dupont = companies.models.get_extended_dupont_analysis()

# Options greeks
greeks = companies.options.collect_all_greeks(expiration_time_range=180)

# Performance – factor correlations
correlations = companies.performance.get_factor_asset_correlations(period="quarterly")

# Risk – Value at Risk (VaR)
var = companies.risk.get_value_at_risk(period="weekly")

# Technicals – Ichimoku Cloud
ichimoku = companies.technicals.get_ichimoku_cloud()

# Fixed Income – ICE BofA effective yields
bond_yields = companies.fixedincome.get_ice_bofa_effective_yield()

# Economics – Unemployment rates
unemployment = companies.economics.get_unemployment_rate()
