[Slides](http://videolectures.net/site/normal_dl/tag=73137/kdd2010_beygelzimer_langford_lte.pdf)
[videos](http://videolectures.net/kdd2010_beygelzimer_langford_lte/?q=lte#)

# The Problem Define

Learn a good policy ($  x_t \rightarrow r(a_t ) $ )for choosing actions given context ($ x_t $).

Which is equivlant to minimize Regret 

$$Regret = \sum r(\pi(x_t)) - \sum r(a_t)$$ , where pi(x_t) is the optimal policy


## Follow the Leader Algorithm(FTL)
let $\pi_t$ be the policy maximizing all previous rounds $(x, a, r(a))$,
where $\pi_t(x)=a$
not optimal since the expected regret of FTL can be $O(T)$

#EFTL-$\tau$ alogrithm
* For first $\tau$ rounds, choose action uniformly
* for $T-\tau$ rounds, choose actin FTL
regret ~ $O(T^{2/3}(Kln(\pi)^{1/3})$

#Exp4
