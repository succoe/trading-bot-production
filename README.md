# Trading Bot Production

A production-ready trading bot with Docker deployment, 
Telegram alerts, multi-asset portfolio management and 
professional risk management.

## What This Project Does
- Docker containerized bot running 24/7
- Telegram alerts for trades, drawdowns and heartbeats
- Multi-asset portfolio trading 5 assets simultaneously
- Correlation matrix to detect over-concentration
- Circuit breaker halting trading on 2% daily loss
- Volatility-targeted position sizing
- SQLite database logging all trades permanently

## Results
| Asset | Trades | P&L |
|-------|--------|-----|
| QQQ | 4 | +$420.66 |
| GLD | 2 | +$150.00 |
| TLT | 2 | +$80.00 |
| MSFT | 5 | -$402.76 |

## Risk Management
- Max daily loss limit: 2%
- Max drawdown limit: 5%
- Circuit breaker: halts all trading automatically
- Volatility sizing: smaller positions in choppy markets
- Correlation filter: reduces size when assets move together

## Tech Stack
- Python 3.12
- Docker
- pandas
- yfinance
- scikit-learn
- SQLite3
- Telegram Bot API
- requests

## How to Run
```bash
# Run locally
pip install pandas yfinance requests scikit-learn
python bot.py

# Run with Docker
docker build -t tradingbot .
docker run tradingbot
```

## Key Files
- `bot.py` — Main production bot
- `risk_manager.py` — Circuit breaker and position sizing
- `portfolio.py` — Multi-asset portfolio manager
- `alerts.py` — Telegram notification system
- `Dockerfile` — Container configuration

- ## Deployment
Bot is containerized with Docker and can be deployed to any 
cloud server (AWS EC2, DigitalOcean, Google Cloud) in minutes.
- `requirements.txt` — Python dependencies

## Architecture
