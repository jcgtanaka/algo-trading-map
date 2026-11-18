# Algo Trading Map: Printed Books Roadmap

Read books come from `books_printed/`. Books you plan to read come from the other folders in `alpha_quant/books/` and are linked to read books in Stage 9. CFA books and everything outside quant or algo trading are left out (see the last section).

## How to read this map

- **Stages** run from foundations to production. Read them in order, but you can skip ahead once you have the prerequisites.
- **IDs** (F1, S3, X5...) are used in the "Connects to" column so you can jump between books.
- **N-IDs** (N1, N2...) are books you haven't read yet. Stage 9 links each one to the read book it expands.
- **Location** is the folder inside `books_printed/`. `root` means the top folder, `Old` means `books_printed/Old/`, and so on. Duplicates across folders are listed once.
- **Verification:** author and title were checked on the first pages for the entries marked with a dagger (†). Everything else was described from its title and its well-known scope, not from a full table-of-contents pass. Entries marked ⚠ are title-only (the PDF has no readable text, or the content is unclear); check them before relying on them.

## Stage 0: Mathematical and stochastic foundations

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| F1 | Strang, *Introduction to Linear Algebra* (5th ed.) + solutions manual | root | Matrices, vector spaces, least squares: the base for factor models and covariance math | F3, P4, P3 |
| F2 | Axler, *Linear Algebra Done Right* | root | Proof-based linear algebra, for when F1 feels too procedural | F1, F3 |
| F3 | Gallier & Quaintance, *Optimization Theory with Applications to ML* | 2020_10_08 | Convex sets, duality, KKT conditions: the math behind portfolio optimization | F4, P4 |
| F4 | Boyd & Vandenberghe, *Convex Optimization* | root | Standard reference for convex solvers and constrained portfolio problems | F3, P1, P3 |
| F5 | Grimmett & Stirzaker, *Probability and Random Processes* | Stochastic Calculus for Finance | Probability, Markov chains, random walks: the base for return models | F6, F7, F9 |
| F6 | Billingsley, *Probability and Measure* | Stochastic Calculus for Finance | Measure-theoretic probability, for the formal side of F9 and F10 | F5, F7 |
| F7 | Jacod & Protter, *Probability Essentials* | Stochastic Calculus for Finance | Compact probability toolkit before stochastic calculus | F5, F6, F10 |
| F8 | Stefanica, *A Primer for the Mathematics of Financial Engineering* | root | Finance math in one place: bonds, options, Brownian motion | F9, V1, V5 |
| F9 | Shreve, *Stochastic Calculus for Finance I: The Binomial Asset Pricing Model* | Stochastic Calculus for Finance | Discrete-time pricing, replication, risk-neutral measure | F10, F8, V1 |
| F10 | Shreve, *Stochastic Calculus for Finance II: Continuous-Time Models* | Stochastic Calculus for Finance | Brownian motion, Black-Scholes, Itô calculus | F9, F11, V5 |
| F11 | Arguin, *A First Course in Stochastic Calculus* | Stochastic Calculus for Finance | A shorter, more intuitive route to Itô calculus | F10, F12 |
| F12 | Mikosch, *Elementary Stochastic Calculus with Finance in View* | Stochastic Calculus for Finance | Compact pricing-oriented stochastic calculus | F10, F11 |
| F13 | Protter, *Stochastic Integration and Differential Equations* | root | The rigorous reference for stochastic integrals and SDEs | F10, F12 |
| F14 | Glasserman, *Monte Carlo Methods in Financial Engineering* | Stochastic Calculus for Finance (2 files) | Monte Carlo pricing, variance reduction, Greeks by simulation: the core of simulation-based trading research | F15, C11 |
| F15 | Kloeden & Platen, *Numerical Solution of Stochastic Differential Equations* | Stochastic Calculus for Finance | Numerical SDE schemes, the engine behind simulation pricing | F14, F16 |
| F16 | Duffy, *Numerical Methods in Computational Finance (PDE/FDM)* | Stochastic Calculus for Finance | Finite-difference pricing as an alternative to Monte Carlo | F15, C1 |
| F17 | Kushner & Dupuis, *Numerical Methods for Stochastic Control Problems* | Stochastic Calculus for Finance | Stochastic control, the math behind optimal execution and market making | X9, F13 |
| F18 | Wilmott, *Paul Wilmott Introduces Quantitative Finance* | Old | A broad, applied introduction to derivatives and quant methods | F9, V1, V5 |
| F19 | Wilmott, *Frequently Asked Questions in Quantitative Finance*; *Paul Wilmott on Quantitative Finance* Vol. 1-3 | root | Deeper quant reference set; FAQ covers many interview-style questions | F18, V1 |

