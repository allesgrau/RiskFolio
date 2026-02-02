## RiskFolio: Investment forecasting & risk quantification ##

*Project created at the Warsaw University of Technology, Faculty of Mathematics and Information Science, for the Advanced Object-Oriented & Functional Programming course.*
*Authors: Adam Bagiński, Aleksandra Dmitruk, Barbara Gawlik*

RiskFolio is a desktop application developed in Java 21, designed to build virtual investment portfolios and simulate their future value. By utilizing statistical algorithms and the Monte Carlo method, the system provides forecasts based on real historical financial data, helping users understand not just potential returns, but also the associated market risks.

### Key features ###
- **Portfolio management** - Add assets via ticker search (supporting ~2400 assets), define weights, and set initial capital.
- **Automated data ingestion**: Automatically fetches historical data from the Stooq external API.
- **Simulation engine** - Runs 10,000 Monte Carlo scenarios to calculate metrics like mean return, max return, VaR, and CVaR.
- **GARCH(1,1) optimization** - Automatically estimates optimal GARCH parameters for the user's specific portfolio configuration.
- **Data reliability**: Handles incomplete data by filling gaps with WIG20 (for Polish assets) or S&P 500 (for US assets) indices, or trimming history for others.
- **Privacy** - No user data is stored; all inputs are cleared after the session ends.

### Tech stack ###

* Language: Java 21
* GUI: JavaFX
* Build tool: Maven
* IDE: IntelliJ IDEA 2024
* Data source: Stooq API
