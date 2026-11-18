# Algo Trading Map: Roadmap

This map covers the quant and algo trading books I have read, and the ones I still plan to read. Read books are arranged in stages from foundations to production. Books still to read are in the later sections. Each one names the read books it complements. The Role tracks section gives a core and an additional list for each role: quant researcher, quant trader, and quant developer.

## How to read this map

- **Stages** run from foundations to production. Read them in order, but you can skip ahead once you have the prerequisites.
- **IDs** (F8, S3, X1...) are used in the "Connects to" column. A link can point to a book in the to-read sections; those IDs are kept so cross-references still work.
- **Core to-read books** keep their original IDs (F1, S14, M4...). **N-IDs** (N1 to N36) are additional books to read.
- **Read with:** for each to-read book, the read books it complements.
- **Scope:** entries are described from each book's title and well-known scope. Some have not been checked against the full text, so treat them as a starting point.

## Stage 0: Foundations (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| F8 | Stefanica, *A Primer for the Mathematics of Financial Engineering* | Intermediate | None | The math used in pricing, written for finance practitioners: bond and rate basics, option payoffs, Brownian motion, and how probability turns into pricing formulas. It bridges the probability books and the derivatives books. | F9, V1, V5 |
| F9 | Shreve, *Stochastic Calculus for Finance I: The Binomial Asset Pricing Model* | Advanced | None | Discrete-time pricing on the binomial model: replication, no-arbitrage pricing, and the risk-neutral measure. Learn it before the continuous-time model, because every later pricing argument reuses the same idea. | F10, F8, V1 |
| F10 | Shreve, *Stochastic Calculus for Finance II: Continuous-Time Models* | Advanced | None | Continuous-time models: Brownian motion, Itô's lemma, and the derivation of Black-Scholes. This is the main theory behind option pricing and hedging, and behind the Monte Carlo work in later stages. | F9, F11, V5 |
| F19 | Wilmott, *Frequently Asked Questions in Quantitative Finance*; *Paul Wilmott on Quantitative Finance* Vol. 1-3 | Intermediate | None | A broad, applied reference set covering derivatives, models, and numerical methods, written as practical questions and answers. Good for filling gaps and for interview-style questions. | F8, V1 |

## Stage 1: Python and R tooling (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| T1 | Yan, *Python for Finance* | Beginner | Python | Building financial applications in Python: time value of money, return and risk statistics, and simple pricing and portfolio models. It covers the finance code basics in one place. | T2, T5 |
| T2 | Hilpisch, *Python for Finance* (2019, *Mastering Data-Driven Finance*) | Intermediate | Python | Financial data in Python, from data retrieval and time-series analysis to option pricing and simple risk measures. It covers the Python workflow the later quant books assume. | T1, T4, M3 |
| T3 | Hilpisch, *Artificial Intelligence in Finance* | Advanced | Python | ML and deep learning applied to finance, with Python examples. It shows how neural networks are used for prediction, pricing, and hedging. | T2, M3, M4 |
| T4 | Hilpisch, *Derivatives Analytics with Python* | Intermediate | Python | Option pricing and risk in Python: Black-Scholes, Monte Carlo simulation, and volatility surfaces. Useful when you want to price and hedge your own option models. | T2, V1, V7 |
| T5 | *Mastering Python for Finance* | Intermediate | Python | Python for financial models and data analysis: data handling, portfolio statistics, and simple pricing. A second Python-for-finance reference to compare with T1 and T2. | T1, T2 |
| T6 | Lachowicz, *Python for Quants* Vol. I | Intermediate | Python | Python workflows for quantitative work: data handling, numerical methods, and model code. Scope not checked against the text yet. | T2, T5 |
| T7 | Fletcher & Gardner, *Financial Modelling in Python* | Intermediate | Python | Building financial models in Python: pricing, yield curves, and risk measures, with attention to how each model is built. | T2, F8 |
| T8 | *Mastering Pandas for Finance* | Intermediate | Python | Using pandas on financial data: time-series indexing, resampling, cleaning messy price data, and aligning several series. Most backtest errors start with bad data, so this comes early. | T9, T2 |
| T9 | McKinney, *Python for Data Analysis* (2nd ed.) | Beginner | Python | The standard reference for pandas and NumPy: data structures, cleaning, grouping, and time series. Read it as the base for T8. | T8 |
| T10 | Berlinger, *Mastering R for Quantitative Finance* | Intermediate | R | Using R for backtests, portfolio optimization, and risk models, with worked examples. A good alternative to Python if you prefer R's statistics tools. | T11, TS2 |
| T11 | *Financial Risk Modelling and Portfolio Optimization with R* (2nd ed.) | Intermediate | R | Risk models and portfolio optimization in R: value at risk, expected shortfall, and optimization under constraints. It extends T10 toward risk management. | T10, P3 |
| T12 | Fantazzini, *Quantitative Finance with R and Cryptocurrencies* (slides) | Intermediate | R | Lecture slides on R-based time-series and risk modelling for crypto assets, with the statistical models behind them. A compact reference rather than a full book. | T10, TS1 |
| T13 | *Introduction to Python for Econometrics* | Intermediate | Python | Econometrics in Python: regression, time-series models, and how to test statistical assumptions. It gives the statistical base for the time-series books. | TS1, T9 |
| T14 | Raschka, *Python Machine Learning* (2017) | Beginner | Python | A scikit-learn workflow: preprocessing, classifiers, model evaluation, and cross-validation. A practical start for the ML books in Stage 4. | M3, M1 |
| T15 | *Python Basics Handbook* | Beginner | Python | A short Python syntax refresher for readers new to the language. Skip it if you already code in Python. | T1 |