## Stage 1: Python and R tooling for data and research

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| T1 | Yan, *Python for Finance* | root | Python applications for quant finance: data, time value, simple models | T2, T5 |
| T2 | Hilpisch, *Python for Finance* (2019, Mastering Data-Driven Finance) | root, Old | Data pipelines, time series, option pricing in Python | T1, T4, M3 |
| T3 | Hilpisch, *Artificial Intelligence in Finance* | root | ML and deep learning applied to finance, in Python | T2, M3, M4 |
| T4 | Hilpisch, *Derivatives Analytics with Python* | root, Old | Option pricing, Monte Carlo, volatility surfaces in Python | T2, V1, V7 |
| T5 | *Mastering Python for Finance* | root, Old | Python for financial models and data analysis | T1, T2 |
| T6 | Lachowicz, *Python for Quants* Vol. I ⚠ | root, Old | Python for quant workflows (title-only check) | T2, T5 |
| T7 | Fletcher & Gardner, *Financial Modelling in Python* | Old | Financial modelling in Python: pricing, curves, risk | T2, F8 |
| T8 | *Mastering Pandas for Finance* | Old | Pandas for financial data: time series, cleaning, resampling | T9, T2 |
| T9 | McKinney, *Python for Data Analysis* (2nd ed.) | Old | The standard pandas and NumPy reference | T8 |
| T10 | Berlinger, *Mastering R for Quantitative Finance* | root (2 copies), Old | R for backtests, portfolio optimization, and risk management | T11, TS2 |
| T11 | *Financial Risk Modelling and Portfolio Optimization with R* (2nd ed.) | root | R-based risk models and portfolio optimization | T10, P3 |
| T12 | Fantazzini, *Quantitative Finance with R and Cryptocurrencies* (slides) | Old | Crypto-focused R time series and risk modelling | T10, TS1 |
| T13 | *Introduction to Python for Econometrics* | Old | Econometrics in Python: regression, time series | TS1, T9 |
| T14 | Raschka, *Python Machine Learning* (2017) | root, Old | Scikit-learn ML workflow: a common starting point for M-group models | M3, M1 |
| T15 | *Python Basics Handbook* | root | Quick Python syntax refresher | T1 |

