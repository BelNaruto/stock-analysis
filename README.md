# Stock Analysis API

The **Stock Analysis API** offers in-depth access to stock market data, analytics, and financial insights. Designed for developers, investors, and analysts, this API provides detailed information on stock performance, historical data, financial ratios, and more, enabling sophisticated market analysis and application integration. This API can be found here: [RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/stock-analysis6)

## Key Features

- **Stock Performance Data**: Retrieve real-time and historical data on stock performance, including price changes, volume, and market capitalization.
- **Financial Ratios**: Access key financial ratios and metrics, such as P/E ratio, earnings per share (EPS), and dividend yield.
- **Company Profiles**: Get detailed profiles of publicly traded companies, including business descriptions, industry classifications, and key executives.
- **Market Insights**: Gain insights into market trends and stock performance with advanced analytics and visualization tools.

## Getting Started

1. **Sign Up**: Create an account on RapidAPI.
2. **Subscribe**: Choose a subscription plan that fits your needs.
3. **API Key**: Obtain your unique API key to begin making requests.
4. **Documentation**: For detailed usage instructions, visit the [Stock Analysis API Documentation](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/stock-analysis6).


## Endpoint: Get Stock Technical Indicators

### URL

`GET /stock/:symbol/indicators`

### Path Parameters

- `symbol` (string): The stock symbol for which to fetch technical indicators.

### Query Parameters

- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the Relative Strength Index (RSI).

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated technical indicators.
  
  ```json
  {
    "symbol": "AAPL",
    "indicators": {
      "sma20": 150.23,
      "sma50": 148.67,
      "rsi14": 45.12
    }
  }



## Endpoint: Get Stock Exponential Moving Average (EMA)

### URL

`GET /stock/:symbol/ema`

### Path Parameters

- `symbol` (string): The stock symbol for which to fetch the EMA.

### Query Parameters

- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the Exponential Moving Average (EMA).

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol, the period used, and the calculated EMA.
  
  ```json
  {
    "symbol": "AAPL",
    "period": 14,
    "ema": 149.85
  }


## Endpoint: Get Stock Price Information

### URL

`GET /stock/:symbol/price`

### Path Parameters

- `symbol` (string): The stock symbol for which to fetch the current price information.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol, current price, currency, display name, and market capitalization.
  
  ```json
  {
    "symbol": "TSLA",
    "price": 700.50,
    "currency": "USD",
    "symbolName": "Tesla, Inc.",
    "marketCap": 700000000000
  }




## Endpoint: Get Accumulation Distribution Line (ADL)

### URL

`GET /stock/adl`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the ADL.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated ADL.
  
  ```json
  {
    "symbol": "AAPL",
    "adl": 123456789.0
  }


## Endpoint: Get Average Directional Index (ADX)

### URL

`GET /stock/adX`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the ADX.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the ADX.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated ADX.
  
  ```json
  {
    "symbol": "AAPL",
    "adx": 24.35
  }



## Endpoint: Get Average True Range (ATR)

### URL

`GET /stock/atr`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the ATR.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the ATR.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated ATR.
  
  ```json
  {
    "symbol": "AAPL",
    "atr": 5.67
  }



## Endpoint: Get Awesome Oscillator (AO)

### URL

`GET /stock/awesome-oscillator`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Awesome Oscillator.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `fastPeriod` (string): The fast period for calculating the Awesome Oscillator.
- `slowPeriod` (string): The slow period for calculating the Awesome Oscillator.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Awesome Oscillator values.
  
  ```json
  {
    "symbol": "AAPL",
    "response": {
      "value": [0.25, -0.10, 0.05, ...] // Example of Awesome Oscillator values
    }
  }



## Endpoint: Get Bollinger Bands

### URL

`GET /stock/bollingerBands`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Bollinger Bands.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-05'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the Bollinger Bands.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Bollinger Bands.

  ```json
  {
    "symbol": "AAPL",
    "response": {
      "upperBand": [150.0, 155.0, ...], // Example values
      "middleBand": [145.0, 150.0, ...],
      "lowerBand": [140.0, 145.0, ...]
    }
  }


## Endpoint: Get Commodity Channel Index (CCI)

### URL

`GET /stock/cci`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Commodity Channel Index (CCI).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the CCI.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Commodity Channel Index (CCI).

  ```json
  {
    "symbol": "AAPL",
    "cci": [120.5, 130.2, ...] // Example CCI values
  }



## Endpoint: Get Force Index (FI)

### URL

`GET /stock/fi`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Force Index (FI).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `period` (string): The period to be used for calculating the Force Index.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Force Index (FI).

  ```json
  {
    "symbol": "AAPL",
    "fi": [15000, 20000, ...] // Example FI values
  }




## Endpoint: Get Know Sure Thing (KST)

### URL

