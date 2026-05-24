# DAND Projects (Udacity Course)
# Communicate-Prosper-Loan-Dataset-Findings-DAND-Project
Communicate Prosper Loan Dataset Findings - DAND 3rd Project
# Prosper Marketplace Peer-to-Peer Lending Data Exploration
## by Saja Khdour

## Dataset

> This project analyzes financial loan performance data from Prosper, a peer-to-peer lending platform. The core dataset focuses on closed loan records (containing only "Completed" or "Defaulted" outcomes) to evaluate risk patterns across borrower profiles. The primary variables investigated include:
- **ProsperRating (Alpha):** The proprietary internal risk scoring grade assigned to borrowers (from safest 'AA' to riskiest 'HR').
- **BorrowerAPR:** The total annual percentage cost of the loan to the borrower.
- **LoanOriginalAmount:** The initial approved principal capital amount requested by the borrower.
- **CreditScore:** The numeric credit score profile midpoint recorded at the time of loan generation.
- **IncomeRange:** The categorized personal annual earnings bracket reported by the borrower.
- **LoanStatusClean:** The final clear status of the closed loan tracking structural repayment success or default failure.

## Summary of Findings

- **The Risk Rating Framework is Highly Reliable:** Our univariate and bivariate investigations confirm that Prosper’s risk classification system cleanly reflects historical repayment realities. As loan grades drop down toward high-risk brackets (`E` and `HR`), real-world historical defaults expand significantly compared to successful loan closures.
- **Operational Volume Anchors:** Rather than operating on the extreme high or low risk margins, the largest operational transaction volume of the platform sits firmly within the moderate-risk middle tiers (`B`, `C`, and `D`), with tier `C` representing the single highest absolute count of active borrowers.
- **Credit Scores Dominate Financial Terms:** A borrower's primary credit score functions as the absolute master variable on the platform. Pristine credit score midpoints smoothly unlock massive loan capitals while commanding the lowest possible interest rate (APR) brackets.
- **Risk Restrictions Supercede High Personal Earnings:** While elevated income brackets generally match up with expanded borrowing capacity, credit risk functions as a hard constraint. When an applicant carrying high annual earnings registers a poor internal risk rating like `HR`, the underwriting logic aggressively caps their maximum allowed loan size to prevent investor loss.
- **The $0 Income Borrowers Explained:** Individuals reporting an income of `$0` are still capable of securing substantial approved loan balances. This happens because the system tracks *loan money approved* based on credit merit. These individuals represent highly creditworthy applicants backed by solid household cash assets, co-signers, or asset security rather than standard salaries.

## Key Insights for Presentation

> The final explanatory presentation condenses the core data narrative down to exactly four polished visualizations to demonstrate how the platform systematically mitigates structural financial hazard.

1. **Marketplace Composition (Univariate Count Plot):** Establishes the visual distribution baseline of the platform, showing how the business relies on moderate-risk categories (`B`, `C`, `D`) while maintaining tight controls at the extreme margins. All axis labels and bar values are cleanly formatted as whole numbers with thousands commas and zero trailing decimals.
2. **Credit Performance Mapping (Bivariate Grouped Count Plot):** Uses distinct green (Completed) and red (Defaulted) indicator clusters to prove that real-world risk scales consistently alongside the internal rating grades.
3. **Credit Score Domination Matrix (Multivariate Scatter Plot):** Investigates the three-way interaction between Loan Amount, Borrower APR, and Credit Score. Utilizing an optimized alpha setting of `0.3`, it perfectly highlights point density while revealing how excellent credit scores (bright plasma tones) capture the largest loan principal brackets at the lowest interest rates.
4. **Income vs. Risk Interaction Matrix (Multivariate Clustered Bar Chart):** Summarizes average loan caps across the intersection of income tiers and risk ranks. It incorporates floating dollar labels with zero trailing decimals to visually display how the platform overrides high salary power with strict principal caps whenever high structural risk (`HR`) is detected.

## References

- https://matplotlib.org/stable/api/ticker_api.html
- https://seaborn.pydata.org/generated/seaborn.countplot.html
- https://seaborn.pydata.org/generated/seaborn.scatterplot.html
- https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.pivot_table.html