## Stage 2: How to build and test a trading system

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| S1 | Chan, *Algorithmic Trading: Winning Strategies and Their Rationale* (2013) | root (Algorithmic Trading.pdf is the same book) | Why momentum and mean reversion work, and how to test them | S2, S3, S4 |
| S2 | Chan, *Quantitative Trading* (2nd ed., 2021) | root | Practical backtesting, regression, Kalman filters, and building a trading business | S1, S3, N12 |
| S3 | Chan, *Machine Trading* (2017) | root (2 copies) | ML-based trading pipeline: data, features, models, and costs | S2, M1, M3 |
| S4 | Chan, *Quantitative Trading: How to Build Your Own Algorithmic Trading Business* | Old, root | First-edition version of S2; useful for comparison | S2 |
| S5 | Halls-Moore, *Successful Algorithmic Trading*† | root, Old | QuantStart approach: event-driven backtests, data handling, IB execution | S6, S8, X11 |
| S6 | Halls-Moore, *Advanced Algorithmic Trading* | Old | Event-driven backtester, strategy testing, and live execution | S5, X11 |
| S7 | Halls-Moore, *C++ for Quantitative Finance*† | Old | The same QuantStart workflow implemented in C++ | S5, C10 |
| S8 | Davey, *Building Winning Algorithmic Trading Systems* | root | Robustness testing: walk-forward, Monte Carlo, and avoiding overfitting | S9, N8 |
| S9 | Davey, *Algo Trading Cheat Codes* (2021) | root | Shorter, practical version of S8 | S8 |
| S10 | Conlan, *Automated Trading with R* | root | End-to-end R platform for research and execution | T10, S5 |
| S11 | Kakushadze & Serur, *151 Trading Strategies* | Old | Catalog of strategy ideas by asset class: a source of hypotheses to test | S1, S2 |
| S12 | *The Ultimate Algorithmic Trading System Toolbox* ⚠ | root, Old | Trading system development toolkit (title-only check) | S8, N25 |
| S13 | Ehrman, *The Handbook of Pairs Trading*† | root, Old | Pairs selection and spread trading in equities, options, and futures | P2, P5 |
| S14 | Masters, *Testing and Tuning Market Trading Systems: Algorithms in C++* | Timothy Masters folder | Monte Carlo permutation tests and tuning without curve-fitting | S8, N8, M12 |
| S15 | Tulchinsky et al., *Finding Alphas* | Old | How alpha research works in practice: idea, test, combine | P4, M1 |
| S16 | Chen & Tsang, *Detecting Regime Change in Computational Finance* | root | Regime detection for switching strategies | M3, S1 |
| S17 | Guo, Lai, Shek & Wong, *Quantitative Trading: Algorithms, Analytics, Data, Models, Optimization* ⚠ | root | Broad quant trading reference (title-only check) | S2, P1 |
| S18 | Zeng, *A Comprehensive Reliability Test of Technical Trading Strategies* (MSc thesis, 2019)† | root | Statistical tests of technical trading rules: a worked example of S8's robustness testing | S8, S14, N8 |
| S19 | Doloc, *Applications of Computational Intelligence in Data-Driven Trading* ⚠ | 2020_10_08 | Computational-intelligence methods for trading (title-only check) | M3, S16 |
| S20 | Lee, *Quantum Finance: Intelligent Forecast and Trading Systems* ⚠ | 2020_10_08 | Forecasting and trading systems with quantum-inspired methods (title-only check) | S19, M3 |
| S21 | Sarmento & Horta, *A Machine Learning Based Pairs Trading Investment Strategy* | 2020_10_08 | ML-based pairs trading, end to end | S13, M1 |
## Stage 3: Portfolio construction, risk, and money management

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| P1 | Isichenko, *Quantitative Portfolio Management: The Art and Science of Statistical Arbitrage* | root | Statistical arbitrage: factor models, portfolio construction, and implementation | P2, P4, F4 |
| P2 | *Statistical Arbitrage Algorithmic Trading: Insights and Techniques* ⚠ | root, Old | Statistical arbitrage methods (author not checked) | P1, S13 |
| P3 | Paleologo, *Advanced Portfolio Management: A Quant's Guide for Fundamental Investors* | root (2 copies) | Turning alphas into portfolios: risk models, constraints, and transaction costs | P4, F4, T11 |
| P4 | Grinold & Kahn, *Advances in Active Portfolio Management* | root | The fundamental law of active management: how signal quality turns into returns | P3, S15, F3 |
| P5 | Gray & Vogel, *Quantitative Momentum* | Old | A practical momentum stock-selection system | S1, P4 |
| P6 | Vince, *The Mathematics of Money Management* | root | Optimal f, position sizing, and risk of ruin | P7, S8 |
| P7 | *The Kelly Capital Growth Investment Criterion: Theory and Practice* | 2020_10_08 | Kelly sizing in theory and practice, including fractional Kelly | P6, P8 |
| P8 | Harvey, Rattray & Van Hemert, *Strategic Risk Management* | root | Portfolio-level risk budgeting and design | P3, P9 |
| P9 | Burns, *The Ultimate Trading Risk Management Guide* | root | Practical stop-loss, drawdown, and position-risk rules | P6, P8 |
| P10 | Nash, *Effective Product Control: Controlling for Trading Desks* | root, Old | How a trading desk controls P&L, limits, and reconciliation | P9, X11 |

