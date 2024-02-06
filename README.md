README

## Fair Value Gap Sweep MT4

This code is a custom indicator for MetaTrader 4 that detects and draws fair value gaps on a price chart. Fair value gaps occur when there is a significant difference between the closing price of one candle and the opening price of the next candle. This indicator is designed to help traders identify potential trading opportunities based on these gaps.

### Features

- Detects and draws fair value gaps on the price chart
- Customizable colors and styles for bullish and bearish gaps
- Sound, email, and push notification alerts for gap detection

### Global Variables

- `gapColorBullish`: Color for bullish gaps
- `gapColorBearish`: Color for bearish gaps
- `gapStyle`: Style for gap lines
- `gapWidth`: Width for gap lines
- `soundAlert`: Enable sound alert
- `emailAlert`: Enable email alert
- `pushAlert`: Enable push notification

### Indicator Initialization

The `OnInit` function is responsible for initializing the indicator. It sets the indicator's short name, style, and buffer. 

### Indicator Deinitialization

The `OnDeinit` function is called when the indicator is being removed from the chart. It clears the indicator buffers.

### Indicator Calculation

The `OnCalculate` function is the main calculation function of the indicator. It iterates through the price data and detects fair value gaps using the `IsGap` function. If a gap is detected, it calls the `DrawGap` function to draw the gap line on the chart. It also triggers alerts based on the alert settings.

### Gap Detection

The `IsGap` function checks if a gap exists at a given index by comparing the previous close price with the current open price. If the gap is positive and the current open is greater than the previous close, or if the gap is negative and the current open is less than the previous close, a gap is considered to exist.

### Drawing Gap Lines

The `DrawGap` function is responsible for drawing the fair value gap line on the chart. It calculates the gap size and determines the color based on the gap direction. It then creates a trend line object using the `ObjectCreate` function and sets the color using the `ObjectSet` function.

### Product Description

Fair Value Gap Sweep MT4 is a powerful forex trading indicator that helps traders identify and take advantage of fair value gaps in the market. Fair value gaps occur when there is a significant difference between the closing price of one candle and the opening price of the next candle. These gaps can indicate potential trading opportunities.

This indicator automatically detects and draws fair value gaps on the price chart, making it easy for traders to identify these gaps visually. It also provides customizable colors and styles for bullish and bearish gaps, allowing traders to personalize the indicator to their preference.

In addition to visual detection, Fair Value Gap Sweep MT4 also offers sound, email, and push notification alerts for gap detection. Traders can choose to receive alerts whenever a fair value gap is detected, ensuring they never miss a potential trading opportunity.

Please note that ForexRobotEasy is not the official developer of this product. We only provide this sample code as an example of how the indicator can work. To find the official developer of this product, please refer to the MQL5 platform.

For detailed reviews and trading results of this product, please visit [ForexRobotEasy Fair Value Gap Sweep MT4 Review](https://forexroboteasy.com/forex-robot-review/fair-value-gap-sweep-mt4-review-powerful-forex-trading-indicator/).
