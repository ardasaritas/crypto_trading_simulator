# CTIS255 Cryptocurrency Trading Simulator

A web-based educational cryptocurrency trading platform that simulates real-world crypto trading using historical market data from 2021.

## Features

### Trading Simulation
- **365 Days of Historical Data**: Complete 2021 market data for 9 major cryptocurrencies
- **Real Market Prices**: Authentic OHLC (Open, High, Low, Close) price data
- **Interactive Trading**: Buy and sell cryptocurrencies with real-time portfolio updates
- **Multi-User Support**: Create and manage multiple trader profiles

### Portfolio Management
- Start with $1,000 virtual cash
- Real-time wallet balance tracking
- Dynamic portfolio value calculation
- Transaction validation (sufficient funds/coins)
- Persistent storage across sessions

### Visualization & Controls
- **Interactive Charts**: Candlestick-style price charts with hover details
- **Timeline Control**: Manual day-by-day progression or automated play mode
- **Visual Feedback**: Color-coded gains (green) and losses (red)
- **Sliding Window**: 120-day rolling chart view for long-term analysis

## Technology Stack

- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Libraries**: jQuery 3.7.1, Font Awesome 6.7.1
- **Storage**: LocalStorage (client-side persistence)
- **Architecture**: Single Page Application (SPA)
- **No Backend Required**: Fully browser-based application

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A local web server (Live Server, http-server, or similar)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/ardasaritas/github_remake_255.git
cd Project255
```

2. Start a local web server:

**Using VS Code Live Server**
- Install the Live Server extension
- Right-click on `index.html`
- Select "Open with Live Server"
- Navigate to `http://localhost:5502`

3. Open your browser and access the application

### First Steps

1. **Create a Profile**: Click "Create Profile" to add a new trader
2. **Select a Cryptocurrency**: Choose from the 9 available coins
3. **View the Chart**: Examine historical price trends
4. **Make Trades**:
   - Click "Buy" to purchase coins with available cash
   - Click "Sell" to liquidate holdings for cash
5. **Progress Through Time**:
   - Click "Next Day" to advance manually
   - Click "Play" to auto-advance through days

## Usage Guide

### Trading Operations

**Buying Cryptocurrency:**
1. Select a coin from the sidebar
2. Click the "Buy" button
3. Enter the amount of coins to purchase
4. Confirm the transaction (requires sufficient cash)

**Selling Cryptocurrency:**
1. Select a coin you own from the sidebar
2. Click the "Sell" button
3. Enter the amount of coins to sell
4. Confirm the transaction (requires sufficient coins)

### Time Controls

- **Next Day Button**: Manually advance one day
- **Play Button**: Auto-advance at 100ms intervals
- **Pause Button**: Stop auto-advancement
- **Day Counter**: Shows current day (1-365) and date

### Portfolio Tracking

- **Cash Balance**: Available funds for purchasing
- **Wallet Table**: All cryptocurrency holdings with current values
- **Total Balance**: Combined value of cash + all holdings
- **Real-time Updates**: Prices update as you progress through days

## Project Structure

```
crypto_trading_simulator/
├── index.html         # Main application entry point
├── app.js             # Core application logic
├── app.css            # Styling and layout
├── db.js              # Market data database
├── images/            # Cryptocurrency logos
│   ├── ada.png
│   ├── avax.png
│   ├── btc.png
│   ├── doge.png
│   ├── eth.png
│   ├── pol.png
│   ├── snx.png
│   ├── trx.png
│   └── xrp.png
└── README.md
```

## Data Structure

### Market Data
Each day contains OHLC data for all 9 cryptocurrencies:
```javascript
{
  date: '01-01-2021',
  coins: [
    { code: 'btc', open: 29374.15, high: 29600.63, low: 28803.59, close: 29374.15 },
    // ... 8 more coins
  ]
}
```

### User State
Stored in LocalStorage:
```javascript
{
  active: "User Name",
  users: [
    {
      name: "User Name",
      wallet: {
        cash: 1000,
        Bitcoin: 0,
        Ethereum: 0,
        // ... other coins
      },
      currentDay: 1,
      currentDate: "1 January 2021",
      market: []
    }
  ]
}
```

## Key Features Explained

### Chart Visualization
- Custom-built candlestick-style bars using HTML/CSS
- Hover to see detailed OHLC prices
- Green bars indicate price increase (close > open)
- Red bars indicate price decrease (close < open)
- Grey dashed line shows closing price trend

### Sliding Window Algorithm
- Displays 120 days of data at once
- Automatically scrolls as you progress beyond day 120
- Efficient rendering for year-long simulation

### State Persistence
- All user data saved to browser LocalStorage
- Profiles persist across browser sessions
- Automatic save after every transaction or day change

## Development

### Local Development Setup

1. Open project in VS Code
2. Configuration is in `.vscode/settings.json` (port 5502)
3. Use Live Server for hot reload during development

### File Dependencies

- `index.html` → Main structure, loads all dependencies
- `app.js` → Depends on `db.js` and jQuery
- `app.css` → Standalone styling
- `db.js` → Standalone data module

## Educational Value

This project demonstrates:
- JavaScript state management
- DOM manipulation with jQuery
- Data visualization techniques
- Client-side storage (LocalStorage)
- Event handling and user interactions
- Responsive UI design
- Algorithm implementation (sliding window)
- Financial calculation logic

## Browser Compatibility

- Chrome/Edge (Recommended)
- Firefox
- Safari
- Opera

## Known Limitations

- Requires JavaScript enabled
- LocalStorage must be enabled in browser
- No real-time data - uses historical 2021 data only
- Client-side only - no server-side validation
- Data resets if LocalStorage is cleared

## Team Members

- **Yağız Çetin**
- **Arda Sarıtaş**
- **Işık Dönger**
- **İbrahim Can Doğan**

## Course Information

**Course**: CTIS255
**Project Type**: Term Project
**Year**: 2024
**Institution**: Bilkent University

## License

This is an educational project created for academic purposes.

---