## Stage 4: Machine learning for trading signals

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| M1 | López de Prado, *Advances in Financial Machine Learning* | root | Labeling, purged cross-validation, meta-labeling, and bet sizing: the core ML-for-finance reference | M2, S8, S14 |
| M2 | López de Prado, *Machine Learning for Asset Managers* | root, 2020_10_08 | Clustering, denoising, and Hierarchical Risk Parity for portfolios | M1, P3 |
| M3 | Jansen, *Machine Learning for Algorithmic Trading* (2nd ed.) | 2020_10_08, root | End-to-end ML alpha pipeline with alternative data and notebooks | M1, S3, T3 |
| M4 | Dixon, Halperin & Bilokon, *Machine Learning in Finance: From Theory to Practice* | 2020_10_08 | ML for pricing, risk, and trading, with theory | M1, T3 |
| M5 | Nagel, *Machine Learning in Asset Pricing* | root | ML for return prediction and the factor zoo | M2, P4 |
| M6 | Karasan, *Machine Learning for Financial Risk Management with Python* | root | ML models for credit, market, and operational risk | P9, M4 |
| M7 | Nokeri, *Implementing Machine Learning for Finance* | root | Predictive risk and performance analysis for portfolios | M6, M3 |
| M8 | Troiano et al., *Hands-On Deep Learning for Finance* | root | Deep learning for trading strategies | M3, M9 |
| M9 | Klaas, *Machine Learning for Finance* | Old | Applied ML for finance: pricing, trading, and risk examples | M8, M4 |
| M10 | *Deep Learning for Multivariate Financial Time Series* ⚠ | root | Deep learning for multi-asset time series (title-only check) | M8, TS3 |
| M11 | Jansen, *Hands-On Machine Learning for Algorithmic Trading* (1st ed.) | Old | Earlier, shorter version of M3 | M3 |
| M12 | Masters, *Modern Data Mining Algorithms in C++ and CUDA* | c_plus_plus | Feature extraction and selection in C++ for data science | M1, S14 |

## Stage 5: Time-series and forecasting support

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| TS1 | Enders, *Applied Econometric Time Series* | root | ARIMA, VAR, cointegration: the classic econometrics base for pairs and regime work | TS2, S13 |
| TS2 | Elliott & Gray, *Applied Time Series Analysis with R* | root | Time-series modelling in R, with worked examples | TS1, T10 |
| TS3 | Wei, *Multivariate Time Series Analysis and Applications* | root | Multi-asset time series: VAR and cointegration in depth | TS1, M10 |
| TS4 | Joseph, *Modern Time Series Forecasting with Python* | root | Modern forecasting pipelines, including deep learning | TS5, M8 |
| TS5 | Auffarth, *Machine Learning for Time-Series with Python* | root | ML forecasting and anomaly detection | TS4, M3 |
| TS6 | Lazzeri, *Machine Learning for Time Series Forecasting with Python* | root | ML forecasting models in Python | TS5 |
| TS7 | Korstanje, *Advanced Forecasting with Python* | root | LSTM, Prophet, and DeepAR for forecasting | TS4 |
| TS8 | *Recent Advances in Time Series Forecasting* ⚠ | root | Survey of forecasting methods (title-only check) | TS4 |
| TS9 | Brownlee series (*Introduction to Time Series Forecasting*, *Deep Learning for Time Series*, *Data Preparation for ML*, *Imbalanced Classification*, *Better Deep Learning*, *ML Algorithms From Scratch*) | root, Old | Practical, code-first ML recipes: useful as reference, not for finance-specific theory | TS4, M3 |

## Stage 6: Options, volatility, and rates

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| V1 | Natenberg, *Option Volatility and Pricing* | root | Option pricing, Greeks, and volatility strategies from a trader's view | V2, V3, F8 |
| V2 | Sinclair, *Option Trading: Pricing and Volatility Strategies* | root, Old | Pricing and option strategies: a complement to V1 | V1, V4 |
| V3 | Sinclair, *Volatility Trading* (2nd ed.) | root, Old | How to forecast and trade volatility | V2, V6 |
| V4 | Sinclair, *Positional Option Trading* | root | Multi-week option strategies for retail-size accounts | V2, V3 |
| V5 | Taleb, *Dynamic Hedging* | root | Delta and gamma hedging with real-world hedging error | F10, V1 |
| V6 | *Derivatives Markets and Analysis* (Bloomberg Press, 2017) | root, Old | Derivatives market structure and products | F8, V3 |
| V7 | *Derivatives Algorithms* Vol. 1: Bones (2nd ed.) ⚠ | root | Algorithms for derivatives pricing (title-only check) | T4, C1 |
| V8 | *SABR and SABR LIBOR Market Models in Practice* | root, Old | Stochastic volatility smile models used in rates and FX | F10, V9 |
| V9 | *Listed Volatility and Variance Derivatives: A Python-based Guide* ⚠ | root, Old | Variance swaps and volatility products in Python (author not checked) | T4, V3 |
| V10 | McInerney & Zastawniak, *Stochastic Interest Rates* | root | Interest-rate models for pricing and hedging | F10, V8 |
| V11 | Donnelly, *The Art of Currency Trading* | 2020_10_08 | FX market structure and trading practice | X11, F8 |

