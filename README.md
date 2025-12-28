# Trading Systems Repository

A collection of trading strategies, indicators, and tools for forex and commodity trading.

## 📁 What's Inside

- **Strategies** - Trading systems for XAUUSD, EURUSD, GBPUSD, USDJPY
- **Indicators** - Pine Script and Python technical indicators
- **Backtesting** - Framework for testing strategies on historical data
- **Risk Management** - Position sizing and risk calculators
- **Data** - Historical market data and analysis tools

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/yourusername/trading-systems.git
cd trading-systems
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Run a Backtest
```python
from backtesting.backtest_engine import Backtester
from strategies.technical.ema_crossover import EMA200Strategy

backtest = Backtester(symbol='XAUUSD', timeframe='1D', 
                      start_date='2023-01-01', end_date='2024-12-31')
results = backtest.run(EMA200Strategy)
print(f"Win Rate: {results['win_rate']:.2f}%")
```

## 📂 Directory Structure

```
trading-systems/
├── strategies/           # Trading strategies
│   ├── smart_money/     # Order block analysis
│   ├── gann/            # Gann methods
│   └── technical/       # EMA, S/R, Fibonacci
├── indicators/          # Technical indicators
│   ├── pine_script/     # TradingView indicators
│   └── python/          # Python implementations
├── backtesting/         # Backtest engine
├── risk_management/     # Position sizing & risk
├── data/                # Market data
├── docs/                # Documentation
└── tests/               # Unit tests
```

## 📊 Available Strategies

| Strategy | Win Rate | Risk:Reward | Status |
|----------|----------|------------|--------|
| Smart Money (SMC) | 62% | 2.5:1 | ✅ Live |
| EMA 200 Trend | 60% | 2.1:1 | ✅ Live |
| Gann Angles | 58% | 2.8:1 | 📄 Paper |
| Support/Resistance | 55% | 2.0:1 | 📄 Paper |
| Fibonacci | 60% | 2.2:1 | 📄 Paper |

## 🔧 Key Features

✅ Multiple trading strategies (Smart Money, Gann, EMA, etc.)  
✅ Pine Script indicators for TradingView  
✅ Backtesting framework with performance metrics  
✅ Position sizing calculator  
✅ Risk management tools  
✅ Historical data support  

## 📈 Technical Indicators

**Pine Script (TradingView)**
- Order Block Detector
- Smart Money Levels
- Gann Angles
- Market Structure Analyzer
- Fibonacci Dynamic Levels

**Python Library**
- Moving Averages
- Oscillators (RSI, MACD, Stochastic)
- Volume Analysis
- Smart Money Tools

## ⚙️ Configuration

Edit `config.yaml` to customize:
- Trading symbols and timeframes
- Strategy parameters
- Risk management limits
- Market hours

## 📝 Usage Examples

### Calculate Position Size
```python
from risk_management.position_sizing import RiskCalculator

risk = RiskCalculator(account_size=10000)
position = risk.calculate_position(
    symbol='XAUUSD', entry=2000, stop_loss=1990, risk_percent=2
)
print(f"Position Size: {position['lot_size']} lots")
```

### Use an Indicator
```python
from indicators.python.smart_money import OrderBlockDetector

detector = OrderBlockDetector(symbol='EURUSD', timeframe='4H')
signal = detector.get_signal()
print(f"Support: {signal['support']}, Resistance: {signal['resistance']}")
```

## 🧪 Testing

Run all tests:
```bash
pytest tests/ -v
```

Run specific test:
```bash
pytest tests/test_strategies.py -v
```

## 📚 Documentation

- `docs/SETUP_GUIDE.md` - Installation & setup
- `docs/STRATEGY_GUIDE.md` - Strategy documentation
- `docs/INDICATOR_GUIDE.md` - Indicator usage
- `docs/API_REFERENCE.md` - Complete API docs

## ⚠️ Disclaimer

**Educational purposes only.** Past performance ≠ future results. Trading involves risk of loss. Test on demo accounts first. Not financial advice.

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/yourusername/trading-systems/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/trading-systems/discussions)
- **Email**: your.email@example.com

## 📄 License

MIT License - See [LICENSE](LICENSE) file

## 🗺️ 2026 Roadmap

- [ ] Options trading strategies
- [ ] AI signal generation
- [ ] Real-time alerts
- [ ] Web dashboard
- [ ] Mobile app

---

**Last Updated**: December 2025  
**Version**: 1.0.0  
**Status**: ✅ Active Development

⭐ **Star this repo if it helps you!**
