# How to hedge
At first,if the value of call option is $C$ at time $t_0$, then the buyer would pay $C_0$ to the writer,
who will buy $A_0$ units of assets(price $S_0$) using $C_0$ plus cash $D_0$
 borrowed from the bank. Of course,the writer will have to pay the interest of cash $D$ to the
 bank with the interest rate $r$. We have:
 $$ A_0S_0=C_0+D_0$$

 In the middle, trader (namely,writer becomes trader) monitors the asset price $S_t$ at time $t$, and calculates
 a delta hedge $\delta=\frac{\partial C}{\partial S} $. If $\delta >0$, trader will hold $\delta$
 units of assets at the price $S_t$ via borrowing money $\delta S_t$ with the interest rate $r$;
 if $\delta<0$, trader will short sell $\delta$ units of assets at the price $S_t$,then deposite the money
 $\delta S_t$ in the bank who pay the interests to trader with rate $r$.
 In the real life, every trasaction needs cost. It is reasonalbe to only carry out hedging when
 $$|\frac{\partial^2 C}{\partial S^2}|>\epsilon$$
 where,$\epsilon$ is a threshold value in the industry(I guess).

 At last, holder(namely,buyer becomes holder) may exercise the option if $S_T>E$.
 Writer has to pay $S_T-E$ to holder. At this time, writer should own 1 unit of asset throught carrying out
 hedging, but pay back $E$(including the interest,also given $r$,$\sigma$) to the bank. so writer could sell the asset and get money
 $S_T$,which is split two parts, $E$ for the bank and $S_T-E$ for the holder.

 From another view, the above three items can be put together in one basket, which could be called a portfolio $B$:
*. item assets
*. item cashs(invested in a bank)
*. options
 
In one hand, it could be interpreted that the value change of $B$ must equal the correponding growth suppiled by the risk-free interest
rate,this says,
$$  B_{t+\Delta{t}}-B_{t} =r\Delta{t}B_t$$

 On the other hand,if we define a combination of asset and cash as a portfilio $ \Pi=(AS,D)$,
 it could also be interpreted that $\Pi$ replicate the risk of options $C$:
 $$ \Delta(\vee-\Pi)=r\Delta{t}(\vee-\Pi)$$
 which means $ \Delta(\vee-\Pi)$ is non-random. Could we suppose the above example is one case of this formula,this is
 ${\vee-\Pi}=0$ at time $t_0$? I think so.

 since $\Lambda$ is also a random based on asset price $S$, so now pay me money $C_0$ for the risk
 with price volatility $\sigma$(that means I have took the worst situation in consideration). This intuitively
 leads to Binomial optional pricing method,given the upper and lower prices.
