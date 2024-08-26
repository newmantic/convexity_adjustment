# convexity_adjustment

In fixed income, convexity adjustment is a technique used to refine the estimate of a bond's price sensitivity to interest rate changes. While duration provides a linear approximation of the price change, convexity accounts for the curvature in the price-yield relationship, providing a second-order adjustment. This is particularly important when the change in interest rates is large, as the price-yield relationship is not perfectly linear.

Duration measures the sensitivity of a bond's price to changes in interest rates. It assumes a linear relationship between price and yield, which is accurate for small changes in yield.
Convexity:

Convexity measures the curvature of the price-yield relationship. It provides an adjustment to the duration estimate, improving the accuracy for larger changes in yield. Positive convexity indicates that as yields decrease, bond prices increase at an increasing rate, and as yields increase, bond prices decrease at a decreasing rate.

The convexity adjustment refines the price change estimate by adding a term that accounts for the bond's convexity.


1. Price Change Approximation Using Duration
The first-order approximation of the price change (ΔP) for a small change in yield (Δy) using duration is:
\Delta P \approx -D_{\text{mod}} \times \Delta y \times P
Where:
D_{mod} is the modified duration.
Δy is the change in yield.
P is the current price of the bond.

2. Price Change Approximation Using Duration and Convexity
To improve the estimate, we include the convexity adjustment. The convexity-adjusted price change (ΔP) is given by:
\Delta P \approx -D_{\text{mod}} \times \Delta y \times P + \frac{1}{2} \times C \times (\Delta y)^2 \times P
Where:
C is the convexity of the bond.
Δy is the change in yield.
P is the current price of the bond.

3. Convexity Calculation
The convexity (C) of a bond is calculated using the following formula:
C = \frac{\sum_{t=1}^{T} \left( t \times (t + 1) \times \frac{CF_t}{(1 + r)^{t+2}} \right)}{\sum_{t=1}^{T} \frac{CF_t}{(1 + r)^t}}
Where:
t is the time in years when each cash flow CF_t is received.
r is the yield to maturity (discount rate).
T is the total number of periods.

Calculate Convexity:
Given the cash flows, times, and yield to maturity, calculate the bond's convexity C.

Estimate Price Change:
Using the bond's modified duration D_{mod}, convexity C, current price P, and a given change in yield Δy, calculate the convexity-adjusted price change.