## Stage 2: Building and testing a trading system (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| S1 | Chan, *Algorithmic Trading: Winning Strategies and Their Rationale* (2013) | Beginner | MATLAB | Why momentum and mean-reversion strategies work, and how to test the rationale before trusting a backtest. Chan writes about strategy logic more than code, which makes it a good first trading book. | S2, S3, S4 |
| S2 | Chan, *Quantitative Trading* (2nd ed., 2021) | Intermediate | MATLAB | How to build a backtest, then use regression, Kalman filters, and position sizing, and set up a small trading business. The practical companion to S1. | S1, S3, N12 |
| S3 | Chan, *Machine Trading* (2017) | Advanced | MATLAB | An ML-based trading pipeline end to end: data preparation, feature selection, model choice, and realistic transaction costs. It links the strategy ideas in S1 to the ML books. | S2, M1, M3 |
| S4 | Chan, *Quantitative Trading: How to Build Your Own Algorithmic Trading Business* (first edition) | Intermediate | MATLAB | The earlier version of S2, with the same core ideas and fewer updates. Read S2 instead unless you want to compare editions. | S2 |
| S5 | Halls-Moore, *Successful Algorithmic Trading* | Intermediate | Python | Building a trading system the QuantStart way: data handling, an event-driven backtest, and connecting to Interactive Brokers for execution. A first end-to-end build. | S6, S8, X11 |
| S6 | Halls-Moore, *Advanced Algorithmic Trading* | Advanced | Python | An event-driven backtester in depth, with strategy testing and live execution. It builds on S5 with a more complete system. | S5, X11 |
| S7 | Halls-Moore, *C++ for Quantitative Finance* | Advanced | C++ | The same QuantStart workflow written in C++: a backtester, data handling, and execution. Read it with C4 or C6 if you want the C++ version. | S5, C4, C6 |
| S8 | Davey, *Building Winning Algorithmic Trading Systems* | Intermediate | None | Testing whether a system is robust: walk-forward tests, Monte Carlo resampling, and avoiding overfitting. The main reference for judging a backtest before risking money. | S9, N8, N25 |
| S9 | Davey, *Algo Trading Cheat Codes* (2021) | Beginner | None | A shorter, practical version of S8, with the key tests and rules in less space. Use it as a checklist after S8. | S8 |
| S10 | Conlan, *Automated Trading with R* | Intermediate | R | An end-to-end R platform for research and execution: data, backtests, and order routing. A way to build the S5 workflow in R. | T10, S5 |
| S11 | Kakushadze & Serur, *151 Trading Strategies* | Intermediate | None | A catalog of strategy ideas across asset classes, with the logic behind each. Use it to generate hypotheses to test, not as a list of ready-made trades. | S1, S2 |
| S12 | *The Ultimate Algorithmic Trading System Toolbox* | Intermediate | None | A toolkit for developing trading systems: rules, testing, and money-management components. Scope not checked against the text yet. | S8, N25 |
| S13 | Ehrman, *The Handbook of Pairs Trading* | Intermediate | None | Pairs selection, spread construction, and trading pairs with equities, options, and futures. The practical base for pairs strategies. | S21, TS1 |
| S16 | Chen & Tsang, *Detecting Regime Change in Computational Finance* | Advanced | Varies | How to detect regime shifts in market data and switch strategies when the regime changes. Pairs well with the time-series books. | M3, S1, TS1 |
| S21 | Sarmento & Horta, *A Machine Learning Based Pairs Trading Investment Strategy* | Advanced | Python | A complete ML pairs-trading strategy, from pair selection to signal and backtest. A worked example that links S13 to the ML books. | S13, M1 |

## Stage 3: Portfolio construction and risk (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| P2 | *Statistical Arbitrage Algorithmic Trading: Insights and Techniques* | Advanced | Varies | Statistical arbitrage methods: finding relationships between assets and trading them as a portfolio. Author not checked yet; treat it as a summary of stat-arb ideas. | P4, S13 |
| P4 | Grinold & Kahn, *Advances in Active Portfolio Management* | Advanced | None | The fundamental law of active management: how signal quality (information coefficient) and breadth turn into portfolio return. The key framework for judging whether a strategy can earn money after costs. | P9, M1 |
| P5 | Gray & Vogel, *Quantitative Momentum* | Intermediate | None | A practical momentum stock-selection system: ranking stocks, rebalancing, and testing the rules. A concrete example of applying the ideas in S1 to equities. | S1, P4 |
| P6 | Vince, *The Mathematics of Money Management* | Intermediate | None | Optimal f, position sizing, and risk of ruin: how the size of each trade decides whether a system survives. The reference for sizing decisions. | P7, S8 |
| P9 | Burns, *The Ultimate Trading Risk Management Guide* | Beginner | None | Practical risk rules: stop-losses, drawdown limits, and position-level controls. A checklist-style complement to the sizing theory in P6. | P6, P4 |

