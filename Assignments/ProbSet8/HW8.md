Yaghoub Shahmari - 98100883

# Problem 7.2:

## a.
$p_k = \frac{N-1}{N}\delta(k-1)+\frac{1}{N}\delta(k-(N-1))$

## b.
$q_k = \frac{\delta (k-1)+\delta (k-(N-1))}{2}$

## c.

$e_{jk}=\frac{\delta_{j,1}\delta_{k,N-1}+\delta_{j,N-1}\delta_{k,1}}{2}$

$r=\Sigma_{j,k}\frac{jk(e_{jk}-q_j q_k)}{\sigma^2}$

$\sigma^2 = \Sigma_k = k^2q_k-(\Sigma_kkq_k)^2$

$\Rightarrow r=\frac{(N-1)-(\frac{N^2}{4})}{\frac{1+(N-1)^2}{2}-(\frac{N^2}{4})}=-1$

## d.

All of the nodes with small degree are connected to the nodes with large degree. Therefore, the network is disassortative.

# Problem 7.4:

# a.
In the Erdős-Rényi G(N,L) model, the probability that there is a link between nodes i and j is given by:

$e_{ij} = \frac{L}{\binom{N}{2}}$

Where $\binom{N}{2}$ is the total number of possible links. 

The conditional probability that there is a link between i and j given there is a link between l and s is:

$e_{ij}|e_{ls} = \frac{L-1}{\binom{N}{2}-1}$

# b.
For small networks, the ratio of these probabilities is: 

$\frac{e_{ij}|e_{ls}}{e_{ij}} = \frac{\frac{L-1}{\binom{N}{2}-1}}{\frac{L}{\binom{N}{2}}} \approx 1$

For large networks (as N → ∞), this ratio approaches 1. 

# c.
In the Erdős-Rényi G(N,p) model, the probabilities are:

$e_{ij} = p$ 

$e_{ij}|e_{ls} = p$

These probabilities are independent. 

The ratio is always 1, regardless of network size.

Implications for small networks:

- Using the G(N,L) model introduces correlations between link existence probabilities that are not present in the G(N,p) model.

- For model validation or simulation of small real-world networks, the G(N,p) model may not capture these correlations appropriately.

- The ratio of conditional to unconditional probabilities being ≈1 in G(N,L) for small N indicates significant correlations.

- The G(N,L) model may better represent the linking process in small real networks.

So for modeling and analyzing small networks, using the G(N,L) over G(N,p) model is likely more appropriate to account for degree correlations not present in G(N,p).