# 🚀 ICT Quant Suite v3.0

![ICT Quant Suite Banner](https://img.shields.io/badge/Version-3.0-blue?style=for-the-badge&logo=metatrader) ![MQL5](https://img.shields.io/badge/MQL5-Expert%20Advisor-green?style=for-the-badge) ![License](https://img.shields.io/badge/License-Custom-red?style=for-the-badge)

**Advanced ICT Trading Algorithm for MetaTrader 5**  
Built by the ICT Quant Engineering Team | © Copyright by M4DI~UciH4  
Empowering traders with multi-timeframe analysis, smart detections, and high-probability signals.  
Turn market chaos into structured opportunities with FVG, Order Blocks, Liquidity Grabs, OTE Zones, and more!

---

## 📜 Overview

ICT Quant Suite v3.0 is a cutting-edge MQL5 Expert Advisor (EA) designed for traders following the Inner Circle Trader (ICT) methodology. This powerful tool automates the detection of key ICT concepts like Fair Value Gaps (FVG), Order Blocks (OB), Liquidity Pools, Optimal Trade Entry (OTE) zones, and Market Structure breaks. It generates high-confluence trading signals, complete with entry, stop-loss, and take-profit levels, while providing a sleek dashboard for real-time insights.

Whether you're scalping on M5 or swinging on H4, this suite adapts to your style with multi-timeframe support and customizable kill zones. Say goodbye to manual charting – let the algorithm do the heavy lifting!

**Key Highlights:**
- **Multi-Timeframe Analysis**: Syncs detections across H4, H1, M15, and M5 (configurable).
- **Signal Generation**: High-confidence BUY/SELL signals with confluence scoring (0-10).
- **Auto-Trading Option**: Risk-managed trades with drawdown protection.
- **Visual Dashboard**: Real-time stats on kill zones, structure, and setups.

> ⚠️ **Disclaimer**: Trading involves risk. This EA is for educational purposes. Backtest thoroughly and use on a demo account first. Past performance ≠ future results.

---

## ✨ Features

- **Fair Value Gaps (FVG)**: Detects bullish/bearish gaps with strength grading (A/B/C). Tracks mitigation and fill percentage.
- **Order Blocks (OB)**: Identifies high-probability reversal zones with expiry, touch counts, and strength.
- **Liquidity Pools**: Spots swing highs/lows and equal levels for potential grabs. Visualizes untouched liquidity.
- **Optimal Trade Entry (OTE) Zones**: Fibonacci-based retracement zones (0.618-0.786) with "sweet spot" at 0.705.
- **Market Structure Analysis**: Detects HH/HL/LH/LL, BOS, CHOCH, and trend strength (0-100%).
- **Kill Zones**: Time-based filters for London, New York, Asian, and London Close sessions.
- **Signal Engine**: Generates setups like FVG Retest, OB Retest, Liquidity Grab, OTE Pullback, and Silver Bullet. Includes confidence % and R:R checks.
- **Dashboard**: Interactive panel showing active elements, confluence, signals, and stats.
- **Display Controls**: Toggle layers (HTF/MTF/LTF), auto-hide labels on zoom, and limit max displayed objects.
- **Auto-Trading**: Risk % per trade, max drawdown protection, magic number, and slip/deviation handling.
- **Alerts & Notifications**: Popup alerts and push notifications for new signals.

**Supported Timeframes**: M1 to MN1 (default: H4/H1/M15/M5).  
**Pairs**: Optimized for forex majors/minors, but works on indices, crypto, etc.  
**Broker Compatibility**: Any MT5 broker with low spreads.

---

## 🛠️ Installation

1. **Download the Script**:
   - Clone this repo: `git clone https://github.com/RizkyEvory/ICT-Advance-MT5.git`
   - Or download the `.mq5` file from the releases.

2. **Compile in MetaEditor**:
   - Open MetaTrader 5 → Tools → MetaQuotes Language Editor (F4).
   - Open `ICT_Quant_Suite_v3.ex5` and compile (F7). Fix any errors if prompted.

3. **Attach to Chart**:
   - In MT5, open a chart (e.g., EURUSD H1).
   - Drag the EA from Navigator (Expert Advisors) onto the chart.
   - Configure inputs in the popup and click OK.

4. **Enable Auto-Trading**:
   - Click the "AutoTrading" button in MT5 toolbar (or Ctrl+E).
   - Ensure "Allow live trading" in EA settings.

> 💡 **Pro Tip**: Use a VPS for 24/7 operation. Test on demo first!

---

## ⚙️ Configuration

The EA offers extensive inputs grouped for ease. Default values are optimized, but tweak based on your strategy.

### General Settings
- `EnableTrading`: false → Enable auto-trading.
- `RiskPercent`: 1.0 → % of balance to risk per trade.
- `MaxDrawdown`: 10.0 → Pause trading if DD exceeds this %.
- `MagicNumber`: 202401 → Unique ID for trades.

### Kill Zone Settings
- `UseLondonKZ`: true → Enable London session (2-5 GMT).
- `UseNewYorkKZ`: true → Enable NY session (13-16 GMT).
- `GMTOffset`: 0 → Adjust for broker time.

### FVG Settings
- `DetectFVG`: true → Enable FVG detection.
- `MinFVGSize`: 5.0 → Min gap size in points.
- `DrawFVG`: true → Visualize zones.
- Colors: Bullish (DarkGreen), Bearish (DarkRed).

### Order Block Settings
- `DetectOB`: true → Enable OB detection.
- `OBLookback`: 50 → Bars to scan.
- `MinOBSize`: 10.0 → Min OB size in points.

### Liquidity Settings
- `DetectLiquidity`: true → Enable liquidity detection.
- `SwingLookback`: 20 → Swing detection period.
- `EqualLevelTolerance`: 5.0 → Points for equal highs/lows.

### OTE Zone Settings
- `DetectOTE`: true → Enable OTE zones.
- `OTEFibHigh`: 0.618 → Upper Fib level.
- `OTEFibLow`: 0.786 → Lower Fib level.

### Market Structure Settings
- `DetectMS`: true → Enable structure analysis.
- `MSLookback`: 50 → Bars for swings.

### Signal Settings
- `MinConfluence`: 7 → Min score for signals (0-10).
- `RequireKillZone`: true → Only signal in kill zones.
- `MinRiskReward`: 2.0 → Min R:R ratio.
- `EnableAlerts`: true → Popup alerts.

### Dashboard Settings
- `ShowDashboard`: true → Display panel.
- `DashboardX/Y`: 20/30 → Position.
- Colors & Font: Customize look.

### Display Control
- `OnlyCurrentTF`: false → Show only current TF elements.
- `MaxFVGDisplay`: 15 → Limit drawn FVGs.
- `ShowOnlyActiveFVG`: false → Hide mitigated FVGs.
- `AutoHideLabels`: true → Hide labels when zoomed out.
- `ZoomThreshold`: 300 → Bars visible to trigger hide.

### Multi-Timeframe
- `TF1/TF2/TF3/TF4`: H4/H1/M15/M5 → Analysis frames.

> 🔧 **Customization Tip**: For aggressive trading, lower `MinConfluence` to 5. For conservative, set to 8+.

---

## 📈 Usage

1. **Attach EA**: Load on chart, configure inputs.
2. **Monitor Dashboard**: Watch for kill zones, structure, and confluence.
3. **Signals**: When confluence ≥ min, a signal appears with levels drawn.
   - **Silver Bullet**: Rare, high-prob setup (all factors aligned).
4. **Auto-Trade**: If enabled, EA opens position. Manage manually or let it run.
5. **Manual Trading**: Use signals as alerts; enter trades yourself.
6. **Backtesting**: Use MT5 Strategy Tester with visual mode to see drawings.

**Common Scenarios**:
- **FVG Retest**: Price pulls back to unfilled FVG in trend direction.
- **OB Retest**: Bounce from strong OB with MS alignment.
- **Liquidity Grab**: Trade reversal after sweeping highs/lows.
- **OTE Pullback**: Enter at Fib zone during retracement.

**Performance Tracking**:
- Internal stats: Total signals, wins, profit pips (accessible via globals).

---

## 📸 Screenshots

*(Insert screenshots of the dashboard, chart with zones, and a signal example here.)*

---

## 🤝 Contributing

Contributions welcome! Fork the repo, make changes, and submit a PR.
- Report issues via GitHub Issues.
- Suggestions: Improve detections, add new ICT concepts (e.g., PD Arrays).

**Development Notes**:
- Code is modular with structs for elements.
- Use MQL5 debugger for testing.
- Ensure compliance with ICT principles.

---

## 📄 License

© 2024 ICT Quant Engineering Team | M4DI~UciH4  
All rights reserved. This script is provided "as is" without warranty.  
You may use/modify for personal use, but commercial redistribution requires permission.  
GitHub: [https://github.com/RizkyEvory](https://github.com/RizkyEvory)

---

## 📞 Contact

- GitHub: [@RizkyEvory](https://github.com/RizkyEvory)
- Questions? Open an issue or DM on GitHub.

*Built with ❤️ for the ICT community. Trade smart, stay profitable! 💹*