## Stage 4: Machine learning for trading signals (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| M1 | López de Prado, *Advances in Financial Machine Learning* | Advanced | Python | Labeling financial data, purged cross-validation, meta-labeling, and bet sizing. The core reference for avoiding leakage in ML trading models. | M2, S8, M3 |
| M2 | López de Prado, *Machine Learning for Asset Managers* | Advanced | Python | Clustering, denoising covariance matrices, and Hierarchical Risk Parity for building portfolios. A shorter, portfolio-focused companion to M1. | M1, P4 |
| M3 | Jansen, *Machine Learning for Algorithmic Trading* (2nd ed.) | Intermediate | Python | An end-to-end ML alpha pipeline: alternative data, features, model training, and backtests, with notebooks. The most practical ML-for-trading book on this list. | M1, S3, T3 |
| M6 | Karasan, *Machine Learning for Financial Risk Management with Python* | Intermediate | Python | ML models for credit, market, and operational risk, in Python. It shows how ML is used on the risk side of a fund rather than for trading signals. | P9, M3 |
| M9 | Klaas, *Machine Learning for Finance* | Intermediate | Python | Applied ML across pricing, trading, and risk, with worked examples. A broad survey that connects the other ML books. | M8, M1 |
| M11 | Jansen, *Hands-On Machine Learning for Algorithmic Trading* (1st ed.) | Intermediate | Python | The earlier, shorter edition of M3, with the same pipeline ideas. Read M3 first and use M11 for comparison. | M3 |

## Stage 5: Time-series and forecasting (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| TS1 | Enders, *Applied Econometric Time Series* | Advanced | None | ARIMA, VAR, unit roots, and cointegration: the classic econometric base for pairs trading and regime models. | TS2, S13 |
| TS2 | Elliott & Gray, *Applied Time Series Analysis with R* | Intermediate | R | Time-series modelling in R with worked examples: stationarity tests, ARIMA, and forecasting. The R counterpart to TS1. | TS1, T10 |
| TS3 | Wei, *Multivariate Time Series Analysis and Applications* | Advanced | R | Models for several series at once: VAR, cointegration, and multivariate forecasting. Relevant to multi-asset strategies. | TS1, M9 |
| TS4 | Joseph, *Modern Time Series Forecasting with Python* | Intermediate | Python | Modern forecasting pipelines, from statistical baselines to deep learning, with Python code. The base for the forecasting books on the to-read list. | TS5, TS7 |
| TS5 | Auffarth, *Machine Learning for Time-Series with Python* | Intermediate | Python | ML for forecasting and anomaly detection: feature engineering for time series and how to evaluate it. | TS4, M3 |
| TS6 | Lazzeri, *Machine Learning for Time Series Forecasting with Python* | Intermediate | Python | ML forecasting models in Python: lag features, model selection, and evaluation. | TS5 |
| TS7 | Korstanje, *Advanced Forecasting with Python* | Intermediate | Python | LSTM, Prophet, and DeepAR, with the code and the trade-offs between them. | TS4 |

## Stage 6: Options, volatility, and FX (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| V1 | Natenberg, *Option Volatility and Pricing* | Intermediate | None | Option pricing, the Greeks, and volatility strategies from a trader's point of view: what a position gains or loses as price and volatility move. | V2, V3, F8 |
| V2 | Sinclair, *Option Trading: Pricing and Volatility Strategies* | Intermediate | None | Option pricing and strategy selection, with a focus on where the pricing edge comes from. A complement to V1 with a more practical approach. | V1, V4 |
| V3 | Sinclair, *Volatility Trading* (2nd ed.) | Advanced | None | Forecasting volatility, comparing it with implied volatility, and trading the difference. The main book on volatility as a trading edge. | V2, V9 |
| V4 | Sinclair, *Positional Option Trading* | Intermediate | None | Multi-week option strategies for smaller accounts, with risk management built in. | V2, V3 |
| V9 | *Listed Volatility and Variance Derivatives: A Python-based Guide* | Advanced | Python | Variance swaps and volatility products, priced and analyzed in Python. Author not checked yet. | T4, V3 |
| V11 | Donnelly, *The Art of Currency Trading* | Beginner | None | How the FX market is structured and how professionals trade it. Useful before FX strategies, so the market mechanics are clear first. | X11, F8 |

