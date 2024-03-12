---
title: "Spectrum of bipartite graphs"
author: "Apurva Nakade"
date: "2024-03-12 11:09:11"
---

**Theorem.**
Let $G$ be a simple graph. 
Let $\lambda_1 \ge \lambda_2 \ge \cdots \ge \lambda_n$ be the eigenvalues of $G$.
$G$ is bipartite if and only if for every $1 \le i \le n$, $\lambda_{i} = -\lambda_{n - (i - 1)}$.

*Proof.*

$G$ is bipartite 

$\iff$ 
$G$ does not contain any odd cycles

$\iff$ 
$G$ does not contain any odd closed walks 

$\iff$ 
For all $r \in \mathbb{N}$, the diagonal entries of $A(G)^{2r+1}$ are all 0

${\color{red} \iff}$ 
For all $r \in \mathbb{N}$, $\mathrm{tr}(A(G)^{2r+1}) = 0$. This is because all the entries of $A(G)$, and hence $A(G)^{2r+1}$, are non-negative. The only way the trace of $A(G)^{2r+1}$ can be 0 is if all the diagonal entries are 0

$\iff$ 
For all $r \in \mathbb{N}$, 
$$\sum \limits_{i = 1}^n \lambda_i^{2r + 1} = 0$$
as the trace of a matrix is the sum of its eigenvalues and the eigenvalues of $A(G)^{2r+1}$ are $\lambda_1^{2r+1}, \lambda_2^{2r+1}, \ldots, \lambda_n^{2r+1}$.

Plugging in $r = 0$, gives us $\lambda_1 \ge 0 \ge \lambda_n$.

If $|\lambda_1| > |\lambda_n|$ then $\lambda_1$ has larger magnitude than all the negative eigenvalues. Therefore, 
$$\sum \limits_{i = 1}^n \lambda_i^{2r + 1} = \lambda_1^{2r + 1} + \mathcal{O}(\lambda_n^{2r + 1}) \overset{r \to \infty}{\longrightarrow} \infty.$$
Similarly, if $|\lambda_1| < |\lambda_n|$ then $\lambda_n$ has larger magnitude than all the positive eigenvalues. Therefore, 
$$\sum \limits_{i = 1}^n \lambda_i^{2r + 1} = \lambda_n^{2r + 1} + \mathcal{O}(\lambda_n^{2r + 1}) \overset{r \to \infty}{\longrightarrow} -\infty.$$
Both of these are contradictions. Therefore, $|\lambda_1| = |\lambda_n|$ and $\lambda_1 = -\lambda_n$.

---

Now we induct on $i$ to show that $\lambda_i = -\lambda_{n - (i - 1)}$. 