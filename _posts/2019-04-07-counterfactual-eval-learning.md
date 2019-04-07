[Tutorial Link](http://www.cs.cornell.edu/~adith/CfactSIGIR2016/)
[Code Repo](https://github.com/yun-zhou-rb/counterfactual_learning/)

# Evaluation I
## Terms
* Deterministic Policy: $y=\pi(x)$, given an x, always predict y.
* Stochastic Policy: $\pi(y\|x)$, given an x, predict an distribtion over y.

Estimate Policy Utility Function:
$U(\pi_0) = \int\int\delta(x,y)\pi_0(y|x)P(x)dxdy$ (1)
## Approach 1 : Reward Predictor
Under policy $\pi_0$, collect dataset $S=((x_1,y_1,\delta_1),...,(x_t,y_t,\delta_t))$
We can learn a predictor $\Delta$(regression function in ML) to predict $\hat{\delta_i}$ given $(x_i,y_i)$.

Now we define a new policy $\pi_1$, the log dataset $S$ can generate $\hat{S}=(((x_1, \hat{y_1}),\hat{\delta_i}(x_1, \hat{y_1})),...,((x_t, y_t),\hat{\delta_i}(x_t, \hat{y_t})))$, where $\hat{y_i}=\pi_1(x_i)$

## Problems with Approach 1
* Selection bias $\pi_0$’s actions are overrepresented, $\Delta$ can be unreliable and biased
* Modeling bias, choice of features and regression functions


## Approach 2: “Model the bias”
DO NOT model the $\Delta$, but replace the $\pi_0$ with $\pi$ in equation (1)
$U(\cancel{\pi}\pi_0) = \int\int\delta(x,y)\cancel{\pi}\pi_0(y|x)P(x)dxdy$
