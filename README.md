# Tesla Inc. Integrated Financial Model & Valuation

An independent, bottom-up discounted cash flow (DCF) valuation of Tesla, Inc. (NASDAQ: TSLA), built on a fully integrated three-statement financial model with explicit operating drivers, a Damodaran-consistent cost of capital framework, and scenario analysis.

## 1. Headline Output

| | |
|---|---|
| **DCF Intrinsic Value per Share (Base Case)** | $24.23 |
| **Current Market Price** | $408.95 |
| **Implied Price / Intrinsic Value Multiple** | 16.9x |
| **WACC** | 10.41% |
| **Cost of Equity** | 11.10% |
| **Levered Beta (target capital structure)** | 1.19 |
| **Scenario Range (Worst → Best)** | −$9.56 → $65.29 |

> **On the gap to market price:** this DCF values Tesla's core automotive and energy business exactly as reflected in its financial statements and this model's operating assumptions. It does **not** separately value optionality the market may be pricing in — FSD licensing, autonomous ride-hailing, Optimus/humanoid robotics, or energy storage scale-up beyond the base forecast. A gap of this size says something about the *scope* of a fundamentals-only DCF, not that the market is irrational or the model is broken.

## 2. Project Description

This project is a fully integrated three-statement financial model and DCF valuation for Tesla, Inc., built from the ground up in Excel. It forecasts vehicle deliveries, pricing, and margins by product line (Model 3, Model S/X, Model Y, Cybertruck, Semi), links those forecasts through a complete income statement, balance sheet, and cash flow statement, and estimates intrinsic value using a bottom-up FCFF discounted cash flow methodology.

It was built as an independent portfolio project to demonstrate financial modeling, corporate finance, and valuation skills applied to a real, publicly traded company — not as investment advice or a research report. Every historical figure traces back to Tesla's public SEC filings; every forecast assumption is documented with its rationale rather than left as an unexplained number.

## 3. Documentation — Long & Short Versions

Every write-up in this project comes in two lengths, so you can pick the right depth for the audience:

| Document | Short Version | Long Version |
|---|---|---|
| **Analyst Documentation** | [`Documentation_Short.pdf`](./Documentation_Short.pdf) — 15 pages | [`Documentation_Long.pdf`](./Documentation_Long.pdf) — 23 pages |
| **Assumptions Reference** | [`Assumptions_Short.pdf`](./Assumptions_Short.pdf) — 2 pages | [`Assumptions_Long.pdf`](./Assumptions_Long.pdf) — 11 pages |
| **Presentation Deck** | [`Tesla_DCF_Valuation_Presentation_Short.pptx`](./Tesla_DCF_Valuation_Presentation_Short.pptx) — 11 slides | [`Tesla_DCF_Valuation_Presentation_Long.pptx`](./Tesla_DCF_Valuation_Presentation_Long.pptx) — 20 slides |

**Use the Short versions** for a quick read, a recruiter screen, or a live walkthrough. **Use the Long versions** for a deep technical review — they cover every operating segment (Automotive, Energy & Other), every supporting schedule (PP&E, working capital, financing), and the full methodology behind each number, section by section.

## 4. Charts

Visual highlights generated directly from the model's calculations — not screenshots. All available at full resolution in [`Images/Charts/`](./Images/Charts/).

<table>
<tr>
<td width="50%">

**Revenue & Net Income Trend**
![Revenue and Net Income](./Images/Charts/Revenue%20and%20Net%20Income.png)
Historical actuals (FY2021–2025) vs. Base Case forecast (FY2026–2032).

</td>
<td width="50%">

**Gross & EBIT Margin Trend**
![Margin Trend](./Images/Charts/Margin%20Trend.png)
Margin compression as opex converges toward peer-benchmarked levels.

</td>
</tr>
<tr>
<td width="50%">

**Cost of Capital Build-Up**
![WACC Buildup](./Images/Charts/WACC%20Buildup.png)
CAPM cost of equity and after-tax cost of debt, blended to WACC.

</td>
<td width="50%">

**DCF Value Bridge**
![DCF Value Bridge](./Images/Charts/DCF%20Value%20Bridge.png)
Enterprise Value → Equity Value, step by step.

</td>
</tr>
<tr>
<td width="50%">

**DCF Sensitivity (WACC × Terminal Growth)**
![Sensitivity Heatmap](./Images/Charts/Sensitivity%20Heatmap.png)
Terminal value ($M) across a range of WACC and growth assumptions.

</td>
<td width="50%">

**Scenario Comparison**
![Scenario Comparison](./Images/Charts/Scenario%20Comparison.png)
Intrinsic value per share: Worst / Base / Best vs. market price.

</td>
</tr>
</table>

**Model Architecture**
![Model Architecture](./Images/Charts/Model%20Architecture.png)

## 5. Screenshots

Captured directly from the live workbook — available in [`Images/`](./Images/).

<table>
<tr>
<td width="50%">

**DCF Valuation**
![DCF](./Images/DCF.png)

</td>
<td width="50%">

**Cost of Capital (WACC)**
![WACC](./Images/WACC.png)

</td>
</tr>
<tr>
<td width="50%">

**Financial Statements (P&L)**
![Financial Statements](./Images/Financial%20Statements.png)

</td>
<td width="50%">

**Revenue Drivers (Scenario Toggle)**
![Revenue Drivers](./Images/Revenue%20Drivers.png)

</td>
</tr>
<tr>
<td width="50%">

**Balance Sheet Check Row**
![Balance Sheet Check](./Images/Balance%20Sheet%20Check.png)

</td>
<td width="50%">

