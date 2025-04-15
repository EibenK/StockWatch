# StockWatch

## Project Roadmap

### Frontend
    - Monitor a single stock using an API
    - Auto-refresh
    - Display:
        i.   Current price
        ii.  Trend line / historical chart
        iii. Price deltas with animated green/red flashes
        iv.  Potentially add Buy/Sell simulated data or display data acquistion rate

### Backend
    - REST API
        i.   GET /stock/price
        ii.  GET /stock/history
    - Data can come from a service such as Alpha Vantage, IEX Cloud, Yahoo Finance API
    - Cache response in SQLite

### Testing Suite
    - Tools
        i.   Pytest, httpx, requests, jsonschema, pytest-html
    - Tests
        i.   Status codes(200, 404, etc.)
        ii.  JSON Schema for GET requests
        iii. Simulated Sandboxing for API delay or outage
        iv.  Response time < 500 ms
        v.   Stock price value formatting(float, range validation, etc.)
    
### UI Testing Suite
    - Selenium, Playwright, or pytest-playwright
        i.   Testing animations 
        ii.  Charts render correctly
        iii. Dark mode or theme toggles
    
### CI/CD Integration
    - Github Actions or Jenkins to run test for code quality/security
    - Generate pytest html reports