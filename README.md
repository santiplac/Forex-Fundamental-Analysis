# Forex Fundamental Analysis Dashboard

A comprehensive, institutional-grade platform for real-time monitoring and analysis of fundamental economic indicators across major currency pairs. Designed for financial professionals, institutional traders, and sophisticated market participants.

![Status](https://img.shields.io/badge/Status-Production-success) ![License](https://img.shields.io/badge/License-MIT-blue) ![Version](https://img.shields.io/badge/Version-1.0.0-informational)

## Overview

This dashboard provides professional-grade fundamental analysis tools for the foreign exchange market, integrating real-time market data with comprehensive macroeconomic indicators. The platform employs quantitative methodologies to assess currency strength and relative value across G10 currencies.

### Key Capabilities

**Currency Strength Assessment**
- Quantitative scoring methodology (0-100 scale) based on nine fundamental indicators
- Real-time classification into bullish, bearish, or neutral sentiment categories
- Systematic ranking of currencies by fundamental strength
- Integration of central bank policy stance and forward guidance

**Macroeconomic Intelligence**
- Coverage of eight major currencies: USD, EUR, GBP, JPY, AUD, CAD, CHF, NZD
- Comprehensive tracking of GDP growth, inflation, employment, and external balance metrics
- Central bank policy monitoring including interest rates and meeting schedules
- Live foreign exchange rates with 60-second refresh intervals

**Visual Analytics**
- Heat map visualization of economic indicators with color-coded strength metrics
- Intuitive interface for rapid assessment of cross-currency dynamics
- Interactive tooltips providing contextual information on each indicator
- Responsive design optimized for desktop and tablet devices

## Technical Architecture

**Frontend Framework**
- React 18 for component-based architecture
- Pure JavaScript implementation with no build dependencies
- Single-page application design for optimal performance

**Data Infrastructure**
- RESTful API integration for foreign exchange rates
- Client-side data processing and calculation engine
- Automatic refresh mechanisms for real-time data integrity
- Fallback data provisions for API unavailability scenarios

**Hosting Environment**
- Static site deployment compatible with GitHub Pages, Netlify, Vercel
- No server-side dependencies required
- SSL/TLS encryption supported
- Global CDN distribution capability

## Deployment Instructions

### Standard Deployment

The application is designed as a standalone HTML file requiring no compilation or build process.

```bash
# Clone repository
git clone https://github.com/yourusername/forex-dashboard.git

# Navigate to directory
cd forex-dashboard

# Deploy to web server or open locally
# No additional dependencies required
```

### GitHub Pages Deployment

1. Navigate to repository Settings
2. Access Pages section
3. Configure source branch: `main`
4. Set directory: `/ (root)`
5. Confirm deployment
6. Access via: `https://yourusername.github.io/forex-dashboard`

### Local Development Environment

```bash
# Python HTTP Server
python -m http.server 8000

# Node.js HTTP Server
npx http-server -p 8000

# Access at http://localhost:8000
```

## Data Sources and Methodology

### Market Data

| Category | Source | Update Frequency | Coverage |
|----------|--------|------------------|----------|
| FX Rates | ExchangeRate-API | 60 seconds | Major pairs vs USD |
| Economic Indicators | Central Bank Publications | 24 hours | G10 currencies |
| Policy Rates | Monetary Authority Announcements | Event-driven | Central bank decisions |

### Primary Data Providers

- Federal Reserve System (United States)
- European Central Bank (Eurozone)
- Bank of England (United Kingdom)
- Bank of Japan (Japan)
- Reserve Bank of Australia (Australia)
- Bank of Canada (Canada)
- Swiss National Bank (Switzerland)
- Reserve Bank of New Zealand (New Zealand)

### Quantitative Methodology

The fundamental strength score employs a weighted, multi-factor model incorporating:

**Growth Dynamics** (20% weight)
- Real GDP growth rate relative to historical averages
- Industrial production trends
- Economic momentum indicators

**Monetary Policy Stance** (25% weight)
- Policy rate differential versus global average
- Central bank forward guidance
- Real interest rate calculations

**Price Stability** (15% weight)
- Consumer Price Index deviation from 2% target
- Core inflation trends
- Inflation expectations

**Labor Market Conditions** (15% weight)
- Unemployment rate versus natural rate estimates
- Employment growth trends
- Wage pressure indicators

**External Balance** (25% weight)
- Current account balance as percentage of GDP
- Trade balance in absolute terms
- Capital flow dynamics

**Fiscal Position** (10% weight)
- Government debt-to-GDP ratio
- Fiscal deficit trends
- Credit ratings

Scores are normalized on a 0-100 scale with dynamic weighting adjustments based on market regime and volatility conditions.

## Configuration and Customization

### Data Update Configuration

Modify refresh intervals in the codebase:

```javascript
// Line 860: FX rate refresh interval (milliseconds)
const ratesInterval = setInterval(fetchForexRates, 60000);

// Line 861: Economic data refresh interval (milliseconds)
const fundamentalInterval = setInterval(loadEconomicData, 86400000);
```

### Economic Data Updates

Update the `baseEconomicData` object with latest statistical releases:

```javascript
const baseEconomicData = {
    USD: { 
        gdp: 29.18,          // Trillions USD
        gdpGrowth: 1.8,      // Annual %
        interestRate: 4.25,  // Policy rate %
        inflation: 3.4,      // CPI YoY %
        unemployment: 4.2,   // % of labor force
        currentAccount: -3.9, // % of GDP
        debt: 126.5,         // % of GDP
        tradeBalance: -68.2, // Billions USD
        production: 1.6      // Industrial production YoY %
    },
    // Additional currencies...
};
```

### Indicator Customization

Modify displayed indicators by updating:
1. Tooltip definitions in `indicatorTooltips` object
2. Table header structure in heatmap component
3. Data cell rendering logic in table body

## Browser Compatibility Matrix

| Browser | Minimum Version | Status | Notes |
|---------|----------------|--------|-------|
| Google Chrome | 90+ | Fully Supported | Recommended for optimal performance |
| Mozilla Firefox | 88+ | Fully Supported | All features functional |
| Safari | 14+ | Supported | Minor visual differences possible |
| Microsoft Edge | 90+ | Fully Supported | Chromium-based versions |
| Mobile Safari | 14+ | Limited | Tablet optimized, phone support minimal |
| Chrome Mobile | 90+ | Limited | Tablet optimized, phone support minimal |

## Risk Disclosure and Disclaimers

**IMPORTANT LEGAL NOTICE**

This software is provided for informational and educational purposes only and does not constitute:
- Financial advice or investment recommendations
- Trading signals or market timing guidance
- Professional investment advisory services
- An offer or solicitation to buy or sell any financial instruments

**Risk Warnings**

Foreign exchange trading carries a high level of risk and may not be suitable for all investors. Key risks include:

- **Market Risk**: Currency values can fluctuate significantly due to economic, political, and market conditions
- **Leverage Risk**: Margin trading can result in losses exceeding initial investment
- **Liquidity Risk**: Market conditions may prevent execution at desired prices
- **Operational Risk**: Technology failures may impact data accuracy or availability
- **Country Risk**: Political and economic instability can affect currency values

**User Responsibilities**

Users of this platform are solely responsible for:
- Conducting independent research and due diligence
- Consulting with licensed financial advisors before making investment decisions
- Understanding that past performance does not guarantee future results
- Ensuring compliance with applicable laws and regulations in their jurisdiction
- Verifying the accuracy of data from primary sources

**No Warranty**

This software is provided "as is" without warranty of any kind, express or implied. The developers make no representations regarding the accuracy, completeness, or timeliness of information provided.

## Planned Enhancements

**Phase 1: Data Expansion**
- Integration of additional G10 and emerging market currencies
- Historical time series data with trend analysis
- Economic calendar integration with event impact assessment
- Enhanced central bank communication analysis

**Phase 2: Analytics Enhancement**
- Advanced charting capabilities with technical overlays
- Correlation matrices across currency pairs
- Volatility metrics and implied vs realized analysis
- Sentiment indicators from multiple data sources

**Phase 3: User Experience**
- Customizable dashboard layouts and saved views
- Alert system for significant economic releases
- Export functionality (CSV, PDF, Excel)
- API access for programmatic data retrieval

**Phase 4: Mobile and Accessibility**
- Responsive mobile design optimization
- Progressive Web App (PWA) implementation
- WCAG 2.1 AA compliance for accessibility
- Multi-language internationalization support

## Contributing Guidelines

Contributions from the financial technology and quantitative finance community are welcome. We maintain high standards for code quality and documentation.

**Contribution Process**

1. Fork the repository to your account
2. Create a feature branch with descriptive naming: `feature/enhancement-name`
3. Implement changes with comprehensive documentation
4. Ensure backward compatibility with existing functionality
5. Submit pull request with detailed description of modifications
6. Await code review and address feedback

**Code Standards**

- Maintain consistent code formatting and style
- Include inline comments for complex logic
- Update documentation to reflect changes
- Test across supported browsers before submission
- Preserve existing API contracts and data structures

**Priority Areas for Contribution**

- Enhanced calculation methodologies and factor models
- Additional data source integrations
- Performance optimizations and caching strategies
- Accessibility improvements (ARIA labels, keyboard navigation)
- Unit testing and test coverage expansion
- Security enhancements and input validation

## License

This project is licensed under the MIT License.

```
MIT License

Copyright (c) 2026 [Your Name/Organization]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Contact and Support

**Technical Support**
- Issue Tracking: https://github.com/yourusername/forex-dashboard/issues
- Discussion Forum: https://github.com/yourusername/forex-dashboard/discussions

**Professional Inquiries**
- GitHub: [@santiplac](https://github.com/santiplac/)
- Email: santiagocasuriaga@gmail.com
- LinkedIn: https://www.linkedin.com/in/santiago-pla-casuriaga/

**Security Concerns**
For security-related issues, please contact security@yourdomain.com directly rather than opening public issues.

## Acknowledgments

This project integrates data and methodologies from various sources:

- Exchange rate data provided by ExchangeRate-API
- Economic statistics sourced from central bank publications and statistical agencies
- Analytical framework informed by institutional research methodologies
- Built on open-source technologies including React and modern web standards

## Version History

**Version 1.0.0** (February 2026)
- Initial production release
- Core fundamental analysis framework
- Real-time data integration
- Heat map visualization
- Eight major currency coverage

---

**Developed for institutional-grade financial analysis | Production deployment ready | February 2026**
