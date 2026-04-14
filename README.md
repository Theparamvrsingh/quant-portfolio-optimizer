# Portfolio Optimizer

Institutional-style portfolio analytics application for constructing and evaluating equity portfolios with modern optimization and risk metrics.

## Overview

This project helps you design a portfolio from ticker symbols, optimize allocations with multiple quantitative strategies, and evaluate outcomes through risk/performance analytics and Monte Carlo simulation.

The app is built to be practical for finance interviews, personal research, and portfolio prototyping workflows.

## Core Features

- Multi-strategy optimization:
  - Max Sharpe (Efficient Frontier)
  - Minimum Volatility
  - Hierarchical Risk Parity (HRP)
  - Black-Litterman (with custom views)
- Risk and return analytics:
  - Expected return
  - Annualized volatility
  - Sharpe ratio
  - Sortino ratio
  - VaR (95%)
  - CVaR (95%)
- Monte Carlo simulation for forward-looking portfolio paths
- Optional ticker-level max-weight constraints
- Capital allocation table in dollar terms
- Refreshed institutional-themed UI

## Latest Updates

- Added hard portfolio cap so no single asset exceeds **40%**
- Added output fields for:
  - total invested weight
  - unallocated weight
  - unallocated cash amount when constraints are infeasible
- Added result banner in UI when cash remains unallocated due to constraints
- Updated visual style to a cleaner, institutional dashboard look

## Tech Stack

- Backend: FastAPI, Python
- Quant libraries: PyPortfolioOpt, NumPy, Pandas
- Data source: yfinance
- Frontend: HTML, CSS, JavaScript, Chart.js

## Project Structure

- `main.py` - API routes and orchestration logic
- `PortfolioOptimizer/` - optimization, data, simulation, and finance modules
- `static/` - frontend UI (HTML/CSS/JS)
- `tests/` - unit and integration tests

## Local Development

### Prerequisites

- Python 3.11+ (3.12 recommended)
- `pip`

### Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. Optional: enable AI-related features with `.env`:

```env
OPENAI_API_KEY=YOUR_API_KEY
```

3. Run the application:

```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

4. Open:

`http://localhost:8000`

## Docker

Start:

```bash
docker compose up -d
```

Stop:

```bash
docker compose down
```

## Usage Flow

1. Enter tickers and date range
2. Choose optimization strategy
3. (Optional) add Black-Litterman views and/or weight constraints
4. Analyze portfolio
5. Review allocation, performance metrics, and simulation chart

## Notes

- This is an educational and analytical project, not investment advice.
- The institutional visual style is inspired by professional finance dashboards and is not an official affiliation or endorsement.

## License

Distributed under the MIT License.
