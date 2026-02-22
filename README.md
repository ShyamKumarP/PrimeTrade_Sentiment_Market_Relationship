# PrimeTrade_Sentiment_Market_Relationship
#Performance Analysis
#Behaviorial Analysis
#Segmentation Analysis

Sentiment-Driven Trader Behavior Analysis

Methodology

This study examines whether trader behavior and performance vary across sentiment regimes (Extreme Fear, Fear, Neutral, Greed, Extreme Greed).

0. Data Cleaning

We loaded the dataset. No null values or duplicates were present.The timestamp was changed accordingly.
The same format date from both datasets was used to merge the dataset using the left join.
After merging there was one date without value but from sentiment dataset the average value of sentiment around the missing date was found and used to fill it.

1. Data Aggregation

We computed daily trader-level metrics by grouping trades by trade_date and Account. Key performance and behavioral metrics included:
    Performance: daily PnL, win rate, drawdown proxy
    Behavioral: trades per day, average trade size, total leverage, long/short ratio

2. Sentiment Regime Analysis

Daily metrics were grouped by sentiment classification. We used:
    Mean comparisons (for rough idea)
    Boxplots (for distributional differences and median behavior)

This allowed us to compare central tendency, dispersion, and regime-specific behavioral amplification.

3. Trader Segmentation

We segmented traders using median splits:
    High vs Low Risk → based on average leverage
    Frequent vs Infrequent → based on average trades per day
    Long-Term vs Short-Term → based on long/short ratio

We then analyzed how each segment performed and behaved across sentiment regimes.

Key Insights
1. Fear Amplifies Aggressive Behavior

Trading activity, leverage usage, and directional bias all increase significantly during Fear regimes, especially Extreme Fear.
This indicates that emotional stress triggers overtrading and higher exposure.

2. Greed Does Not Drive Aggression

Contrary to intuition, Greed regimes show lower leverage and reduced trade frequency.
Behavior appears more stable and controlled during optimistic market conditions.

3. Risk Efficiency Is Regime-Dependent

High-risk traders outperform during Fear regimes, while low-risk traders perform relatively better during Extreme Greed.
This suggests that optimal risk exposure depends on the prevailing sentiment regime.

4. Long-Term Traders Increase Conviction in Fear

Long-term traders dramatically increase long bias during Fear, suggesting long-term positioning behavior.
Rather than holding short-term like greed makret.

Strategy Recommendations
Strategy 1 — Regime-Adjusted Risk Allocation

Adopt sentiment-adaptive leverage control:
    During Fear: Cap leverage to prevent panic-driven overexposure; selectively allocate to historically strong      high-risk traders.
    During Extreme Greed: Reduce aggressive exposure and shift capital toward low-risk traders.

Strategy 2 — Volatility-Responsive Trade Intensity

Align strategy style with regime:
    During Extreme Fear: Increase short-term or volatility-exploiting strategies.
    During Greed: Reduce turnover and favor lower-frequency, capital-efficient strategies.

Final Conclusion

Trader behavior is strongly regime-dependent. Fear conditions amplify trading intensity, leverage usage, and directional conviction, while Greed conditions correspond to reduced activity and lower risk exposure. Emotional stress appears to be the primary driver of aggressive trading behavior. A sentiment-adaptive strategy framework can therefore improve risk control and capital allocation efficiency.
