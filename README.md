# Options-Technical Hybrid Scanner

A trading tool designed for retail traders to identify and execute trades in volatile stocks by combining options data and technical analysis.

## Overview

The Options-Technical Hybrid Scanner is a trading tool designed to empower retail traders by providing a systematic, data-driven method to identify trading opportunities in volatile stocks, such as TSLA. It implements the "Options-Technical Hybrid Strategy" framework, which combines options data and technical analysis.

## Features

- **Market Context Analysis**: Evaluate market environment using technical indicators and options data
- **Key Levels Mapping**: Use options chain data to pinpoint critical support and resistance levels
- **Trade Setup Rules Engine**: Define conditions for bullish, bearish, or neutral trade setups
- **Confirmation and Timing**: Provide entry and exit signals
- **Risk Management**: Offer risk control suggestions
- **Scanner Feature**: Filter stocks and deliver actionable insights

## Installation

```bash
# Clone the repository
git clone https://github.com/oghenetejiriorukpegmail/options-scanner-tool.git
cd options-scanner-tool
python -m venv .venv
.venv\Scripts\activate.ps1  # On Windows
# OR
source .venv/bin/activate  # On macOS/Linux

# Install dependencies
pip install -r requirements.txt
```

## Usage

```bash
# Run the web interface
python src/web/app.py

# Or run the scanner directly
python src/main.py
```

## Project Structure

```
options-scanner-tool/
├── src/
│   ├── modules/           # Core modules
│   │   ├── scanner.py     # Main scanner implementation
│   │   ├── market_context.py
│   │   ├── key_levels.py
│   │   ├── trade_setup.py
│   │   ├── confirmation.py
│   │   └── risk_management.py
│   ├── web/               # Web interface
│   │   └── app.py         # Flask web application
│   └── main.py            # CLI entry point
├── static/                # Static web assets
│   ├── css/               # Stylesheets
│   └── js/                # JavaScript files
├── templates/             # HTML templates
├── scanner_results/       # Output directory for scan results
├── config.json            # Configuration file
├── requirements.txt       # Dependencies
└── README.md              # Documentation
```

## Configuration

The scanner can be configured through the `config.json` file:

```json
{
  "max_workers": 5,
  "filters": {
    "trend": ["bullish", "bearish", "neutral"],
    "pcr_min": 0,
    "pcr_max": 2,
    "rsi_min": 0,
    "rsi_max": 100,
    "stoch_rsi_min": 0,
    "stoch_rsi_max": 100,
    "min_confidence": 60
  },
  "output_dir": "scanner_results"
}
```

## Development Phases

### Phase 1: Core Functionality
- Implement market context analysis with basic indicators (EMAs, RSI)
- Integrate basic options data (OI, volume)
- Develop the scanner with initial filters for trade setups

### Phase 2: Advanced Features
- Add advanced options metrics (gamma, charm, vanna, vomma, VWIV, GEX)
- Integrate social media sentiment analysis
- Enhance the scanner with sophisticated filters and real-time alerts

### Phase 3: User Experience and Optimization
- Improve UI with interactive visualizations and dashboards
- Optimize performance for real-time data handling
- Launch educational resources (tutorials, guides, webinars)

## License

MIT