`GET /stock/kst`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Know Sure Thing (KST).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-08'`.
- `signalPeriod` (string): The signal period to be used for calculating KST.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Know Sure Thing (KST).

  ```json
  {
    "symbol": "AAPL",
    "kst": [0.05, 0.10, ...] // Example KST values
  }



## Endpoint: Get Money Flow Index (MFI)

### URL

`GET /stock/mfi`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Money Flow Index (MFI).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (string): The period to be used for calculating the MFI.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Money Flow Index (MFI).

  ```json
  {
    "symbol": "AAPL",
    "mfi": [50.23, 45.67, ...] // Example MFI values
  }



## Endpoint: Get Moving Average Convergence Divergence (MACD)

### URL

`GET /stock/macd`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Moving Average Convergence Divergence (MACD).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `fastPeriod` (string): The period for the fast EMA (Exponential Moving Average) used in MACD calculation.
- `slowPeriod` (string): The period for the slow EMA used in MACD calculation.
- `signalPeriod` (string): The period for the signal line used in MACD calculation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated MACD values.

  ```json
  {
    "symbol": "AAPL",
    "macd": {
      "macdLine": [0.23, -0.45, ...], // Example MACD line values
      "signalLine": [0.10, -0.30, ...], // Example signal line values
      "histogram": [0.13, -0.15, ...] // Example histogram values
    }
  }


## Endpoint: Get On Balance Volume (OBV)

### URL

`GET /stock/onbv`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the On Balance Volume (OBV).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated OBV values.

  ```json
  {
    "symbol": "AAPL",
    "obv": [1000, 1500, 1200, ...] // Example OBV values
  }

## Endpoint: Get Parabolic Stop and Reverse (PSAR)

### URL

`GET /stock/psar`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the Parabolic Stop and Reverse (PSAR).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated PSAR values.

  ```json
  {
    "symbol": "AAPL",
    "psar": [123.45, 125.67, 124.89, ...] // Example PSAR values
  }


## Endpoint: Get Rate of Change (ROC)

### URL

`GET /stock/rateoc`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Rate of Change (ROC).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The number of periods to use for the ROC calculation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Rate of Change (ROC) values.

  ```json
  {
    "symbol": "AAPL",
    "roc": [1.23, -0.56, 0.89, ...] // Example ROC values
  }


## Endpoint: Get Simple Moving Average (SMA)

### URL

`GET /stock/simplema`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Simple Moving Average (SMA).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The number of periods to use for the SMA calculation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Simple Moving Average (SMA) values.

  ```json
  {
    "symbol": "AAPL",
    "sma": [150.25, 152.30, 153.45, ...] // Example SMA values
  }


## Endpoint: Get Stochastic Oscillator (KD)

### URL

`GET /stock/stochastic`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Stochastic Oscillator (KD).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The number of periods for the Stochastic Oscillator calculation.
- `signalPeriod` (integer): The number of periods for the signal line calculation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Stochastic Oscillator (KD) values.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "K": [70, 65, 72, ...],  // %K values
      "D": [50, 55, 52, ...]   // %D values
    }
  }


## Endpoint: Get Triple Exponentially Smoothed Average (TRIX)

### URL

`GET /stock/trix`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Triple Exponentially Smoothed Average (TRIX).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The number of periods for the TRIX calculation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated TRIX values.

  ```json
  {
    "symbol": "AAPL",
    "data": {
       [0.12, 0.15, 0.14, ...]  // TRIX values
    }
  }

## Endpoint: Get Volume Weighted Average Price (VWAP)

### URL

`GET /stock/vwap`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Volume Weighted Average Price (VWAP).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated VWAP values.

  ```json
  {
    "symbol": "AAPL",
    "vwap": [150.23, 152.56, 153.45, ...]  // VWAP values
  }



## Endpoint: Get Volume Profile (VP)

### URL

`GET /stock/volProfile`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Volume Profile (VP).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `noOfBars` (integer, optional): The number of bars to include in the volume profile calculation. Default is `10`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Volume Profile values.

  ```json
  {
    "symbol": "AAPL",
    "volumeProfile": [ // Array of volume profile data
      {
        "priceRange": "150-155",
        "volume": 123456
      },
      ...
    ]
  }

## Endpoint: Get Weighted Moving Average (WMA)

### URL

`GET /stock/weightMA`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Weighted Moving Average (WMA).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The period over which to calculate the Weighted Moving Average.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Weighted Moving Average values.

  ```json
  {
    "symbol": "AAPL",
    "vwa": [ // Array of WMA values
      145.67,
      147.89,
      ...
    ]
  }

## Endpoint: Get Wilder’s Smoothing (WEMA)

### URL

`GET /stock/wema`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate Wilder’s Smoothing (WEMA).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The period over which to calculate Wilder’s Smoothing (WEMA).

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Wilder’s Smoothing values.

  ```json
  {
    "symbol": "AAPL",
    "data": [ // Array of WEMA values
      145.67,
      146.75,
      ...
    ]
  }


## Endpoint: Get Williams %R (WilliamsR)

### URL

