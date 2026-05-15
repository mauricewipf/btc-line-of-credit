# Bitcoin Line of Credit Calculator

A web-based calculator to visualize and project Bitcoin-backed line of credit scenarios over a 5-year period. This tool helps you understand how monthly withdrawals, interest rates, and Bitcoin price growth affect your credit line and collateral.

![Bitcoin Line of Credit Calculator](https://github.com/user-attachments/assets/placeholder.png)

## Features

- **Interactive Chart**: 5-year projection with visual breakdown of accumulated credit, interest, and Bitcoin price trends
- **Configurable Parameters**:
  - BTC Collateral amount
  - Maximum Loan-to-Value (LTV) ratio
  - Bitcoin price and growth rate projections
  - Annual interest rate
  - Monthly withdrawal amounts
  - Inflation rate adjustments
  - Two interest payment methods (accumulate vs. pay with BTC)

- **Real-time Calculations**: Instant updates as you adjust parameters
- **Shareable URLs**: All settings are saved to URL parameters for easy sharing
- **Monthly Breakdown Table**: Detailed view of the first 12 months

## Live Demo

Visit the calculator at: https://mauricewipf.github.io/btc-line-of-credit

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
3. **Input current Bitcoin price**: Or your expected price
4. **Configure growth expectations**:
   - Expected annual Bitcoin price growth (optional)
   - Expected annual inflation rate (optional)
5. **Set loan terms**:
   - Annual interest rate
   - Monthly withdrawal amount
   - Interest payment method
6. **Review the chart**: See how your credit line and interest evolve over 5 years

### Interest Payment Methods

- **Accumulate**: Interest is added to your credit balance each month
- **Pay with BTC**: Interest is paid by selling a small portion of your Bitcoin collateral

## Configuration via URL Parameters

You can pre-configure the calculator using URL parameters:

| Parameter | Description | Example |
|-----------|-------------|---------|
| `btc` | BTC Collateral amount | `?btc=1.5` |
| `ltv` | Max LTV ratio | `?ltv=50` |
| `price` | Bitcoin price in USD | `?price=100000` |
| `rate` | Annual interest rate | `?rate=3.0` |
| `rent` | Monthly withdrawal | `?rent=2000` |
| `inflation` | Annual inflation rate | `?inflation=2.5` |
| `growth` | Annual BTC growth rate | `?growth=10` |
| `payBtc` | Pay interest with BTC | `?payBtc=true` |

**Example**: `https://mauricewipf.github.io/btc-line-of-credit/?btc=2&price=95000&rate=2.5&rent=3000`

## Technology Stack

- **Bootstrap 5.3.3**: Responsive UI framework
- **Chart.js 4.4.1**: Interactive data visualization
- **Vanilla JavaScript**: No build step required
- **Bun**: Package manager and runtime

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