## Stage 7: Execution and microstructure (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| X1 | Kissell, *The Science of Algorithmic Trading and Portfolio Management* | Advanced | None | Transaction cost analysis, market impact models, and execution algorithms such as VWAP and POV. The base for judging whether a strategy survives trading costs. | X2, S8 |
| X2 | Kissell, *Algorithmic Trading Methods* (2020) | Advanced | None | A newer version of X1, with ML and optimization applied to execution. Read it after X1. | X1, M3 |
| X3 | Leshik & Cralle, *An Introduction to Algorithmic Trading* | Beginner | None | Execution strategies from basic to advanced, with a clear explanation of order types. A gentle introduction before X1. | X1, X4 |
| X4 | Johnson, *Algorithmic Trading and DMA* | Intermediate | None | Direct market access, order routing, and how brokers and exchanges handle orders. Useful when building order logic for IB. | X3, X11 |
| X8 | Bouchaud et al., *Trades, Quotes and Prices* | Advanced | None | Market microstructure: order flow, the limit order book, and price impact. The main book on how prices move at the trade level. | X1, X2 |
| X11 | Scarpino, *Algorithmic Trading with Interactive Brokers (Python and C++)* | Intermediate | Python, C++ | The IB API for orders, market data, and indicator-based strategies, with code examples in Python and C++. The practical link between a strategy and a broker. | S5, X12, X13 |
| X12 | *AlgoTrading101: IB Python API, a Step-by-Step Guide* | Beginner | Python | A step-by-step walkthrough of the IB Python API: connecting, requesting data, and placing orders. A quick companion to X11. | X11 |
| X13 | IB FIX manual, FIX Documentation Parts 1-2, and IB API reference | Advanced | None | The FIX protocol and IB's API reference for order messages and connectivity. Read it when you need to understand order messages beyond the Python wrapper. | X11, X14 |
| X14 | Donadio & Ghosh, *Learn Algorithmic Trading* | Intermediate | Python | Building and deploying trading systems and strategies end to end, with the software architecture around them. It connects strategy code to a running system. | S5, X11 |

## Stage 8: C++ for quantitative finance (read)

| ID | Book | Level | Code language | What you get | Connects to |
| --- | --- | --- | --- | --- | --- |
| C4 | *Hedge Fund Modelling and Analysis: An Object-Oriented Approach Using C++* | Advanced | C++ | Hedge-fund analytics in C++: object models for instruments, portfolios, and risk measures. It shows how C++ classes can model a whole fund's positions. | C6, C7 |
| C6 | Oliveira, *Options and Derivatives Programming in C++20* | Advanced | C++ | Option pricing algorithms in modern C++20: binomial trees, Monte Carlo, and the code structure behind them. | C7, V1 |
| C7 | Oliveira, *Practical C++20 Financial Programming* | Advanced | C++ | Quant problems solved in C++20: numerical methods, data structures, and the performance choices that matter in finance. | C6, C15 |
| C15 | *C++ for Financial Mathematics*; *Introduction to C++ for Financial Engineers* | Advanced | C++ | C++ for the math of finance: numerical methods and object-oriented design for pricing. Titles checked; contents not yet verified. | C6, C7 |

## Still to read: core books

These are core books I have not read yet. Each one names the read books it complements.