`GET /stock/williamsR`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate Williams %R (WilliamsR).
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The period over which to calculate Williams %R (WilliamsR).

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Williams %R values.

  ```json
  {
    "symbol": "AAPL",
    "data": [ // Array of Williams %R values
      -20.45,
      -15.67,
      ...
    ]
  }


## Endpoint: Get Ichimoku Cloud

### URL

`GET /stock/ichimokuCloud`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Ichimoku Cloud.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `conversionPeriod` (integer): The period for the conversion line (Tenkan-sen). Default is `9`.
- `basePeriod` (integer): The period for the base line (Kijun-sen). Default is `26`.
- `spanPeriod` (integer): The period for the leading span B (Senkou Span B). Default is `52`.
- `displacement` (integer): The displacement period for the cloud. Default is `26`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Ichimoku Cloud values.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "conversionLine": [ // Array of Conversion Line values
        150.23,
        151.45,
        ...
      ],
      "baseLine": [ // Array of Base Line values
        145.12,
        146.34,
        ...
      ],
      "leadingSpanA": [ // Array of Leading Span A values
        148.45,
        149.78,
        ...
      ],
      "leadingSpanB": [ // Array of Leading Span B values
        142.67,
        143.89,
        ...
      ],
      "laggingSpan": [ // Array of Lagging Span values
        147.56,
        148.78,
        ...
      ]
    }
  }


## Endpoint: Get Average Gain

### URL

`GET /stock/averageGain`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Average Gain.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The period over which to calculate the Average Gain.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Average Gain values.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "averageGain": [
        1.25,
        1.30,
        ...
      ]
    }
  }



## Endpoint: Get Average Loss

### URL

`GET /stock/averageLoss`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the Average Loss.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (integer): The period over which to calculate the Average Loss.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the calculated Average Loss values.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "averageLoss": [
        0.50,
        0.45,
        ...
      ]
    }
  }


## Endpoint: Get Cross Up

### URL

`GET /stock/crossUp`

### Query Parameters

- `symbol` (string): The stock symbol for which to check for cross-up events.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the detected cross-up events.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "crossUps": [
        {"date": "2024-02-10", "value": 150.75},
        {"date": "2024-03-15", "value": 155.30}
        // ... more cross-up events
      ]
    }
  }


## Endpoint: Get Cross Down

### URL

`GET /stock/crossDown`

### Query Parameters

- `symbol` (string): The stock symbol for which to check for cross-down events.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the detected cross-down events.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "crossDowns": [
        {"date": "2024-02-12", "value": 148.50},
        {"date": "2024-03-18", "value": 146.75}
        // ... more cross-down events
      ]
    }
  }

## Endpoint: Get Highest

### URL

`GET /stock/highest`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the highest value.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (string): The period over which to determine the highest value.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the highest value over the specified period.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "highest": {
        "value": 199.50,
        "date": "2024-03-15"
      }
    }
  }


## Endpoint: Get Lowest

### URL

`GET /stock/lowest`

### Query Parameters

- `symbol` (string): The stock symbol for which to fetch the lowest value.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (string): The period over which to determine the lowest value.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the lowest value over the specified period.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "lowest": {
        "value": 120.00,
        "date": "2024-02-15"
      }
    }
  }



## Endpoint: Get Standard Deviation

### URL

`GET /stock/standardDeviation`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the standard deviation.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (string): The period over which to calculate the standard deviation.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the standard deviation over the specified period.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "standardDeviation": 5.23
    }
  }


## Endpoint: Get Sum

### URL

`GET /stock/sum`

### Query Parameters

- `symbol` (string): The stock symbol for which to calculate the sum of the closing prices.
- `from` (string, optional): The start date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-02-02'`.
- `to` (string, optional): The end date for fetching historical data in the format `YYYY-MM-DD`. Default is `'2024-04-08'`.
- `period` (string): The period over which to calculate the sum.

### Responses

#### Success Response

- **Status Code:** `200 OK`
- **Content:** JSON object containing the stock symbol and the sum of the closing prices over the specified period.

  ```json
  {
    "symbol": "AAPL",
    "data": {
      "sum": 12345.67
    }
  }


## Commonly Asked Questions

### 1. What kind of data can I access through the Stock Analysis API?
You can access stock performance data, financial ratios, company profiles, and market insights.

### 2. How do I authenticate my API requests?
You need to include your API key in the headers of your requests as detailed in the API documentation.

### 3. Are there usage limits for the API?
Yes, usage limits vary depending on the subscription plan you select. Check the RapidAPI dashboard for specifics.

### 4. Can I filter data by specific stocks or companies?
Yes, the API allows filtering to retrieve data for specific stocks or companies by their symbols or IDs.

### 5. Is historical data available for stock performance?
Yes, the Stock Analysis API includes historical data on stock performance, allowing for trend analysis and comparisons.

For more information and to start using the Stock Analysis API, visit [Stock Analysis API on RapidAPI](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/stock-analysis6).
