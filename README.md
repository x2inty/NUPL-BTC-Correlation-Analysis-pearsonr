Mini-Procedure:

Download the Data: Go to the Bgeometrics website.

Download the CSV file containing NUPL and Bitcoin price data.

Prepare the Data for Python:

Open the CSV file in Excel or a text editor.

Ensure the DateTime column contains dates without the time ("00:00:00").

Remove the time, keeping only the YYYY-MM-DD format (then use Ctrl+H)

Replace commas with periods in the BTC Price and NUPL columns (select the column, then use Ctrl+H).

Run the Analysis:

Open your terminal (in a virtual environment) and type python.


I wanted to verify whether there was an inverse correlation between NUPL peaks and subsequent drops in Bitcoin (BTC) price. The idea was to see if, after a high NUPL, BTC would reach a low point in the following days.

To do this, I:

Identified NUPL peaks exceeding a threshold of 0.64.

Looked for BTC price lows after each NUPL peak.

Calculated the Pearson correlation between the NUPL value and the BTC low price for different timeframes (0 to 30 days).

Analyzed the significance of this correlation using the p-value to determine whether the relationship was due to chance or not.

The final objective was to determine an optimal timeframe where the inverse correlation was the strongest and most significant, which could help anticipate market movements.

The type of correlation used in your analysis is the Pearson correlation, which measures the linear relationship between two numerical variables.

To determine whether this correlation is statistically significant (i.e., not due to chance), you also use the p-value from the Pearson test.

Interpretation:

Pearson Correlation (r): It ranges between -1 and 1.

r close to -1 → Strong negative correlation (when NUPL increases, the BTC low price tends to decrease).

r close to 1 → Strong positive correlation (when NUPL increases, the BTC low price tends to increase).

r close to 0 → No clear linear relationship.

p-value: It tests the null hypothesis (There is no relationship between NUPL and BTC low price).

p-value < 0.05 → The correlation is statistically significant, with less than a 5% chance that the relationship is due to chance.

p-value > 0.05 → The correlation is not significant, and there is too much uncertainty to conclude a true relationship.

In my analysis, I looked for an optimal timeframe where the inverse (negative) correlation was the strongest and statistically significant 
(p-value < 0.05). This helps better anticipate periods where a BTC drop might follow a NUPL peak.

