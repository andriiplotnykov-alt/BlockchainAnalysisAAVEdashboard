# Blockchain                                                                                                                                                                      Transaction Analysis Dashboard

## Project Overview
This project analyzes recent on-chain transaction activity from the AAVE protocol, transforming raw blockchain transaction traces into a structured analytical model and an interactive Power BI dashboard. The objective is to convert complex DeFi transaction data into clear, decision-oriented insights on user behavior, asset activity, and protocol usage dynamics.

Raw transaction data was extracted directly from the AAVE blockchain in JSON format and contained mixed transaction types, heterogeneous structures, and protocol-level metadata. The dataset was then fully transformed, standardized, and modeled to enable meaningful financial and behavioral analysis.

---

## Dashboard Features & Insights
The Power BI dashboard provides an interactive exploration of AAVE protocol activity:

- **Asset selector slicer** allowing token-level analysis
- **Transaction activity breakdown** showing the relative share of deposits, borrows, repays, and withdrawals per asset
- **Donut chart** illustrating transaction distribution across token tickers

![AAVE Transaction Dashboard](AAVE%20Transactions/docs/Dashboard_screenshot.png)

---

## Data Pipeline & Transformation
- Extracted raw AAVE transaction traces (JSON) from an on-chain data source
- Parsed and separated heterogeneous transaction types into four analytical fact tables:
  - Deposits  
  - Borrows  
  - Repays  
  - Withdrawals
- Cleaned, standardized, and normalized transaction values using Power Query
- Converted on-chain numerical formats into human-readable units using asset decimals
- Built a star schema with:
  - Centralized date dimension
  - Asset (token) dimension shared across all transaction tables
- Ensured consistency of users, timestamps, and asset identifiers across the model

---

## Data Model
The analytical model follows a star schema optimized for performance and clarity:
- Fact tables: Deposits, Borrows, Repays, Withdrawals
- Dimension tables:
  - Asset dimension (token symbols, addresses, decimals)
  - Date dimension (centralized calendar for time-series analysis)

This structure enables efficient slicing by asset, time, and transaction type while maintaining analytical flexibility.

---

## Key Analytical Focus
- User participation and concentration across assets
- Relative intensity of borrowing vs liquidity provision
- Transaction behavior distribution by token
- Central tendency of transaction sizes using median-based measures
- Temporal evolution of protocol activity

---

## Tools & Technologies
- Blockchain transaction data (AAVE protocol)
- Power BI
- Power Query (data transformation and normalization)
- DAX (analytical measures and KPIs)
- Star schema data modeling
- JSON data processing

---

## Why This Project Matters
This project demonstrates the ability to:
- Work with raw, unstructured on-chain data
- Design analytical data models from first principles
- Translate DeFi transaction mechanics into financial insights
- Build interactive dashboards that communicate complex data clearly

It bridges decentralized finance data with traditional analytical workflows, highlighting how blockchain data can be structured for professional-grade analysis and reporting.
