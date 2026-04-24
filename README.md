# ACC102 Mini Assignment - Track 2: Profitability Analysis of US Technology Companies

## 1. Problem & User
This project analyzes the profitability performance of the US technology industry from 2020 to 2025, and compares the net profit margins of three leading tech giants: Apple, Microsoft, and NVIDIA. It is designed for finance and accounting students and novice investors interested in understanding sector and firm-level profitability trends.

## 2. Data
Data source: **WRDS Compustat Annual Fundamental Database**, covering the period 2020–2025.

Access date: 24 April 2026

Key fields include:
- `gvkey`: Firm identifier
- `conm`: Company name
- `sich`: Standard Industrial Classification (SIC) code
- `fyear`: Fiscal year
- `sale`: Net sales (revenue)
- `gp`: Gross profit
- `ni`: Net income

The industry scope is defined using SIC codes between 3000–9000 to focus on technology-related sectors.

## 3. Methods
The analysis follows these main steps:
1.  **Data Acquisition**: Connect to the WRDS database and extract the full dataset for 2020–2025.
2.  **Data Cleaning**: Remove observations with missing financial values (`sale`, `gp`, `ni`), filter out firms with non-positive revenue, and calculate gross and net profit margins.
3.  **Industry Trend Analysis**: Use SIC codes to filter the tech industry, then calculate the average gross and net profit margins per year.
4.  **Firm Comparison**: Select Apple, Microsoft, and NVIDIA, and plot their net profit margin trends for comparison.

## 4. Key Findings
- The US technology industry’s gross profit margin remains stable at around 45–48% throughout 2020–2025, reflecting consistent cost control.
- The industry’s net profit margin shows mild but steady growth, rising from around 5% in 2020 to nearly 10% in 2025.
- Microsoft maintains the most stable performance, with net profit margins consistently between 30–37%.
- Apple’s net profit margin gradually improves from ~21% in 2020 to ~28% in 2025.
- NVIDIA exhibits a dramatic V-shaped trend: its margin dropped to ~17% in 2022 before surging to nearly 50% in 2023, driven by AI chip demand.

## 5. How to Run
To run this notebook, you need:
1.  Python 3 with the following libraries installed:
    - `pandas`
    - `matplotlib`
    - `wrds`
2.  A valid WRDS account to access the Compustat database.
3.  Clone this repository and open the `.ipynb` file in Jupyter Notebook or JupyterLab.

## 6. Limitations & Next Steps
- **Limitations**: NVIDIA’s data is incomplete beyond 2023, and the analysis is limited to profit margins without considering other metrics like revenue growth.
- **Next Steps**: The analysis could be extended to include more tech firms, compare performance across different sub-sectors, or incorporate additional financial ratios for a more comprehensive evaluation.