## Stage 7: Execution, microstructure, and high-frequency trading

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| X1 | Kissell, *The Science of Algorithmic Trading and Portfolio Management* | Old, root | Transaction cost analysis, market impact, and execution algorithms (VWAP, POV) | X2, P1 |
| X2 | Kissell, *Algorithmic Trading Methods* (2020) | root (2 copies) | Newer version of X1, with ML and optimization for execution | X1, M3 |
| X3 | Leshik & Cralle, *An Introduction to Algorithmic Trading* | root, Old | Basic-to-advanced execution strategies | X1, X4 |
| X4 | Johnson, *Algorithmic Trading and DMA* | Old | Direct market access and order routing | X3, X7 |
| X5 | Aldridge, *High-Frequency Trading* (2nd ed.) | root (2 copies), Old | HFT strategies, market making, and system design | X6, X8 |
| X6 | Gregoriou, *Handbook of High Frequency Trading* | Old | Edited collection on HFT strategies and risks | X5, X7 |
| X7 | Dacorogna et al., *An Introduction to High-Frequency Finance* | Old | Tick data, microstructure, and stylized facts | X8, X5 |
| X8 | Bouchaud et al., *Trades, Quotes and Prices* | root | Market microstructure: order flow and price impact | X7, X9 |
| X9 | Cartea, Jaimungal & Penalva, *Algorithmic and High-Frequency Trading* | root | Stochastic control for market making and optimal execution | F17, X8 |
| X10 | Bernut, *Algorithmic Short-Selling with Python* | root | Long-short construction, shorting constraints, and borrow costs | P1, X1 |
| X11 | Scarpino, *Algorithmic Trading with Interactive Brokers (Python and C++)* | root, Scarpino folder | IB API order handling, market data, and indicator strategies (code examples included) | S5, X12, X13 |
| X12 | *AlgoTrading101: IB Python API, a Step-by-Step Guide* | 2020_10_08 | Practical IB API walkthrough | X11 |
| X13 | IB FIX manual, FIX Documentation Parts 1-2, IB API reference | root | FIX protocol and IB API reference for building order connectivity | X11, X14 |
| X14 | Donadio & Ghosh, *Learn Algorithmic Trading* | 2020_10_08 | Building and deploying trading systems and strategies end to end | S5, X11 |
| X15 | Donadio et al., *Developing High Frequency Trading Systems* | c_plus_plus | Building an HFT system from scratch in C++ | X5, C5, C6 |
| X16 | Ghosh, *Building Low Latency Applications with C++* | c_plus_plus | Low-latency trading ecosystem in modern C++ | X15, C8 |
| X17 | Silahian, *C++ High Performance for Financial Systems* | c_plus_plus | Efficient C++ for financial systems | X16, C10 |

## Stage 8: Software craft and C++ for quant

| ID | Book | Location | What you get | Connects to |
|---|---|---|---|---|
| E1 | Martin, *Clean Code* | 2020_10_08 | Naming, functions, and structure for maintainable code | E2, E3 |
| E2 | Fowler, *Refactoring* | 2020_10_08 | Safe restructuring of existing code | E1, E3 |
| E3 | Beck, *Test-Driven Development by Example* | 2020_10_08 | TDD workflow: red, green, refactor | E1, E2, S8 |
| E4 | Gamma et al., *Design Patterns* | c_plus_plus | Standard object-oriented patterns for trading systems | C5, E5 |
| E5 | Alexandrescu, *Modern C++ Design* | root, Old | Generic programming and policy-based design | E4, C1 |
| C1 | Duffy, *Financial Instrument Pricing Using C++* | root, Old, En 2 partes | Pricing instruments in C++, with PDE and numerical methods | F16, V1 |
| C2 | Schlögl, *Quantitative Finance: An Object-Oriented Approach in C++* | root, Old | Object-oriented pricing models in C++ | C1, C3 |
| C3 | Sengupta, *Financial Modeling Using C++* | root, Old | Financial modelling in C++ | C2, C4 |
| C4 | *Hedge Fund Modelling and Analysis: An Object-Oriented Approach Using C++* | root | Hedge fund analytics in C++ | C3, P1 |
| C5 | Joshi, *C++ Design Patterns and Derivatives Pricing* | c_plus_plus | Design patterns applied to derivatives pricing | E4, C1 |
| C6 | Oliveira, *Options and Derivatives Programming in C++20* | c_plus_plus, Old | Option pricing algorithms in modern C++ | C1, V1 |
| C7 | Oliveira, *Practical C++20 Financial Programming* | c_plus_plus | Quant problems solved in C++20 | C6, C8 |
| C8 | Hanson, *Learning Modern C++ for Finance* | c_plus_plus | Modern C++ for quantitative programming | C7, X16 |
| C9 | Peña, *Advanced Quantitative Finance with C++* | Old | Models implemented in C++ | C1, C2 |
| C10 | *Financial Numerical Recipes in C++* | c_plus_plus, Old | Numerical methods reference in C++ | F15, C11 |
| C11 | Savine, *Modern Computational Finance: AAD and Parallel Simulations* | root | Adjoint algorithmic differentiation for fast Greeks and risk | F14, C10 |
| C12 | *Computational Finance Using C and C#* | Old | Derivatives pricing and valuation in C and C# | C1, C2 |
| C13 | *Modeling Maximum Trading Profits with C++* ⚠ | root | Trading and money-management concepts in C++ (title-only check) | P6, C2 |
| C14 | *Practical C++ Financial Programming* ⚠ | Old | C++ for financial programming (title-only check) | C1, C6 |
| C15 | *C++ for Financial Mathematics*; *Introduction to C++ for Financial Engineers* ⚠ | c_plus_plus | C++ for finance math (title-only checks) | C1, C2 |
## Stage 9: Books to read, linked to the read books

