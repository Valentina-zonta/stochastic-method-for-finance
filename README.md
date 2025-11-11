# Stochastic Methods in Finance: Reports and Analysis

This repository contains a collection of reports and analyses on fundamental topics in quantitative finance. Each report tackles a specific problem, from option pricing to risk management, by applying theoretical models and comparing them against real-world market data.

##  Table of Contents

Here is a brief description of each report's contents:

### Report 1: One-Period Binomial Model
* [cite_start]**Objective:** To price a call option on the asset Supermicro (SMCI) using the one-period binomial model[cite: 5].
* [cite_start]**Methodology:** The model is applied to options with 3-month and 6-month maturities[cite: 8]. [cite_start]Historical volatility is calculated and used to find the theoretical price, which is then compared to the market price[cite: 53, 54, 58, 69, 70, 74, 78].
* [cite_start]**Result:** The analysis highlights the limitations of this simple model, revealing a significant error (23-24%) compared to real-world prices[cite: 77, 93, 98, 99].

### Report 2: Calculating Implied Dividends (Box-Spread & Put-Call Parity)
* [cite_start]**Objective:** To attempt to calculate the dividends implied in Morgan Stanley (MS) options[cite: 340, 341].
* [cite_start]**Methodology:** Two techniques are applied: the **Box-Spread** strategy [cite: 359, 401] [cite_start]and **Put-Call Parity**[cite: 370, 401].
* [cite_start]**Result:** The analysis yields unexpected results, such as negative implicit dividends[cite: 430, 435]. [cite_start]This report demonstrates a key practical lesson: theoretical models valid for European options will fail if misapplied to American options, which were used in this analysis[cite: 398, 432, 433, 434].

### Report 3: Convergence of Pricing Models
* [cite_start]**Objective:** To compare the convergence speed of discrete-time pricing models against the analytical Black-Scholes formula[cite: 877, 879].
* [cite_start]**Methodology:** The **N-step Binomial Model** [cite: 882] [cite_start]and the **Leisen-Reimer (L-R) Model** [cite: 911] are compared head-to-head.
* [cite_start]**Result:** Both models converge to the Black-Scholes price as the number of steps (N) increases[cite: 908, 1029]. [cite_start]However, the L-R model is shown to be far more efficient, converging faster and with greater accuracy for a smaller number of steps[cite: 969, 1027, 1028].

### Report 4: Analysis of "The Greeks"
* [cite_start]**Objective:** To calculate, visualize, and analyze the "Greeks" (Delta, Gamma, Vega, Theta, Rho), which measure an option's price sensitivity[cite: 1333, 1340, 1345].
* **Methodology:**
    1.  [cite_start]**Theory:** 3D surfaces are generated for each Greek using the Black-Scholes formulas (via VBA)[cite: 1373, 1377].
    2.  [cite_start]**Practice:** Real-world market data (from Refinitiv) for Adyen NV (ADYEN.AS) is analyzed, showing the "implied volatility smile" phenomenon[cite: 1334, 1577, 1581].
* [cite_start]**Result:** The calculated theoretical values are compared against market data, and the discrepancies are analyzed[cite: 1336, 1590].

### Report 5: Monte Carlo Methods for Option Pricing
* [cite_start]**Objective:** To use Monte Carlo (MC) simulation methods to price various types of options[cite: 106].
* [cite_start]**Methodology:** Leveraging simulations based on Geometric Brownian Motion (GBM)[cite: 112, 177], prices are calculated for:
    * [cite_start]**Vanilla Options:** Comparing the MC result with the Black-Scholes formula[cite: 193, 205].
    * [cite_start]**Exotic (Path-Dependent) Options:** Asian Options [cite: 134, 259] [cite_start]and Lookback Options[cite: 148, 259].
    * [cite_start]**Certificates:** A "Worst-Of" certificate on a basket of 3 assets (NVDA, MSFT, GOOGL) is priced[cite: 109, 310, 313].

### Report 6: Value at Risk (VaR) Analysis
* [cite_start]**Objective:** To calculate and compare different methodologies for estimating Value at Risk (VaR)[cite: 442, 443].
* **Portfolio:** A balanced portfolio composed of McDonald's (MCD) and Yum! [cite_start]Brands (YUM)[cite: 442, 543].
* **Methodology:** VaR is calculated using 5 distinct approaches:
    1.  [cite_start]Parametric Normal (flat sigma) [cite: 444, 585]
    2.  [cite_start]Parametric Normal (with EWMA volatility) [cite: 445, 636]
    3.  [cite_start]Monte Carlo Simulation [cite: 446, 693]
    4.  [cite_start]Historical VaR (percentile method) [cite: 447, 518, 755]
    5.  [cite_start]Historical Simulation (sampling from historical distribution) [cite: 447, 522, 808]
* [cite_start]**Result:** Beyond the comparison, the analysis investigates **subadditivity**, demonstrating that the portfolio's VaR is not always less than the sum of its parts, highlighting a well-known limitation of this risk metric[cite: 448, 449, 862, 863, 871].

## 🛠️ Tools Used

* [cite_start]**VBA (Visual Basic for Applications)** for implementing models in Excel[cite: 177, 924, 1333, 1589].
* **Python** (likely with `pandas`, `numpy`, `matplotlib`) for VaR analysis and plot generation.
* [cite_start]**Refinitiv Eikon** as the source for market data[cite: 543, 1576, 1659].
