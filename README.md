# OPEX Intelligence Pro v12.3 - Forecast Engine

Developed by **Deepak Shori**.

## What is new in v12.3

- Adds **Monthwise Forecast** from the selected YTD month to December.
- Adds **Account Monthwise Forecast** for account-level projection.
- Adds dashboard line chart for monthwise forecast to year end.
- Adds PowerPoint-ready native Excel charts for forecast and projected variance.
- Keeps v12.2 Professional Reporting sheets and category narratives.

## Forecast method

The tool assumes the selected vessel expense file contains YTD expense data up to the selected month.

```text
Average monthly spend = YTD Actual / selected month
Projected YTD actual for future month = YTD Actual + average monthly spend × future months remaining
Projected YTD budget for future month = Annual Budget × future month / 12
Projected variance = Projected YTD Budget - Projected Actual Expense
```

## Existing rules retained

- Category A excluded from variance.
- Category names expanded as B-H.
- Actual expense includes Bill/Bill Credit plus E-code journal expenses as per rules.
- E1940/E1941/E1944 PO costs ignored and shown separately.
- Open accruals are excluded from variance and shown as prognosis.
- Category variance narratives and comment approval retained.

## GitHub build

Upload the complete folder structure to GitHub, preserving:

```text
.github/workflows/build-windows-exe.yml
engine/
reports/
config/
main.py
requirements.txt
version_info.txt
README.md
```

Then run GitHub Actions > Build Windows EXE.