Read the linked read book first, then the to-read book for a newer or deeper treatment of the same topic. The pattern is: "I'm expanding my knowledge of [read book] with [to-read book]."

### Portfolio, risk, and data

| ID | Book to read | Folder | What it adds | Expands (read) | Notes |
|---|---|---|---|---|---|
| N1 | Cajas, *Advanced Portfolio Optimization* (2025) | quant_trading | Modern optimization: risk measures, constraints, and hierarchical methods | P3, F4 | Springer, 2025 |
| N2 | Paleologo, *The Elements of Quantitative Investing* (Draft 7, 2024) | quant_trading | The full framework behind P3, as a quant investing guide | P3, P4 | Draft version |
| N3 | Noguer Alonso et al., *Quantitative Portfolio Optimization* (2025) | quant_trading | Advanced optimization techniques and applications | F4, P1 | EPUB only |
| N4 | Vorobets, *Portfolio Construction and Risk Management* | to_print | Portfolio construction and risk control, end to end | P8, P9 | Marked to print |
| N5 | Edwards, *Risk Management in Trading* (Wiley, 2014) | quant_trading | Risk limits and controls for funds and trading desks | P8, P10 | |
| N6 | Lat, *Managing Data Integrity for Finance* (2024) | quant_trading | Data quality rules: the base for backtests you can trust | T8, S2 | Finance data, not strategies |
| N7 | *PerformanceAnalytics* (R package manual) | programming | Return and risk metrics in R: Sharpe, drawdowns, attribution | P6, T10 | R reference |

### Strategy research and testing