| ID | Book | Level | Code language | What you get | Read with |
| --- | --- | --- | --- | --- | --- |
| F1 | Strang, *Introduction to Linear Algebra* (5th ed.) and solutions manual | Beginner | None | Matrices, vector spaces, eigenvalues, and least squares. This is the math behind covariance matrices and factor models, which the portfolio books rely on. | P4, P5 |
| F2 | Axler, *Linear Algebra Done Right* | Intermediate | None | A proof-based treatment of linear algebra that avoids determinants. Read it if F1's procedures feel unmotivated. | P4 |
| F3 | Gallier & Quaintance, *Fundamentals of Optimization Theory with Applications to Machine Learning* | Advanced | None | Convex sets, duality, and KKT conditions: the optimization theory behind constrained portfolio problems. | P4, P6 |
| F4 | Boyd & Vandenberghe, *Convex Optimization* | Advanced | None | The standard reference for convex problems and solvers, with many finance examples such as portfolio optimization. | T11, P9 |
| F5 | Grimmett & Stirzaker, *Probability and Random Processes* | Intermediate | None | Probability, Markov chains, and random walks: the base for return models and for the probability used in stochastic calculus. | F8, F9 |
| F6 | Billingsley, *Probability and Measure* | Advanced | None | Measure-theoretic probability, the formal foundation under the stochastic calculus books. Dense; use it as a reference. | F9 |
| F7 | Jacod & Protter, *Probability Essentials* | Advanced | None | A compact probability toolkit before stochastic calculus: measures, random variables, and conditional expectation. | F9, F10 |
| F11 | Arguin, *A First Course in Stochastic Calculus* | Advanced | None | A more intuitive route to Itô calculus than the Shreve books, reaching the same core results. | F10 |
| F12 | Mikosch, *Elementary Stochastic Calculus with Finance in View* | Advanced | None | A compact, pricing-oriented treatment of stochastic calculus: Brownian motion, stochastic integrals, and Black-Scholes. | F10 |
| F13 | Protter, *Stochastic Integration and Differential Equations* | Advanced | None | The rigorous reference for stochastic integrals and SDEs. Advanced; read it after F10 and F12. | F9, F10 |
| F14 | Glasserman, *Monte Carlo Methods in Financial Engineering* | Advanced | None | Monte Carlo pricing, variance reduction, and Greeks by simulation. The main reference for simulation-based pricing and risk. | F10, T4 |
| F15 | Kloeden & Platen, *Numerical Solution of Stochastic Differential Equations* | Advanced | None | Numerical schemes for SDEs: how to simulate the paths that Monte Carlo pricing depends on. | F10 |
| F16 | Duffy, *Numerical Methods in Computational Finance* (PDE/FDM) | Advanced | None | Finite-difference (PDE) pricing: the alternative to Monte Carlo for many option problems. | F10, V1 |
| F17 | Kushner & Dupuis, *Numerical Methods for Stochastic Control Problems in Continuous Time* | Advanced | None | Stochastic control and its numerical methods: the math behind optimal execution and market making. | X1, X8 |
| F18 | Wilmott, *Paul Wilmott Introduces Quantitative Finance* | Intermediate | None | A broad, applied introduction to derivatives and quant methods, with less math than F19. | F8, V1 |
| S14 | Masters, *Testing and Tuning Market Trading Systems: Algorithms in C++* | Advanced | C++ | Monte Carlo permutation tests and tuning without overfitting: how to test whether a system's result could be luck. | S8, S9 |
| S15 | Tulchinsky et al., *Finding Alphas* | Advanced | None | How alpha research works in practice: generating an idea, testing it, and combining signals. Written by practitioners who run alpha research. | P4, M2 |
| S17 | Guo, Lai, Shek & Wong, *Quantitative Trading: Algorithms, Analytics, Data, Models, Optimization* | Intermediate | None | A broad quant trading reference covering algorithms, data, and optimization. Contents not checked yet. | S2, P2 |
| S18 | Zeng, *A Comprehensive Reliability Test of Technical Trading Strategies* (MSc thesis, 2019) | Intermediate | Varies | Statistical tests on technical trading rules: a worked example of checking whether a rule's results are reliable. | S8, S9 |
| S19 | Doloc, *Applications of Computational Intelligence in Data-Driven Trading* | Advanced | Varies | Computational-intelligence methods for trading signals. Scope not checked. | M3, S16 |
| S20 | Lee, *Quantum Finance: Intelligent Forecast and Trading Systems* | Advanced | Varies | Forecasting and trading systems using quantum-inspired methods. Scope not checked; treat it as a survey. | S16, M3 |
| P1 | Isichenko, *Quantitative Portfolio Management: The Art and Science of Statistical Arbitrage* | Advanced | Varies | Statistical arbitrage end to end: factor models, portfolio construction, and implementation. | P2, P4 |
| P3 | Paleologo, *Advanced Portfolio Management: A Quant's Guide for Fundamental Investors* | Advanced | Varies | Turning alphas into portfolios: risk models, constraints, and transaction costs, for readers coming from fundamental investing. | P4, P9 |
| P7 | *The Kelly Capital Growth Investment Criterion: Theory and Practice* | Intermediate | None | Kelly sizing in theory and practice: why it maximizes long-run growth, and why fractional Kelly is used given estimation error. | P6, S8 |
| P8 | Harvey, Rattray & Van Hemert, *Strategic Risk Management* | Intermediate | None | Portfolio-level risk budgeting and design: how to allocate risk across strategies and asset classes. | P9, P6 |
| P10 | Nash, *Effective Product Control: Controlling for Trading Desks* | Intermediate | None | How a trading desk controls P&L, limits, and reconciliation. The operational side of running a book. | P9, X11 |
| M4 | Dixon, Halperin & Bilokon, *Machine Learning in Finance: From Theory to Practice* | Advanced | Python | ML for pricing, risk, and trading, with the theory behind each method. A more formal companion to M1. | M1, M3 |
| M5 | Nagel, *Machine Learning in Asset Pricing* | Advanced | Python | ML for return prediction and the factor zoo: which signals survive, and how to test them. | M2, P4 |
| M7 | Nokeri, *Implementing Machine Learning for Finance* | Intermediate | Python | Predictive risk and performance analysis for portfolios, using ML pipelines. | M6, M3 |
| M8 | Troiano et al., *Hands-On Deep Learning for Finance* | Advanced | Python | Deep learning for trading strategies, with worked examples. | M3, M9 |
| M10 | *Deep Learning for Multivariate Financial Time Series* | Advanced | Python | Deep learning for multi-asset time series. Author not checked. | M9, TS3 |
| M12 | Masters, *Modern Data Mining Algorithms in C++ and CUDA* | Advanced | C++ | Feature extraction and selection in C++: the data-mining algorithms behind many ML models. | M1, M3 |
| TS8 | *Recent Advances in Time Series Forecasting* | Advanced | Python | A survey of forecasting methods. Scope not checked. | TS4, TS7 |
| TS9 | Brownlee series (*Introduction to Time Series Forecasting*, *Deep Learning for Time Series*, *Data Preparation for ML*, *Imbalanced Classification*, *Better Deep Learning*, *ML Algorithms From Scratch*) | Intermediate | Python | Code-first ML recipes: time-series forecasting, data preparation, imbalanced data, and deep learning. General rather than finance-specific; useful as a reference. | TS4, M3 |
| V5 | Taleb, *Dynamic Hedging* | Advanced | None | Delta and gamma hedging with real-world hedging error: why hedges fail when markets jump. | V1, F10 |
| V6 | *Derivatives Markets and Analysis* (Bloomberg Press, 2017) | Intermediate | None | The structure of derivatives markets and their products: futures, options, and swaps. | V3, F8 |
| V7 | *Derivatives Algorithms* Vol. 1: Bones (2nd ed.) | Advanced | C++ | Algorithms for derivatives pricing. Contents not checked. | T4, V1 |
| V8 | *SABR and SABR LIBOR Market Models in Practice* | Advanced | None | The SABR stochastic-volatility model for the volatility smile, and its use in rates and FX. | V1, V9 |
| V10 | McInerney & Zastawniak, *Stochastic Interest Rates* | Advanced | None | Interest-rate models for pricing and hedging, with the stochastic calculus behind them. | V1, F10 |
| X5 | Aldridge, *High-Frequency Trading* (2nd ed.) | Intermediate | None | HFT strategies, market making, and system design, from a practitioner's point of view. | X1, X8 |
| X6 | Gregoriou, *Handbook of High Frequency Trading* | Intermediate | None | An edited collection on HFT strategies and their risks. | X1, X8 |
| X7 | Dacorogna et al., *An Introduction to High-Frequency Finance* | Advanced | None | Tick data, microstructure, and stylized facts: how high-frequency data behaves. | X8 |
| X9 | Cartea, Jaimungal & Penalva, *Algorithmic and High-Frequency Trading* | Advanced | None | Stochastic control for market making and optimal execution. | X1, X8 |
| X10 | Bernut, *Algorithmic Short-Selling with Python* | Intermediate | Python | Long-short construction, shorting constraints, and borrow costs. | X1, S13 |
| X15 | Donadio et al., *Developing High Frequency Trading Systems* | Advanced | C++ | Building an HFT system from scratch in C++: order handling, market data, and low-latency design. | X11, X14 |
| X16 | Ghosh, *Building Low Latency Applications with C++* | Advanced | C++ | A low-latency trading ecosystem in modern C++, from data feeds to order handling. | X14, C6 |
| X17 | Silahian, *C++ High Performance for Financial Systems* | Advanced | C++ | Efficient C++ for financial systems: memory, concurrency, and profiling. | C4, X14 |
| E1 | Martin, *Clean Code* | Beginner | Varies | Naming, functions, and structure for maintainable code. Strategy code is reviewed and changed often, so this matters. | S5, X14 |
| E2 | Fowler, *Refactoring* | Intermediate | Varies | Safe restructuring of existing code, using tests to change it without breaking behaviour. | S5, X11 |
| E3 | Beck, *Test-Driven Development by Example* | Intermediate | Java | The TDD cycle: write a failing test, make it pass, then refactor. Useful for backtest code, where a bug can look like a profit. | S8, S5 |
| E4 | Gamma et al., *Design Patterns* | Intermediate | C++ | Standard object-oriented patterns such as strategy, observer, and factory, applied to trading systems. | C4, C6 |
| E5 | Alexandrescu, *Modern C++ Design* | Advanced | C++ | Generic programming and policy-based design in C++. Advanced; for C++ systems design. | C4, C6 |
| C1 | Duffy, *Financial Instrument Pricing Using C++* | Advanced | C++ | Pricing instruments in C++, combining PDE and numerical methods. | C4, V1 |
| C2 | Schlögl, *Quantitative Finance: An Object-Oriented Approach in C++* | Advanced | C++ | Object-oriented pricing models in C++. | C4, C6 |
| C3 | Sengupta, *Financial Modeling Using C++* | Advanced | C++ | Financial modelling in C++, with class design for instruments and models. | C4, C7 |
| C5 | Joshi, *C++ Design Patterns and Derivatives Pricing* | Advanced | C++ | Design patterns applied to derivatives pricing: how to structure a pricing library. | C6, E4 |
| C8 | Hanson, *Learning Modern C++ for Finance* | Intermediate | C++ | Modern C++ for quantitative programming, from language features to finance code. | C6, C7 |
| C9 | Peña, *Advanced Quantitative Finance with C++* | Advanced | C++ | Models implemented in C++, with the numerical code behind them. | C6, C15 |
| C10 | *Financial Numerical Recipes in C++* | Intermediate | C++ | A numerical methods reference in C++: root finding, integration, and random numbers. | C6, C7 |
| C11 | Savine, *Modern Computational Finance: AAD and Parallel Simulations* | Advanced | C++ | Adjoint algorithmic differentiation (AAD) for fast Greeks and risk, plus parallel simulation. | T4, F14 |
| C12 | *Computational Finance Using C and C#* | Intermediate | C, C# | Derivatives pricing and valuation in C and C#. | C6, C15 |
| C13 | *Modeling Maximum Trading Profits with C++* | Intermediate | C++ | Trading and money-management concepts in C++. Scope not checked. | P6, C4 |
| C14 | *Practical C++ Financial Programming* | Intermediate | C++ | C++ for financial programming. Scope not checked. | C6, C7 |

