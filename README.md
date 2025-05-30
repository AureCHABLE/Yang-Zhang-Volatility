# Yang-Zhang-Volatility
The Yang-Zhang volatility is an advanced method for estimating the historical volatility of asset prices. It is widely regarded as one of the most accurate estimators because it combines multiple aspects of price movement and corrects for biases found in simpler volatility estimators.

The Yang-Zhang volatility estimator combines three components:
- Overnight return volatility (close-to-open)
- Open-to-close volatility (intra-day)
- Rogers-Satchell volatility (open-high-low-close)


The Yang-Zhang volatility combines overnight, open-to-close, and Rogers-Satchell estimators:

\[
\sigma^2_{\text{YZ}} = \sigma^2_o + k \cdot \sigma^2_c + (1 - k) \cdot \sigma^2_{rs}
\]

Where:

- \( \sigma^2_o \) = variance of **overnight returns** (log(Open) - log(Previous Close))
- \( \sigma^2_c \) = variance of **open-to-close returns** (log(Close) - log(Open))
- \( \sigma^2_{rs} \) = **Rogers-Satchell estimator**:

\[
\sigma^2_{rs} = \frac{1}{n} \sum_{i=1}^{n} \left[ \ln\left(\frac{H_i}{O_i}\right) \cdot \ln\left(\frac{H_i}{C_i}\right) + \ln\left(\frac{L_i}{O_i}\right) \cdot \ln\left(\frac{L_i}{C_i}\right) \right]
\]

- \( k = \frac{0.34}{1.34 + \frac{n+1}{n-1}} \)
- \( n \) = number of observations (days)

The final Yang-Zhang volatility is:

\[
\sigma_{\text{YZ}} = \sqrt{\sigma^2_{\text{YZ}}}
\]
