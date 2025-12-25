# Market History

Public repository for historical price data of various asset classes.

## Directory Structure

```
data/
├── commodities/          # Commodities (Gold, Silver, Oil, etc.)
│   └── {SYMBOL}/
│       └── {SYMBOL}-{TIMEFRAME}.csv
├── forex/                # Foreign Exchange pairs
│   └── {SYMBOL}/
│       └── {SYMBOL}-{TIMEFRAME}.csv
├── stocks/               # Individual stocks
│   └── {SYMBOL}/
│       └── {SYMBOL}-{TIMEFRAME}.csv
└── etfs/                 # Exchange-Traded Funds
    └── {SYMBOL}/
        └── {SYMBOL}-{TIMEFRAME}.csv
```

## Asset Classes

### Commodities

**CSV Format:**
| Column    | Description                        | Example              |
|-----------|------------------------------------|----------------------|
| Asset     | Asset symbol                       | GOLD                 |
| TimeFrame | Time frame                         | D1, H4, H1, M15      |
| Time      | Timestamp (YYYY-MM-DD HH:MM)       | 2024-08-19 04:00     |
| Open      | Opening price                      | 2509.27              |
| High      | Highest price                      | 2510.06              |
| Low       | Lowest price                       | 2485.60              |
| Close     | Closing price                      | 2504.13              |
| Year      | Year                               | 2024                 |
| Quarter   | Quarter (1-4)                      | 3                    |
| Month     | Month (1-12)                       | 8                    |
| Week      | Week of year (1-52)                | 34                   |

**Available Assets:**
| Asset | Timeframes |
|-------|------------|
| GOLD  | H4, D1, W1, MN |

### Forex
*Coming soon*

### Stocks
*Coming soon*

### ETFs
*Coming soon*

## File Naming Convention

`{SYMBOL}-{TIMEFRAME}.csv`

**Timeframes:**
- `MN` - Monthly
- `W1` - Weekly
- `D1` - Daily
- `H4` - 4 Hours
- `H1` - 1 Hour
- `M15` - 15 Minutes
- `M5` - 5 Minutes

## Download

**Raw URL format:**
```
https://raw.githubusercontent.com/tohaitrieu/market-history/master/data/{category}/{symbol}/{symbol}-{timeframe}.csv
```

**Example:**
```bash
# Download GOLD daily data
curl -O https://raw.githubusercontent.com/tohaitrieu/market-history/master/data/commodities/GOLD/GOLD-D1.csv

# With authentication (higher rate limit)
curl -H "Authorization: token YOUR_TOKEN" -O https://raw.githubusercontent.com/tohaitrieu/market-history/master/data/commodities/GOLD/GOLD-D1.csv
```

## License

Public domain - free to use for any purpose.
