---
kernelspec:
  name: python3
  display_name: 'Python 3'
---
# Non-Convex Optimization

## Annealing 

:::{tip}
Key idea: **Accept a bad move with some probability**
:::

:::{prf:example}
**(Metropolis)**
Given current solution $x$ with cost $f(x)$, and a candidate neighbor $x'$. Let 
\begin{equation}
    \Delta = f(x')-f(x)
\end{equation}
- If $\Delta < 0$: *always accept*
- If $\Delta \geq 0$: accept with probability $\exp(-\Delta /T)$

```{code-cell}
import numpy as np 

x = 1.7 
best_x, best_f = x, x**2
```
:::


