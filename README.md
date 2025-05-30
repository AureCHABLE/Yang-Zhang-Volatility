# Yang-Zhang-Volatility
The Yang-Zhang volatility is an advanced method for estimating the historical volatility of asset prices. It is widely regarded as one of the most accurate estimators because it combines multiple aspects of price movement and corrects for biases found in simpler volatility estimators.

The Yang-Zhang volatility estimator combines three components:
- Overnight return volatility (close-to-open)
- Open-to-close volatility (intra-day)
- Rogers-Satchell volatility (open-high-low-close)


The Yang-Zhang volatility combines overnight, open-to-close, and Rogers-Satchell estimators:

![equation](https://latex.codecogs.com/svg.image?\[\sigma^2_{\text{YZ}}=\sigma^2_o&plus;k\cdot\sigma^2_c&plus;(1-k)\cdot\sigma^2_{rs}\])

Where:

- ![equation](https://latex.codecogs.com/svg.image?\(\sigma^2_o\)=) variance of **overnight returns** ![equation](https://latex.codecogs.com/svg.image?(log(Open)-log(Previous&space;Close)))
- ![equation](https://latex.codecogs.com/svg.image?\(\sigma^2_c\)=)variance of **open-to-close returns** ![equation](https://latex.codecogs.com/svg.image?(log(Close)-log(Open)))
- ![equation](https://latex.codecogs.com/svg.image?\(\sigma^2_{rs}\)=) **Rogers-Satchell estimator**:

![equation](https://latex.codecogs.com/svg.image?\[\sigma^2_{rs}=\frac{1}{n}\sum_{i=1}^{n}\left[\ln\left(\frac{H_i}{O_i}\right)\cdot\ln\left(\frac{H_i}{C_i}\right)&plus;\ln\left(\frac{L_i}{O_i}\right)\cdot\ln\left(\frac{L_i}{C_i}\right)\right]\])

- ![equation](https://latex.codecogs.com/svg.image?\(k=\frac{0.34}{1.34&plus;\frac{n&plus;1}{n-1}}\))
- ![equation](https://latex.codecogs.com/svg.image?\(n\)=number&space;of&space;observations(days))

The final Yang-Zhang volatility is:

![equation](https://latex.codecogs.com/svg.image?\[\sigma_{\text{YZ}}=\sqrt{\sigma^2_{\text{YZ}}}\])