| ID | Book to read | Folder | What it adds | Expands (read) | Notes |
|---|---|---|---|---|---|
| N8 | *Evidence-Based Technical Analysis* (Wiley, ISBN 0470008741) ⚠ | quant_trading | Statistical testing of technical rules: how to tell edge from luck | S8, S14, S18 | Author not checked |
| N9 | Pik, Chan, Broad, Sun & Singh, *Hands-On AI Trading with Python, QuantConnect, and AWS* (2023) | quant_trading | Cloud deployment of a trading system, with ML examples | S5, X11, S3 | PDF and EPUB |
| N10 | Strimpe, *Python for Algorithmic Trading Cookbook* (2024) | quant_trading | Recipes for data, backtests, and orders in Python | S5, T2 | Recipe format |
| N11 | Bisette & Van Der Post, *Next-Gen Algorithmic Trading* (2024) | quant_trading | Strategy and tooling overview in Python | S1, S3 | Independent publisher: check content |
| N12 | Van Der Post, *Quantitative Finance: Advanced Analysis with Python* (2024) | quant_trading | Quant methods in Python, from statistics to strategy | S2, F8, T2 | PDF and EPUB |
| N13 | Marti, *Decoding the Quant Market* (2023) | quant_trading | Machine learning in trading, from data to strategy | M2, S3 | AZW3 (Kindle): needs conversion |
| N14 | Krishtop, *Getting Started with Forex Trading Using Python* (2023) | quant_trading | FX backtests and orders in Python | V11, S5 | |
| N15 | *FX Derivatives Trader School* (Wiley, 2015) ⚠ | quant_trading | FX options and derivatives trading | V6, V8, V11 | Author from filename |
| N16 | Mack & Sinclair, *Retail Options Trading* (2024) | quant_trading | Options strategies for retail-size accounts | V4, V2 | |
| N17 | *Trading Volatility* ⚠ | quant_trading | Volatility trading ideas and measurement | V3 | Author not checked |
| N18 | Strauss, Bisette & Van Der Post, *The Greeks: Options Trading in Python* (2024) | quant_trading | Greeks in theory and Python code | V1, V5 | |
| N19 | Van Der Post, *Coding Black Scholes* (2024) | quant_trading | Black-Scholes and option pricing in Python | F10, T4 | EPUB |
| N20 | Kaabar, *Deep Learning for Finance* (O'Reilly, 2024) | quant_trading | Deep learning models for trading | M8, M1 | |
| N21 | *Machine Learning Trading Book* ⚠ | quant_trading | ML for trading | M3, S3 | Author not checked |
| N22 | *Deep Learning in Quantitative Trading* ⚠ | quant_trading | Deep learning for quant trading | M8, M10 | Author not checked |
| N23 | Baranasooriya, *High-Performance Algorithmic Trading Using AI* (2024) | quant_trading | AI trading algorithms and performance tuning | M3, X2 | Three copies, listed once |
| N24 | *Hydrodynamics of Markets* ⚠ | quant_trading | Market dynamics from a physics-style view | X8, X7 | Author not checked |

### Infrastructure

| ID | Book to read | Folder | What it adds | Expands (read) | Notes |
|---|---|---|---|---|---|
| N25 | Hindering, *Quant Developers' Tools and Techniques* (2023) | quant_trading | Tooling and workflows for quant developers | E3, X11, S5 | Two copies, listed once |

### Forecasting and ML support

| ID | Book to read | Folder | What it adds | Expands (read) | Notes |
|---|---|---|---|---|---|
| N26 | Manokhin, *Applied Conformal Prediction* | forecasting_ml/valeriy_manokhin | Prediction intervals with guaranteed coverage: useful for signal confidence | M1, TS4 | |
| N27 | Manokhin, *Probabilistic Forecasting with Conformal Prediction in Python* | forecasting_ml/valeriy_manokhin | Probabilistic forecasts in Python | N26, TS4 | |
| N28 | Manokhin, *Mastering Advanced Time Series Forecasting in Python* (probabilistic, hierarchical, foundation models) | forecasting_ml/valeriy_manokhin | Advanced forecasting models | TS4, TS7 | |
| N29 | Manokhin, *Mastering Modern Time Series Forecasting* (2026) | forecasting_ml/valeriy_manokhin | Modern forecasting, from statistical to deep learning | TS4, TS5 | Newer than TS4 |
| N30 | Manokhin, *Mastering Forecasting Metrics* | forecasting_ml/valeriy_manokhin | How to measure forecast accuracy | S8, TS4 | |
| N31 | Manokhin, *Mastering CatBoost* | forecasting_ml/valeriy_manokhin | Gradient boosting for tabular data, a common signal model | M3, M7 | |
| N32 | Kulkarni et al., *Time Series Algorithms Recipes* (2023) | forecasting_ml | Implementation recipes for classical and deep models | TS6, TS5 | |
| N33 | *archive.zip* and *pro_package.zip* ⚠ | forecasting_ml/valeriy_manokhin | Contents not checked; may hold more Manokhin material | TS4 | Check before use |

### Optional: interview and career prep

| ID | Book to read | Folder | What it adds | Expands (read) | Notes |
|---|---|---|---|---|---|
| N34 | Stefanica, Radoičić & Wang, *150 Most Frequently Asked Questions on Quant Interviews* (3rd ed., 2024) | interviews_career | Interview questions across the core stages | F8, V1, S8 | Optional |
| N35 | *Quant Bible* (MIT Sloan Business Club) ⚠ | interviews_career | Quant careers and interview prep | F19 | Optional, not checked |
| N36 | *Quant Finance Interview Guide* ⚠ | interviews_career | Interview prep for quant roles | F19, N34 | Optional, not checked |

### Duplicates and exclusions

- **Same book as a printed read book (listed once, not added again):** Donadio et al., *Developing High Frequency Trading Systems* (the read book X15); Hanson, *Learning Modern C++ for Finance* (C8); Kakushadze, `151_trading_strategies.pdf` (S11); Joseph, *Modern Time Series Forecasting with Python* (TS4, in `forecasting_ml/`).
- **Left out as not quant or algo trading:** the rest of `programming/` (Python basics, LLM agents, blockchain, generic C++ books), the career documents and Pfeffer's *7 Rules of Power* in `interviews_career/`, and the non-trading material in `other/`. Files in `other/` that aren't books (a currency-pair portfolio PDF, a course catalog) were not opened.

## Suggested reading order

1. **Foundations:** F1, F5, F9, F10, then F14 (Monte Carlo).
2. **Tooling:** T1, T2, T10 (for R), then T8 and T9.
3. **Build a system:** S1, S2, S8, S14, S18. Learn to test first.
4. **Portfolios and risk:** P3, P4, P6, P9, then P7 for sizing.
5. **ML signals:** M1 first, then M2, M3, M4. Use TS1 and TS2 if you need econometrics.
6. **Options and volatility:** V1, V2, V3, V5, then V8 for smile models.
7. **Execution and HFT:** X1, X3, X5, X8, X9, then X11 and X13 for the IB build.
8. **Production C++:** E3, E1, then C1, C6, X15, X16.

## Main interconnections

- **Testing spine:** S8 (robustness) to S14 (permutation tests) to S18 (a worked example) to M1 (overfitting in ML). These four books should be read together.
- **Portfolio spine:** F4 (convex optimization) to P3 (portfolio management) to P4 (active management theory) to M2 (HRP) to P7 (Kelly sizing).
- **Execution spine:** F17 (stochastic control) to X9 (market making) to X1 (transaction costs) to X11 (IB build) to X15 (C++ HFT).
- **Pricing spine:** F8 to F9/F10 to V1 (options) to C1 (C++ implementation) to C11 (AAD for risk).

## Printed but not in the map

These are in `books_printed/` but are outside quant or algo trading, so they are not mapped:

- **CFA:** all of `CFA Level II/` (excluded by your instruction).
- **General finance and economics:** Fabozzi *Fixed Income Handbook*, *Animal Spirits*, Excel finance and accounting books (*Aplicaciones financieras de Excel*, *Excel para Contadores*, *Excel aplicado a la auditoría*, Goldmeier), *Thirty Days of FOREX Trading* (Horner), *Bariviera 2020* (crypto paper), and the IB Excel add-in C/C++ book.
- **Non-finance:** *Principles of Neural Science*, *Focus* (Goleman), *Never Split the Difference* (Voss), *The Definitive Book of Body Language*, *How to Read a Person Like a Book*, *The Dichotomy of Leadership*, the psychoanalysis book, *Linux Kernel Debugging*, and *Productive and Efficient Data Science with Python*.
- **General programming and C++ (not trading-specific):** Prata's *C++ Primer Plus* and *C Primer Plus*, Meyers' *Effective C++* and *Effective Modern C++*, Vandevoorde's *C++ Templates*, Sutter's *Exceptional C++ Style*, Grimm's C++ books, Williams' *C++ Concurrency in Action*, Koenig & Moo's *Accelerated C++*, Cukic's *Functional Programming in C++*, Boost, and the Standard Library.
- **GPU and parallel computing (not mapped):** the CUDA programming guide, the CUDA books (Tuomanen, Soyata, Han & Sharma), and Matloff's parallel computing book.
- **Math not tied to trading:** Gallier's *Linear Algebra for Computer Vision, Robotics, and ML*. The probability books F5 to F7 stay in the map only because stochastic calculus needs them.

## Verification still needed

Titles marked ⚠ have no readable text layer or unclear content. Check them before relying on them: `Quantitative_Trading.pdf` and `Quantitative_Trading_pic.pdf` (both 203 pages, no text), `Derivatives Algorithms Vol. 1`, `Recent Advances in TS Forecasting`, `Deep Learning for Multivariate Financial TS`, `Modeling Maximum Trading Profits with C++`, and the to-read entries N8, N15, N17, N21, N22, N24, N33, N35, and N36 (author or contents not checked). Entries N2, N9, N11, N13, and N23 need a quick check of edition or publisher before you rely on them.
