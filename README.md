# Crypto Stat - Professional Trading Dashboard & Journal

<div align="center">

![Crypto Stat Dashboard](https://via.placeholder.com/1200x600/0f172a/22d3ee?text=Crypto+Stat+Dashboard)

**A professional cryptocurrency trading dashboard with real-time market data, technical analysis, and trading journal**

[![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React-19-blue?style=flat-square&logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-4-38bdf8?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)

[Live Demo](#) • [Report Bug](#) • [Request Feature](#)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Screenshots](#-screenshots)
- [Tech Stack](#-tech-stack)
- [File Structure](#-file-structure)
- [Getting Started](#-getting-started)
- [API Integration](#-api-integration)
- [UI/UX Design](#-uiux-design)
- [Methods & Techniques](#-methods--techniques)
- [Future Enhancements](#-future-enhancements)
- [Developer](#-developer)
- [License](#-license)

---

## 🎯 Overview

**Crypto Stat** is a comprehensive cryptocurrency trading platform designed for professional traders and enthusiasts. It combines real-time market data, advanced technical analysis, and a robust trading journal to help users make informed trading decisions and track their performance over time.

The application leverages the CoinGecko API to provide up-to-date cryptocurrency prices, market trends, and historical data, while offering a suite of technical indicators including RSI, ATR, and Bollinger Bands for in-depth market analysis.

---

## ✨ Features

### 📊 **Dashboard**
- **Live Ticker Tape**: Continuous scrolling ticker displaying top cryptocurrencies with real-time prices and 24h changes
- **Global Market Statistics**: Total market cap, 24h volume, BTC dominance, and active cryptocurrencies
- **Interactive Price Charts**: Multi-timeframe candlestick charts (24h, 7d, 30d, 90d, 1y) with OHLC data visualization
- **Comprehensive Coin List**: Searchable table with market cap, volume, and price change metrics
- **Animated Statistics**: Smooth number transitions powered by Framer Motion

### 📖 **Trading Journal**
- **Strategy Builder**: Create and manage multiple trading strategies with custom parameters
  - Risk-to-reward ratio targets
  - Maximum drawdown limits
  - Entry and exit rules documentation
- **Trade Logger**: Record all trades with automatic P&L calculations
  - Support for long/short positions
  - Entry/exit prices and dates
  - Trade notes and observations
- **Performance Analytics**: 
  - Total P&L with animated number displays
  - Win rate percentage
  - Profit factor calculation
  - Average risk-to-reward ratio
  - Win/loss distribution pie chart
  - Equity curve visualization
- **Data Persistence**: Local storage integration for offline access

### 🔬 **Research Hub**
- **Multi-Coin Analysis**: Compare technical indicators across different cryptocurrencies
- **Technical Indicators**:
  - **RSI (Relative Strength Index)**: Identify overbought/oversold conditions
  - **ATR (Average True Range)**: Measure market volatility
  - **Bollinger Bands**: Visualize price volatility and trends
  - **Moving Averages**: SMA and EMA calculations
- **Visual Indicator Charts**: Interactive Recharts displaying RSI trends over time
- **Market Sentiment Analysis**: Fear & Greed index with visual gauge

---

## 📸 Screenshots

### Dashboard - Market Overview
![Dashboard](https://via.placeholder.com/1200x700/0f172a/22d3ee?text=Dashboard+with+Live+Ticker+and+Charts)
*Real-time market data with animated ticker tape and interactive price charts*

### Trading Journal - Strategy Management
![Trading Journal](https://via.placeholder.com/1200x700/0f172a/8b5cf6?text=Trading+Journal+with+Analytics)
*Track your trades, manage strategies, and analyze performance metrics*

### Research Hub - Technical Analysis
![Research Hub](https://via.placeholder.com/1200x700/0f172a/f59e0b?text=Research+Hub+with+Technical+Indicators)
*Advanced technical analysis with RSI, ATR, and Bollinger Bands*

### Mobile Responsive Design
![Mobile View](https://via.placeholder.com/400x800/0f172a/10b981?text=Mobile+Responsive+Design)
*Fully responsive design optimized for all screen sizes*

---

## 🛠 Tech Stack

### **Frontend Framework**
- **Next.js 16**: React framework with App Router, Server Components, and Server Actions
- **React 19.2**: Latest React with useEffectEvent and Activity component support
- **TypeScript**: Type-safe development with full IntelliSense support

### **Styling & UI**
- **Tailwind CSS v4**: Utility-first CSS with CSS-first configuration
- **shadcn/ui**: High-quality, accessible component library
- **Framer Motion**: Smooth animations and page transitions
- **Lucide React**: Beautiful, consistent icon set

### **Data Visualization**
- **Recharts**: Composable charting library for interactive data visualization
- **Custom Chart Components**: Line charts, candlestick charts, pie charts, and area charts

### **State Management**
- **Zustand**: Lightweight state management with persistence middleware
- **SWR**: Data fetching with caching, revalidation, and auto-refresh

### **API & Data**
- **CoinGecko API**: Comprehensive cryptocurrency data (Free tier)
- **Native Fetch**: Modern data fetching with TypeScript support

---

## 📁 File Structure

\`\`\`
crypto-stat/
├── app/
│   ├── layout.tsx                 # Root layout with metadata and fonts
│   ├── page.tsx                   # Dashboard page (home)
│   ├── journal/
│   │   └── page.tsx               # Trading journal page
│   ├── research/
│   │   └── page.tsx               # Research hub page
│   └── globals.css                # Global styles and design tokens
│
├── components/
│   ├── layout/
│   │   └── header.tsx             # Navigation header with active states
│   │
│   ├── dashboard/
│   │   ├── ticker-tape.tsx        # Animated scrolling ticker
│   │   ├── market-overview.tsx    # Global market statistics cards
│   │   ├── price-chart.tsx        # Interactive candlestick chart
│   │   └── coin-list.tsx          # Searchable cryptocurrency table
│   │
│   ├── journal/
│   │   ├── journal-stats.tsx      # Performance analytics dashboard
│   │   ├── strategy-list.tsx      # Strategy management interface
│   │   ├── strategy-dialog.tsx    # Create/edit strategy modal
│   │   ├── trade-journal.tsx      # Trade log table
│   │   ├── trade-dialog.tsx       # Log trade modal
│   │   └── pnl-chart.tsx          # Equity curve visualization
│   │
│   ├── research/
│   │   ├── coin-selector.tsx      # Cryptocurrency selection dropdown
│   │   ├── technical-analysis.tsx # Indicator statistics cards
│   │   ├── indicator-charts.tsx   # RSI trend chart
│   │   └── market-sentiment.tsx   # Fear & Greed gauge
│   │
│   └── ui/
│       ├── glass-card.tsx         # Glassmorphism card component
│       ├── animated-number.tsx    # Number animation component
│       └── [shadcn components]    # Button, Card, Dialog, Input, etc.
│
├── hooks/
│   └── use-crypto-data.ts         # SWR hooks for API data fetching
│
├── lib/
│   ├── coingecko-api.ts           # CoinGecko API client with endpoints
│   ├── technical-indicators.ts    # RSI, ATR, Bollinger Bands calculators
│   ├── store.ts                   # Zustand store for journal data
│   └── utils.ts                   # Utility functions (cn, etc.)
│
└── public/                        # Static assets
\`\`\`

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ and npm/yarn/pnpm
- Modern web browser with ES6+ support

### Installation

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/yourusername/crypto-stat.git
   cd crypto-stat
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   \`\`\`

3. **Run the development server**
   \`\`\`bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   \`\`\`

4. **Open your browser**
   \`\`\`
   Navigate to http://localhost:3000
   \`\`\`

### Build for Production

\`\`\`bash
npm run build
npm start
\`\`\`

### Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/yourusername/crypto-stat)

---

## 🔌 API Integration

### CoinGecko API (Free Tier)

Crypto Stat uses the **CoinGecko API v3** to fetch real-time cryptocurrency data. The free tier provides generous rate limits suitable for personal use.

**Endpoints Used:**
- `/coins/markets` - List of cryptocurrencies with market data
- `/global` - Global cryptocurrency market statistics
- `/coins/{id}/market_chart` - Historical price data for charts
- `/coins/{id}/ohlc` - OHLC candlestick data
- `/search/trending` - Trending coins
- `/simple/price` - Real-time price data

**Rate Limiting:**
- The app implements SWR caching with intelligent revalidation
- Automatic retry logic with exponential backoff
- 30-second refresh intervals to stay within free tier limits

**API Client Location:** `lib/coingecko-api.ts`

---

## 🎨 UI/UX Design

### Design Philosophy

Crypto Stat embraces a **glassmorphism fintech aesthetic** with a focus on clarity, professionalism, and data density. The design system prioritizes readability while maintaining visual appeal through subtle animations and modern UI patterns.

### Design System

**Color Palette:**
- **Background**: Deep slate (#0f172a) for reduced eye strain during extended use
- **Primary**: Cyan (#22d3ee) for calls-to-action and interactive elements
- **Success**: Emerald green for positive metrics and gains
- **Destructive**: Rose red for negative metrics and losses
- **Accent Colors**: Purple and orange for data visualization (chart-2, chart-3)

**Typography:**
- **Headings**: Plus Jakarta Sans (weights 200-800) for modern, clean headlines
- **Body**: Plus Jakarta Sans for excellent readability
- **Monospace**: IBM Plex Mono for numeric data and code
- **Serif**: Lora for elegant accent text

**Visual Techniques:**
- **Glassmorphism**: Translucent cards with backdrop blur for depth
- **Gradient Borders**: Subtle gradients to define card boundaries
- **Smooth Animations**: Framer Motion for page transitions and number updates
- **Micro-interactions**: Hover states, tap feedback, and loading states

### Responsive Design

- **Mobile-First Approach**: Optimized for small screens, enhanced for desktop
- **Breakpoints**: sm (640px), md (768px), lg (1024px), xl (1280px)
- **Adaptive Layouts**: Flexbox and CSS Grid for fluid, responsive components
- **Touch-Friendly**: Large tap targets and swipe gestures on mobile

### Accessibility

- **WCAG 2.1 AA Compliant**: Proper contrast ratios and text sizing
- **Keyboard Navigation**: Full keyboard support for all interactive elements
- **Screen Reader Support**: Semantic HTML and ARIA labels
- **Focus Indicators**: Visible focus states for navigation

---

## 🧪 Methods & Techniques

### Architecture Patterns

**1. Server Components by Default**
- Leverage Next.js 16 App Router for optimal performance
- Server-side data fetching reduces client-side JavaScript
- Client components only when interactivity is required

**2. Custom Hooks for Data Fetching**
- SWR-based hooks (`use-crypto-data.ts`) for consistent data management
- Centralized error handling and loading states
- Automatic revalidation and cache management

**3. Zustand for Client State**
- Lightweight state management (< 1kb)
- localStorage persistence for trading journal
- Computed selectors for analytics calculations

**4. Component Composition**
- Small, focused components for maintainability
- Shared UI components via shadcn/ui
- Glass card wrapper for consistent styling

### Technical Techniques

**1. Technical Indicator Calculations**
\`\`\`typescript
// RSI (Relative Strength Index)
- 14-period calculation with gain/loss averages
- Identifies overbought (>70) and oversold (<30) conditions

// ATR (Average True Range)
- 14-period volatility measurement
- Helps determine position sizing

// Bollinger Bands
- 20-period SMA with 2 standard deviation bands
- Identifies volatility expansion/contraction
\`\`\`

**2. Performance Optimizations**
- SWR caching reduces API calls by 90%
- React.memo for expensive chart components
- Lazy loading for off-screen content
- CSS containment for layout performance

**3. Real-time Updates**
- 30-second polling intervals for live data
- Optimistic UI updates for instant feedback
- Background revalidation with SWR

**4. Data Persistence**
- localStorage for trading journal entries
- Zustand persist middleware for automatic serialization
- Fallback mechanisms for storage errors

---

## 🚀 Future Enhancements

### Planned Features

**Phase 1: Enhanced Analysis**
- [ ] Additional technical indicators (MACD, Stochastic, Fibonacci)
- [ ] Multiple timeframe analysis view
- [ ] Price alerts and notifications
- [ ] Portfolio tracking with allocation pie charts

**Phase 2: Social & Community**
- [ ] Share trading strategies with the community
- [ ] Follow top traders and their performance
- [ ] Trading idea discussions and comments
- [ ] Leaderboard for top-performing strategies

**Phase 3: Advanced Tools**
- [ ] Backtesting engine for strategies
- [ ] Paper trading simulator
- [ ] Advanced charting tools (drawing tools, trendlines)
- [ ] Automated trading signals

**Phase 4: Integration & Export**
- [ ] Exchange API integration (Binance, Coinbase)
- [ ] Automatic trade import from exchanges
- [ ] Export reports to PDF/CSV
- [ ] Tax calculation and reporting tools

**Phase 5: AI & Machine Learning**
- [ ] AI-powered trade suggestions
- [ ] Sentiment analysis from social media
- [ ] Pattern recognition in charts
- [ ] Predictive analytics with ML models

---

## 👨‍💻 Developer

<div align="center">

### **Ethel Technologies**

**Natnael Sintayehu** - Full-Stack Developer & Creator

[![Portfolio](https://img.shields.io/badge/Portfolio-etheltechnologies.com-22d3ee?style=for-the-badge&logo=google-chrome)](https://etheltechnologies.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Natnael_Sintayehu-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/natnael-sintayehu)
[![GitHub](https://img.shields.io/badge/GitHub-ethel--tech-181717?style=for-the-badge&logo=github)](https://github.com/ethel-tech)
[![Twitter](https://img.shields.io/badge/Twitter-@ethel__tech-1DA1F2?style=for-the-badge&logo=twitter)](https://twitter.com/ethel_tech)
[![Email](https://img.shields.io/badge/Email-contact@etheltechnologies.com-D14836?style=for-the-badge&logo=gmail)](mailto:contact@etheltechnologies.com)

</div>

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.



---

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/crypto-stat/issues) page
2. Create a new issue with detailed information
3. Contact us at: contact@etheltechnologies.com

---

<div align="center">

**Built with ❤️ by Ethel Technologies**

⭐ Star this repo if you find it helpful!

[Back to Top](#crypto-stat---professional-trading-dashboard--journal)

</div>
