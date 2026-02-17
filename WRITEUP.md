# Analysis Write-Up
**Trader Performance vs Market Sentiment — Hyperliquid x Bitcoin Fear & Greed**

---

## Methodology

I merged two datasets: 211,224 Hyperliquid trade records across 32 accounts (2023-2025), and a daily Bitcoin Fear & Greed index covering the same window. After aligning both to a daily date key, I aggregated individual trades to (account, date) level. Computing daily PnL, win rate, trade count, position size, long ratio, and a drawdown proxy. The final merged dataset has 530 trader-day observations. Analysis is at that level throughout.

---

## Insights

**1. Moderate Fear is the best time to trade -- Extreme Fear is a trap**

Fear days (Fear & Greed score 25-45) produce the highest mean daily PnL at $11,333, beating Greed days ($3,192). But the median is more honest: $396 vs $147. The mean is skewed by a small number of large winning days during moderate fear conditions. Extreme Fear is different median PnL drops to zero and win rate falls to 17.4%, while traders are actually running their highest long bias (65.7%). The dip-buying instinct kicks in hard during panic, but the data shows it is not paying off.

**2. Greed days are riskier than they look**

Average drawdown on Greed days is $1,857 -- 4.8x higher than the $388 average on Fear days. Win rate barely changes (35.0% vs 35.3%), which means sentiment is not helping traders pick winners more often. What it is doing is making them size up, which amplifies both wins and losses. The large PnL variance on Greed days ($24,776 std vs $55,888 on Fear) reflects this.

**3. Higher activity on Fear days does not translate to proportionally higher returns**

Traders execute 88 trades per day on Fear days vs 59 on Greed -- a 49% increase in activity. Daily volume is 70% higher too ($507K vs $299K). But the extra trades are not generating proportional profit; the marginal PnL per trade is lower on Fear days. More activity in an uncertain environment likely means more noise trades and more fees eating into returns.

---

## Strategy Recommendations

**Rule 1: On Fear days, reduce trade count by roughly 30%**
The data shows traders run 49% more trades on Fear days without a 49% increase in returns. Cutting frequency during fear -- keeping only highest-conviction setups -- would reduce fee drag and noise exposure while preserving the legitimate opportunities that do exist on those days.

**Rule 2: On Greed days, tighten stops or reduce position size**
Drawdown is 4.8x higher on Greed days. The confidence that comes with a Greed sentiment reading seems to lead traders to hold losing positions longer or size up without adjusting risk accordingly. A simple rule of tightening stop-losses by 20-30% on Greed days would reduce the tail-risk that the drawdown numbers reveal.

---
