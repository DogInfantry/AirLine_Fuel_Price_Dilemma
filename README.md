# AirLine_Fuel_Price_Dilemma
Strategic Decision Engine designed to optimize profitability and liquidity for an Indian regional airline facing a 25% fuel price shock. This project integrates Monte Carlo simulations, Linear Programming, and Real-time Financial Data to evaluate strategic trade-offs between pricing elasticity, government subsidy expansion (UDAN), and structural fleet redesign.

--------------------------------------------------------------------------------
📋 Project Overview
Problem Statement: A fast-growing regional airline faces a profitability crisis driven by a 15–25% surge in Aviation Turbine Fuel (ATF) prices. With 30–40% of routes becoming structurally unviable and load factor breakevens exceeding 85%, the airline required a data-driven turnaround strategy.
The Solution: A Python-based simulation engine that ingests real-time market data (Brent Crude, USD/INR) to stress-test three strategic horizons:
1. Network Optimization: Dynamic pricing and route rationalization.
2. UDAN Expansion: Government-backed subsidy prioritization for downside protection.
3. Structural Redesign: Long-term fleet transition analysis (Turboprop to Airbus A220/Embraer E195).

--------------------------------------------------------------------------------
🚀 Key Features
1. Real-Time Volatility Modeling
• Fetches live market data using yfinance to model Brent Crude volatility and FX risk (USD/INR).
• Constructs a dynamic Unit Economics Model calculating RASK, CASK, and contribution margins per route under stochastic fuel scenarios.
2. Risk Analysis (Monte Carlo Simulation)
• Performs 1,000+ iterations to quantify the "Risk of Ruin" (probability of negative EBITDA) for various strategic options.
• Visualizes risk profiles using Kernel Density Estimation (KDE) plots to compare "fat-tail" risks of commercial routes vs. the stability of subsidized routes.
3. Route Optimization Engine
• Implements Integer Linear Programming (PuLP) to solve the "Knapsack Problem" for subsidy allocation.
• Optimizes route selection to maximize total margin preserved and social connectivity under strict government budget constraints.
4. Strategic Consulting Frameworks
• Profitability Tree Analysis (McKinsey): Decomposes EBITDA drivers into volume, yield, fuel, and fixed cost levers.
• MECE Decision Trees (Bain): Segments routes into "Safe," "Salvageable," "At-Risk," and "Unviable" quadrants for targeted intervention.

--------------------------------------------------------------------------------
🛠️ Tech Stack & Methodologies
• Languages: Python 3.10+
• Data Analysis: Pandas, NumPy, SciPy
• Financial APIs: yfinance (Yahoo Finance), FRED (Federal Reserve Economic Data)
• Optimization: PuLP (Linear Programming), Statsmodels
• Visualization: Matplotlib, Seaborn
• Strategy Frameworks: MECE, Sensitivity Analysis (Tornado Charts), Unit Economics, Cost-Benefit Analysis (NPV/IRR).

--------------------------------------------------------------------------------
📊 Business Impact & Results
• Quantified Risk: Demonstrated that the "Network Optimization" strategy carried a 35% risk of failure due to demand elasticity, whereas the "UDAN Subsidy" strategy reduced downside risk to <5%.
• Turnaround Roadmap: Developed a 24-month "Blended Strategy" roadmap projected to swing EBITDA from -₹50 Cr to +₹650 Cr.
• Subsidy Optimization: Identified that pure commercial pricing strategies failed due to the "Operating Leverage Paradox," necessitating a shift to government-backed revenue floors.

--------------------------------------------------------------------------------
📂 Repository Structure
├── data/
│   ├── atf_timeseries.csv       # Historical fuel price data [18]
│   └── route_economics.csv      # Route-level P&L and distance data
├── notebooks/
│   ├── 01_volatility_model.ipynb # Monte Carlo simulation of fuel prices
│   ├── 02_route_optimization.ipynb # Linear programming for subsidy allocation [10]
│   └── 03_sensitivity_analysis.ipynb # Tornado charts for profitability drivers [19]
├── src/
│   ├── financial_models.py      # Unit economics and CASK/RASK calculators
│   └── strategy_engine.py       # Core decision logic
├── reports/
│   ├── executive_summary.pdf    # Management consulting deliverable [2]
│   └── risk_profile_charts.png  # Visualization of strategic options [20, 21]
└── README.md

--------------------------------------------------------------------------------
📈 SEO Keywords
• Financial Modeling Python
• Monte Carlo Simulation
• Airline Strategy Consulting
• Business Intelligence Analyst
• Linear Programming Optimization
• Risk Management
• Data Analytics Capstone
• Unit Economics Analysis
• Revenue Management
• Python for Finance

--------------------------------------------------------------------------------
⚖️ License & Attribution
This project was developed for the Winter Consulting Capstone 2025 by the Consulting & Analytics Club, IIT Guwahati. Market data derived from public APIs; strategic frameworks adapted from standard management consulting methodologies (McKinsey/Bain).
