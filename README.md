# Bitcoin Line of Credit Calculator

A web-based calculator to visualize and project Bitcoin-backed line of credit scenarios over a 20-year period. This tool helps you understand how monthly withdrawals, interest rates, and Bitcoin price growth affect your credit line and collateral.

## Features

- **Interactive Chart**: 20-year projection with visual breakdown of accumulated credit, monthly interest, Bitcoin price, max credit line, and Bitcoin net worth
- **Live BTC Price**: Fetch current Bitcoin price from CoinPaprika API with one click
- **Configurable Parameters**:
  - BTC Collateral amount
  - Maximum Loan-to-Value (LTV) ratio
  - Bitcoin price (manual or fetched live)
  - Bitcoin price growth rate projection
  - Annual interest rate
  - Monthly withdrawal amounts
  - Inflation rate adjustments
  - Two interest payment methods (cash flow vs. sell BTC)

- **Real-time Calculations**: Instant updates as you adjust parameters
- **Shareable URLs**: All settings are saved to URL parameters for easy sharing
- **Monthly Breakdown Table**: Detailed view of all months until credit limit is reached

## What is a Bitcoin Line of Credit?

A Bitcoin line of credit allows you to borrow against your Bitcoin holdings without selling them. This means:

- Keep your Bitcoin exposure and potential upside
- Access liquidity for expenses, investments, or other needs
- Pay interest only on what you borrow
- No capital gains tax events from selling crypto

Learn more about [Strike's Bitcoin-backed line of credit](https://strike.me/en/blog/introducing-the-bitcoin-backed-line-of-credit/).

## Getting Started

### Prerequisites

- [Bun](https://bun.sh/) or Node.js
- Modern web browser
- Internet connection (for live BTC price fetch, optional)

### Installation

```bash
# Clone the repository
git clone https://github.com/mauricewipf/btc-line-of-credit.git
cd btc-line-of-credit

# Install dependencies
bun install
# or
npm install

# Open index.html in your browser
open index.html
```

## How to Use

1. **Enter your BTC collateral**: The amount of Bitcoin you plan to use as collateral
2. **Set your LTV ratio**: Typically 30-50% for conservative approaches
3. **Input Bitcoin price**: Click the ↻ button to fetch the live price, or enter manually
4. **Configure growth expectations**:
   - Expected annual Bitcoin price growth (optional)
   - Expected annual inflation rate (default: 2%)
5. **Set loan terms**:
   - Annual interest rate (default step: 0.1%)
   - Monthly withdrawal amount (default: $210)
   - Interest payment method (cash flow or sell BTC)
6. **Review the chart**: See how your credit line and interest evolve over 20 years

### Interest Payment Methods

- **Pay from cash flow**: Interest is covered by external funds; BTC collateral remains unchanged
- **Pay with BTC (sell Bitcoin)**: Interest is paid by selling a portion of your Bitcoin collateral each month

## Configuration via URL Parameters

You can pre-configure the calculator using URL parameters:

| Parameter | Description | Example |
|-----------|-------------|---------|
| `btc` | BTC Collateral amount | `?btc=1.5` |
| `ltv` | Max LTV ratio | `?ltv=50` |
| `price` | Bitcoin price in USD | `?price=100000` |
| `rate` | Annual interest rate | `?rate=3.5` |
| `withdrawal` | Monthly withdrawal | `?withdrawal=500` |
| `inflation` | Annual inflation rate | `?inflation=2.0` |
| `growth` | Annual BTC growth rate | `?growth=5` |
| `payBtc` | Pay interest with BTC | `?payBtc=true` |

**Example**: `index.html?btc=2&price=95000&rate=2.5&withdrawal=3000`

## Technology Stack

- **Bootstrap 5.3.3**: Responsive UI framework (local)
- **Chart.js 4.4.1**: Interactive data visualization (local)
- **CoinPaprika API**: Live Bitcoin price data
- **Vanilla JavaScript**: No build step required
- **Bun/npm**: Package manager

## Offline Usage

The calculator works completely offline after initial setup:
- Bootstrap and Chart.js are loaded from local `node_modules`
- Live BTC price fetch will gracefully fall back to $100,000 if offline
- All calculations and chart rendering work without internet

## Disclaimer

This calculator is for educational and planning purposes only. It provides projections based on the parameters you input, but actual results may vary significantly.

- Cryptocurrency prices are highly volatile
- Interest rates may change
- LTV requirements may be adjusted by lenders
- This is not financial advice

Always consult with financial professionals before making borrowing decisions.

## License

MIT License - see LICENSE file for details

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Acknowledgments

- Inspired by [Strike's Bitcoin-backed line of credit](https://strike.me/en/blog/introducing-the-bitcoin-backed-line-of-credit/)
- Built with [Chart.js](https://www.chartjs.org/) and [Bootstrap](https://getbootstrap.com/)
- Live price data from [CoinPaprika](https://coinpaprika.com/)
