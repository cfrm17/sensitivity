# Risk Sensitivity 

Risk sensitivities, also referred to as Greeks, are the measure of a financial instrument’s value reaction to changes in underlying factors. The value of a financial instrument is impacted by many factors, such as interest rate, stock price, implied volatility, time, etc. Sensitivities are risk measures that are more important than fair values. 

Risk sensitivities or Greeks are vital for risk management. They can help financial market participants isolating risk, hedging risk and explaining profit & loss. This presentation gives certain practical insights onto this topic. 

Keywords
Risk sensitivity, Greeks, Delta, Gamma, Vega, Theta, hedging, profit and loss, backbone adjustment.


	Financial Sensitivity Definition
	Financial sensitivity is the measure of a financial instrument’s value reaction to changes in underlying factors.
	The value of a financial instrument is impacted by many factors, such as interest rate, stock price, implied volatility, time, etc.
	Financial sensitivities are also called Greeks, such as Delta, Gamma, Vega, Rho and Theta.
	Sensitivities are risk measures that are more important than fair value.
	They are vital for risk management: isolating risk, hedging risk, explaining profit and loss, etc.

	Delta Definition
	Delta is a first-order Greek that measures the value change of a financial instrument with respect to changes in the underlying asset price.
	Interest rate Delta:
IrDelta=∂V/∂r=(V(r+0.0001)-V(r))/0.0001
where V(r) is the financial instrument value and r is the underlying interest rate entity.
	PV01, or dollar duration, is analogous to interest rate Delta but has the change value of a one-dollar annuity given by
PV01=V(r+0.0001)-V(r)
	Credit Delta is applied to fixed income and credit product represented as
CreditDelta=∂V/∂c  (V(c+0.0001)-V(c))/0.0001
Where c is the underlying credit spread.
	CR01 is analogous to credit Delta but has the change value of a one-dollar annuity given by
PV01=V(r+0.0001)-V(r)
	Equity/FX/Commodity Delta:

Delta=∂V/∂S=(V(1.01S)-V(S))/0.01S
where S is the underlying equity price or FX rate or commodity price

	Vega Definition
	Vega is a first-order Greek that measures the value change of a financial instrument with respect to changes in the underlying implied volatility.
Vega=∂V/∂σ=(V(σ+∆σ)-V(σ))/∆σ
where σ is the implied volatility.
	Only non-linear products, such as options, have Vegas.

	Gamma Definition
	Gamma is a second order Greek that measures the value change of a financial instrument with respect to changes in the underlying price.

Gamma=(∂^2 V)/〖∂S〗^2 =(V(S+0.5∆S)+V(S-0.5∆S)-2V(S))/〖∆S〗^2 

	Theta Definition
	Theta is a first order Greek that measures the value change of a financial instrument with respect to time.

Theta=∂V/∂t=(V(t+∆t)-V(t))/∆t

	Curvature Definition
	Curvature is a new risk measure introduced by Basel FRTB.
	It is a risk measure that captures the incremental risk not captured by the delta risk of price changes in the value of an option.

Curvature=min{V(S+∆W)-V(S)-∆W*Delta,V(S-∆W)-V(S)-∆W*Delta}
where ∆W is the risk weight.

	Option Sensitivity Pattern
	Sensitivity behaviors are critical for managing risk. 
	Gamma
	Gamma behavior in relation to time to maturity.
	Gamma has a greater effect on shorter dated options.
 
	Gamma behavior in relation to moneyness.
	Gamma has the greatest impact on at-the-money options.
	Vega
	Vega behavior in relation to time to maturity shown below.
	Vega has a greater effect on longer dated options.
	Vega behavior in relation to moneyness shown below.
	Vega has the greatest impact on at-the-money options.
	Theta or time decay
	Theta is normally negative except some deeply in-the-money deals.
	Theta behavior in relation to time to maturity shown below.
	Theta has a greater effect on shorter dated options.
	Theta behavior in relation to moneyness shown below.
	Theta has the biggest impact on at-the-money options.

	Sensitivity Hedging
	The objective of hedging is to have a lower price volatility that eliminate both downside risk (loss) and upside profit. 
	It is a double-edged sword.
	The benefit of a broker or investment bank comes from spread rather than market movement. Thus it is better to hedge all risk.
	Delta is normally hedged.
	Vega can be hedged by using options.
	Gamma is hardly hedged in real world.

	Sensitivity Profit & Loss (P&L)
	Hypothetic P&L is the P&L that is purely driven by market movement.
	Hypothetic P&L is calculated by revaluing a position held at the end of the previous day using the market data at the end of the current day, i.e.,
HypotheticalP&L=V(t-1,P_(t-1),M_t )-V(t-1,(t-1,P_(t-1),M_(t-1) )
where t-1 is yesterday;  t is today; P_(t-1) is the position as yesterday;  〖M 〗_(t-1) is yesterday’s market and  〖M 〗_t is today’s market.
	Sensitivity P&L is the sum of Delta P&L, Vega P&L and Gamma P&L.
	Unexplained P&L = HypotheticalP&L – SensitivityP&L.
	Delta P&L:
DeltaP&L=Delta*(S_t-S_(t-1))
Where S_t is today’s underlying price and S_(t-1) is yesterday’s underlying price.
	Vega P&L:
VegaP&L=Vega*(σ_t-σ_(t-1))
Where σ_t is today’s underlying price and σ_(t-1) is yesterday’s underlying price.
	Gamma P&L:
GammaP&L=0.5*Gamma*〖(S_t-S_(t-1))〗^2

	Backbone Adjustment
	Backbone adjustment is an advanced topic in sensitivity P&L.
	It can be best explained mathematically.
	Assume the value of an option is the function of the underlying price S and implied volatility σ, i.e., V=F(S,σ).
	If the implied volatility is a function of the ATM volatility and strike (sticky strike assumption), i.e., σ=σ_A+f(K), the first order approximation of the option value is
∆V=∂F/∂S dS+∂F/〖∂σ〗_A  〖dσ〗_A=DeltaP&L+VegaP&L
Where DeltaP&L=∂F/∂S dS and VegaP&L=∂F/〖∂σ〗_A  〖dσ〗_A
	If the implied volatility is a function of the ATM volatility and moneyness K/S (sticky moneyness or stricky Delta assumption), i.e., σ=σ_A+f(S,K), the first order approximation of the option value is

∆V=∂F/∂S dS+∂F/〖∂σ〗_A  〖dσ〗_A+∂F/∂σ  ∂σ/∂S dS=DeltaP&L+VegaP&L

Where DeltaP&L=(∂F/∂S+∂F/∂σ  ∂σ/∂S)dS and VegaP&L=∂F/〖∂σ〗_A  〖dσ〗_A
	Under sticky moneyness/Delta assumption, the DeltaP&L above has one more item, i.e., ∂F/∂σ  ∂σ/∂S dS that is the backbone adjustment.



References:

https://finpricing.com/lib/EqConvertible.html

https://bitbucket.org/cfrm17/sensitivity/downloads/sensitivity-13.pdf