## Still to read: additional books

These are additional books I still plan to read. Each one names the read books it complements.

| ID | Book | Level | Code language | What it adds | Read with |
| --- | --- | --- | --- | --- | --- |
| N1 | Cajas, *Advanced Portfolio Optimization* (2025) | Advanced | Python | Modern portfolio optimization with several risk measures, constraints, and hierarchical methods. An updated treatment of the optimization ideas in P4. | P4, P9 |
| N2 | Paleologo, *The Elements of Quantitative Investing* (Draft 7, 2024) | Advanced | Varies | The full framework behind a quant portfolio: signals, risk, and implementation, written as a practical guide. Draft version. | P4, P9 |
| N3 | Noguer Alonso et al., *Quantitative Portfolio Optimization* (2025) | Advanced | Varies | Advanced optimization techniques with applications across asset classes. EPUB only. | T11, P2 |
| N4 | Vorobets, *Portfolio Construction and Risk Management* | Intermediate | None | Portfolio construction and risk control end to end, from alpha to position size. Marked to print. | P9, P6 |
| N5 | Edwards, *Risk Management in Trading* (Wiley, 2014) | Intermediate | None | Risk limits, controls, and governance for funds and trading desks. | P9, P6 |
| N6 | Lat, *Managing Data Integrity for Finance* (2024) | Intermediate | Varies | Data quality rules for finance: validation, lineage, and checks that catch bad data before it corrupts a backtest. | T8, S2 |
| N7 | *PerformanceAnalytics* (R package manual) | Intermediate | R | Return and risk metrics in R: Sharpe ratio, drawdowns, and performance attribution. | P6, T10 |
| N8 | *Evidence-Based Technical Analysis* (Wiley, ISBN 0470008741) | Intermediate | Varies | Statistical testing of technical rules, to separate real edge from luck. Author not checked. | S8, S9 |
| N9 | Pik, Chan, Broad, Sun & Singh, *Hands-On AI Trading with Python, QuantConnect, and AWS* (2023) | Intermediate | Python | Deploying a trading system on the cloud, with ML examples and the QuantConnect platform. | S5, X11 |
| N10 | Strimpe, *Python for Algorithmic Trading Cookbook* (2024) | Beginner | Python | Recipes for market data, backtests, and orders in Python. Quick to use as a reference. | S5, T2 |
| N11 | Bisette & Van Der Post, *Next-Gen Algorithmic Trading* (2024) | Intermediate | Python | A strategy and tooling overview in Python. Published by an independent press, so check its content against S1 and S3 first. | S1, S3 |
| N12 | Van Der Post, *Quantitative Finance: Advanced Analysis with Python* (2024) | Intermediate | Python | Quant methods in Python, from statistics to strategy design. | S2, F8, T2 |
| N13 | Marti, *Decoding the Quant Market* (2023) | Intermediate | Python | ML in trading, from data to strategy. Available as AZW3 (Kindle) only; needs conversion. | M2, S3 |
| N14 | Krishtop, *Getting Started with Forex Trading Using Python* (2023) | Beginner | Python | FX backtests and orders in Python. | V11, S5 |
| N15 | *FX Derivatives Trader School* (Wiley, 2015) | Intermediate | None | FX options and derivatives trading. Author taken from the filename; not checked against the text. | V11, V1 |
| N16 | Mack & Sinclair, *Retail Options Trading* (2024) | Beginner | None | Options strategies for retail-size accounts, and the risk limits that matter at that size. | V4, V2 |
| N17 | *Trading Volatility* | Beginner | None | Volatility trading ideas and how to measure them. Author not checked. | V3, V2 |
| N18 | Strauss, Bisette & Van Der Post, *The Greeks: Options Trading in Python* (2024) | Intermediate | Python | The Greeks in theory and in Python code: delta, gamma, vega, and theta, and how they change a position. | V1, T4 |
| N19 | Van Der Post, *Coding Black Scholes* (2024) | Beginner | Python | Black-Scholes and option pricing in Python, with the derivation alongside the code. | F10, T4 |
| N20 | Kaabar, *Deep Learning for Finance* (O'Reilly, 2024) | Advanced | Python | Deep learning models for trading signals and prediction, with Python code. | M1, M3 |
| N21 | *Machine Learning Trading Book* | Intermediate | Python | ML for trading. Author not checked. | M3, S3 |
| N22 | *Deep Learning in Quantitative Trading* | Advanced | Python | Deep learning for quant trading strategies. Author not checked. | M3, M9 |
| N23 | Baranasooriya, *High-Performance Algorithmic Trading Using AI* (2024) | Advanced | Python | AI trading algorithms and performance tuning for speed and throughput. | M3, X2 |
| N24 | *Hydrodynamics of Markets* | Advanced | None | Market dynamics from a physics-style view. Author not checked. | X8, X1 |
| N25 | Hindering, *Quant Developers' Tools and Techniques* (2023) | Intermediate | Varies | Tooling and workflows for quant developers: environments, testing, and data pipelines. | X11, S5 |
| N26 | Manokhin, *Applied Conformal Prediction* | Advanced | Python | Prediction intervals with guaranteed coverage, so a signal's stated confidence can be trusted. | M1, TS4 |
| N27 | Manokhin, *Probabilistic Forecasting with Conformal Prediction in Python* | Advanced | Python | Probabilistic forecasts in Python using conformal methods. | TS4, M1 |
| N28 | Manokhin, *Mastering Advanced Time Series Forecasting in Python* (probabilistic, hierarchical, foundation models) | Advanced | Python | Probabilistic, hierarchical, and foundation-model forecasting. | TS4, TS7 |
| N29 | Manokhin, *Mastering Modern Time Series Forecasting* (2026) | Intermediate | Python | Modern forecasting from statistical baselines to deep learning. Newer than TS4. | TS4, TS5 |
| N30 | Manokhin, *Mastering Forecasting Metrics* | Intermediate | Python | How to measure forecast accuracy properly, and which metric fits which problem. | S8, TS4 |
| N31 | Manokhin, *Mastering CatBoost* | Intermediate | Python | Gradient boosting for tabular data: a common model for trading signals. | M3, M6 |
| N32 | Kulkarni et al., *Time Series Algorithms Recipes* (2023) | Intermediate | Python | Implementation recipes for classical and deep forecasting models. | TS6, TS5 |
| N33 | *archive.zip* and *pro_package.zip* | Intermediate | Varies | Two archives from the same Manokhin collection; contents not checked. Check before using. | TS4 |
| N34 | Stefanica, Radoičić & Wang, *150 Most Frequently Asked Questions on Quant Interviews* (3rd ed., 2024) | Intermediate | None | Quant interview questions across the core stages: probability, pricing, and trading. Optional career prep. | F8, V1, S8 |
| N35 | *Quant Bible* (MIT Sloan Business Club) | Beginner | None | Quant careers and interview prep. Optional; not checked. | F19 |
| N36 | *Quant Finance Interview Guide* | Beginner | None | Interview prep for quant roles. Optional; not checked. | F19, S8 |

### Duplicates

- **Already on the map under another ID:** the Donadio et al. HFT book (X15), Hanson's C++ for finance (C8), Kakushadze's *151 Trading Strategies* (S11), and Joseph's *Modern Time Series Forecasting with Python* (TS4) also appear in a second edition or format. They are listed once, under the entry above.

## Role tracks

The three roles overlap more each year. Every role starts with the shared spine, then adds its own core and additional books. A book can appear in more than one role.

### Shared spine (all roles)

- **Core (read):** F8, F9, F10 (foundations); S8, S9 (testing); X1 (costs); M1 (leakage in ML); T1, T2 (Python for finance).
- **Additional (to read):** F5, F7 (probability); S14 (permutation tests); N8 (testing technical rules); X8 (microstructure); N6 (data integrity).

### Quant researcher

**Scarce skill:** judging whether a result is real. Most of the work is leakage, overfitting, and whether the signal survives costs.

- **Core (read):** S1, S2, S3 (strategy logic and ML pipeline); S16 (regime detection); S21 (pairs with ML); M2, M3 (portfolio ML and ML pipeline); M9 (applied ML); TS1, TS2 (econometrics); TS4 (forecasting); P4 (active management theory); T8, T9 (data handling); T10 (R).
- **Additional (to read):** S15 (finding alphas); S18 (reliability test of technical rules); F14 (Monte Carlo); M4, M5 (ML in finance and asset pricing); M10 (deep learning, multivariate series); N26, N30, N31 (conformal prediction, forecast metrics, CatBoost).

### Quant trader

**Scarce skill:** knowing how a position behaves when prices move, and how much it costs to trade.

- **Core (read):** V1, V2, V3, V4 (options and volatility); V11 (FX market); X1, X2, X3, X4 (execution and costs); X8 (microstructure); P6, P9 (sizing and risk); S13 (pairs trading).
- **Additional (to read):** V5 (dynamic hedging); V6 (derivatives markets); V8 (SABR smile); V10 (interest rates); X5 (HFT); X9 (optimal execution); P3, P7, P8, P10 (portfolio, Kelly, risk, desk controls); N4, N5 (portfolio construction and risk); N15, N16, N17, N18 (FX options, retail options, volatility, Greeks).

### Quant developer

**Scarce skill:** making sure the code does what the research says, in the live system as well as the backtest.

- **Core (read):** S5, S6, S7 (building a backtester in Python and C++); S10 (R platform); X11, X12, X13 (IB API and FIX); X14 (system architecture); C4, C6, C7, C15 (C++ for finance); T8, T9 (data handling).
- **Additional (to read):** E1, E2, E3 (clean code, refactoring, TDD); E4, E5 (design patterns); X15, X16, X17 (low-latency C++ systems); C1, C2, C3, C5, C8 to C14 (C++ pricing libraries and numerics); M12 (C++ data mining); N9, N10 (cloud deployment, cookbook); N25 (quant developer tooling).

## Main interconnections

- **Testing spine:** S8 (robustness) to S9 (checklist) to S14 (permutation tests, to read) to M1 (overfitting in ML). These four belong together.
- **Portfolio spine:** F4 (convex optimization, to read) to P4 (active management theory) to M2 (HRP) to P6 (sizing) to P7 (Kelly, to read).
- **Execution spine:** X1 (transaction costs) to X8 (microstructure) to X11 (IB build) to X14 (system architecture) to X15 (C++ HFT, to read).
- **Pricing spine:** F8 to F9 and F10 to V1 (options) to C4 and C6 (C++ implementation) to C11 (AAD for risk, to read).

