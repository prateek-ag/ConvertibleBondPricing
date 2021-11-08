# Pricing a Convertible Bond
An implementation John Hull's binomial tree model to estimate the price of convertible bonds, as described in his textbook **Options, Futures and Other Derivatives**.

The model assumes that the underlying stock's price follows a geometric brownian motion, which can be represented by the standard binomial tree. By assigning a value for the convertible at the last timestep and utilizing the rollback methodology, the model allows us to estimate the present value of the convertible bond.

The model requires a few key inputs:
- Valuation Date
- Maturity Date
- Coupon
- Payment Frequency
- Risk Free Rate
- Stock volatility 
- Default intensity
- Current stock price
- Conversion Ratio
- Recovery Value (in case of default)

My implementation of the model makes the following key assumptions:
- The underlying stock does not pay any dividends
- The bond instrument does not have any put/call features
- The bond instrument is continuously convertible
- Continuous compounding of the risk free rate
