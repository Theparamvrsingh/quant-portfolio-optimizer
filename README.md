# AI Portfolio Optimizer

A financial portfolio optimization app with a clean web interface, optional AI ticker suggestions, and downloadable analysis output.

## Features

- Manual ticker input for custom portfolios
- Optional AI-based ticker suggestions
- Portfolio optimization with risk/return analytics
- PDF analysis export with allocation details
- FastAPI backend and browser-based UI

## Tech Stack

- Python
- FastAPI
- Uvicorn
- Pandas
- NumPy
- PyPortfolioOpt
- yfinance

## Prerequisites

- Python 3.11+ (3.12 recommended)
- `pip`

## Local Setup

1. Install dependencies:

```bash
pip install -r requirements.txt
```

2. (Optional) Create a `.env` file if you want AI features:

```env
OPENAI_API_KEY=YOUR_API_KEY
```

3. Start the app:

```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

4. Open in browser:

`http://localhost:8000`

## Docker Setup

Start:

```bash
docker compose up -d
```

Stop:

```bash
docker compose down
```

## Usage

1. Enter tickers manually or generate suggestions
2. Set date range and investment amount
3. Run analysis to view optimized allocation and metrics
4. Export or review generated report output

## License

Distributed under the MIT License.
