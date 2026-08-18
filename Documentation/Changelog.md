# Changelog

All notable changes to this model are documented here.

## [2.1] — Condensed Deck & Charts README

### Changed
- `Tesla_DCF_Valuation_Presentation.pptx` condensed from 20 slides to 11 slides (title + 9 content pages + closing), mirroring the condensed `Documentation.pdf` structure
- `README.md` rebuilt with a dedicated Charts section (Revenue & Net Income trend, WACC build-up, sensitivity heatmap, scenario comparison, model architecture) generated directly from model calculations, distinct from the existing live-workbook screenshots
- `Images/Charts/` subfolder added to hold the five chart PNGs referenced in the README

## [2.0] — Condensed Documentation

### Changed
- `Documentation.pdf` condensed 12 pages (Formula Dictionary, References), consolidating multiple topics per page while retaining all figures, tables, and screenshots
- Page structure changed to: Cover, Project Overview, Workbook Structure, Assumptions & Forecast Methodology, Financial Model Design, Valuation Methodology, Key Outputs & Analysis, Model Checks & Best Practices, Limitations & Risks, Conclusion, Formula Dictionary, References

## [1.5] — Documentation Package

### Added
- `Documentation.pdf` — 12-page analyst-manual-style writeup covering 
- `Assumptions.pdf` — standalone 11-page assumptions register, split out from `Documentation.pdf` Section 5 for quick reference
- `Tesla_DCF_Valuation_Presentation.pptx` expanded from a 10-slide executive summary to a 20-slide deck mirroring the full documentation structure
- `Images/` folder with 8 screenshots captured directly from the live workbook (Cover, DCF, WACC, Financial Statements, Revenue Drivers, Sensitivity, Balance Sheet Check, Deliveries Scenario)
- `LICENSE` and this `Changelog.md`

## [1.4] — Final Base Case Release

### Fixed
- Scenario toggle (`Drivers!C3`) confirmed set to `2` (Base Case) as the primary reported output
- Remaining spelling corrections: "Digital assets, net" punctuation, "customer deposits," "Levered Beta" (WACC!I32), "Revenue growth rate" (P&L)
- Vehicle naming fully standardized to "Tesla Cybertruck" across all sheets (previously split between "Cybertruck" and "Pickup" depending on tab)

### Known Open Items
- `DCF Valuation!B9` ("Prepaid Expenses") and `Cash Flow!B18` ("Other liabilities") reverted to earlier typos in the final upload; flagged for a future pass

## [1.3] — Structural Fixes

### Fixed
- `PP&E!H18` — depreciation formula was referencing the wrong useful-life assumption cell (`C13` instead of `C12`); corrected to match every other forecast year
- `Deliveries` Worst Case block — row labels were shifted by one, causing "Tesla Model Y" to display as "Tesla Cybertruck" and vice versa; the underlying figures were always correct, only the labels were wrong
- Majority of outstanding spelling corrections across WACC, DCF Valuation, and Balance Sheet tabs

## [1.2] — Spelling & Labeling Pass

### Fixed
- WACC tab: "weitage" → "weight," "leavered/unleavered" → "levered/unlevered," "Avarage" → "Average"
- DCF Valuation: "Net Capx" → "Net Capex"

## [1.1] — Core Methodology Fixes

### Fixed
- **Sensitivity table (DCF Valuation)** — replaced a native Excel Data Table construct (which threw `#VALUE!` errors when recalculated outside Excel) with direct live formulas referencing the terminal value calculation, so the table now recalculates automatically in any spreadsheet program
- **WACC target capital structure** — target D/E was being calculated by averaging historical D/E *ratios* directly; corrected to average the historical debt *weights* instead, which is the methodologically correct approach. This moved WACC from 10.38% to 10.41%

## [1.0] — Initial Model

- Full three-statement integrated model with operating drivers for Automotive and Energy & Other segments
- DCF valuation with Hamada-based WACC build
- Best / Base / Worst case scenario toggle across all operating drivers
- Initial audit identified the issues addressed in versions 1.1–1.4 above