**Deliveries Scenario**
![Deliveries Scenario](./Images/Deliveries%20Scenario.png)

</td>
</tr>
</table>

## 6. Project Objectives

- Build an integrated three-statement model
- Forecast operating performance by segment and product line
- Estimate intrinsic value using DCF
- Analyze business drivers (deliveries, pricing, margins, opex, working capital, capex)
- Demonstrate financial modeling best practices (color coding, integrity checks, scenario toggles)

## 7. Features

- Dynamic assumptions with a single scenario toggle (Best / Base / Worst case)
- Driver-based forecasting by vehicle line and segment
- Full three-statement integration with balance-check integrity rows
- Segment revenue modeling (Automotive + Energy & Other)
- Working capital schedule (DSO / DIO / DPO)
- PP&E schedule with vintage-based depreciation
- Debt/equity financing schedule
- Bottom-up (Hamada) WACC build
- DCF valuation with Gordon Growth terminal value
- Two-way sensitivity analysis (WACC × terminal growth)
- Verified error checks (0 formula errors, balance sheet ties to zero every period)

## 8. Workbook Structure

| Section | Sheets |
|---|---|
| Cover | Cover |
| Drivers | Drivers |
| Inputs | P&L Input, Balance Sheet Input |
| Workings | Deliveries, Average Prices, Automotive Revenue/Gross Margin/Gross Profit, Revenue & Gross Profit Energy & Other, Opex, PP&E, Working Capital, Financing (plus comparable-data tabs for each) |
| Outputs | P&L, Balance Sheet, Cash Flow |
| Valuation | WACC, DCF Valuation |

38 sheets total, including labeled section-divider tabs for navigation.

## 9. Model Flow

```
Historical Data
      ↓
Forecast Drivers
      ↓
Revenue (Deliveries × ASP, by segment)
      ↓
Margins (Gross Profit, Opex)
      ↓
Financial Statements (P&L, Balance Sheet, Cash Flow)
      ↓
FCFF (NOPAT − Reinvestment)
      ↓
WACC (CAPM + Target Capital Structure)
      ↓
DCF (Terminal Value + PV of Cash Flows)
      ↓
Intrinsic Value per Share
```

## 10. Key Assumptions

| Assumption | Value |
|---|---|
| Risk-free rate | 4.55% (10-yr U.S. Treasury) |
| Equity market risk premium | 5.50% |
| Beta (relevered, target structure) | 1.19 |
| Marginal tax rate | 21.0% |
| Terminal growth rate | 4.55% (capped at risk-free rate) |
| WACC | 10.41% |
| Capex basis | % of prior-year PP&E |
| Working capital | 5-yr average DSO/DIO/DPO |

Full detail and sourcing for every assumption — including scenario band conventions for each driver — is in `Assumptions_Long.pdf` (or the 2-page `Assumptions_Short.pdf` for a quick table view).

## 11. Financial Concepts Used

Three-Statement Modeling · Free Cash Flow to Firm (FCFF) · WACC · CAPM · Hamada Beta Unlevering/Relevering · Terminal Value (Gordon Growth) · Discounted Cash Flow · Sensitivity Analysis · Operating Leverage · Working Capital Forecasting · Scenario Analysis

## 12. Skills Demonstrated

Financial Modeling · Corporate Finance · Valuation · Forecasting · Accounting · Excel · Scenario Analysis · Investment Analysis · Capital Budgeting · Financial Statement Analysis · Data Structuring

## 13. Folder Structure

```
Tesla-Inc-Integrated-Financial-Model/
│
├── README.md
├── LICENSE
├── Changelog.md
├── Tesla_Inc__Integrated_Financial_Model___Valuation.xlsx
├── Documentation_Short.pdf
├── Documentation_Long.pdf
├── Assumptions_Short.pdf
├── Assumptions_Long.pdf
├── Tesla_DCF_Valuation_Presentation_Short.pptx
├── Tesla_DCF_Valuation_Presentation_Long.pptx
└── Images/
    ├── Cover.png
    ├── DCF.png
    ├── WACC.png
    ├── Financial Statements.png
    ├── Revenue Drivers.png
    ├── Sensitivity.png
    ├── Balance Sheet Check.png
    ├── Deliveries Scenario.png
    └── Charts/
        ├── Revenue and Net Income.png
        ├── Margin Trend.png
        ├── WACC Buildup.png
        ├── DCF Value Bridge.png
        ├── Sensitivity Heatmap.png
        ├── Scenario Comparison.png
        └── Model Architecture.png
```

## 14. Future Improvements

- Scenario manager (beyond the current single-toggle Best/Base/Worst)
- Monte Carlo simulation on key operating drivers
- Relative valuation (comparable company multiples)
- Football field valuation summarizing DCF, comps, and 52-week range
- VBA automation for scenario switching and reporting
- Power BI dashboard layer for interactive exploration

## 15. Disclaimer

This project was built for educational and portfolio purposes only. All historical figures are drawn from Tesla, Inc.'s public SEC filings; forward-looking figures are model estimates. This is not investment advice, a research report from a registered investment adviser or broker-dealer, or a recommendation to buy, sell, or hold any security.

---

📄 Documentation: [`Short`](./Documentation_Short.pdf) · [`Long`](./Documentation_Long.pdf)
📋 Assumptions: [`Short`](./Assumptions_Short.pdf) · [`Long`](./Assumptions_Long.pdf)
📊 Presentation: [`Short`](./Tesla_DCF_Valuation_Presentation_Short.pptx) · [`Long`](./Tesla_DCF_Valuation_Presentation_Long.pptx)
