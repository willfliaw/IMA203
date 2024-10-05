# Synthesis

## Introduction to markov random fields

- Definition and simulation of a Markov random field
  - Set of sites: $S = \{s\} \subset \mathbb{Z}^d$ (discrete and finite), $d$ dimensiton of the space
  - Descriptor: $x_s \in E = \begin{cases}\{0..255\} & \text{(gray-levels)}\\ \{0..q-1\} & \text{(labels)} \\ \mathbb{R}\end{cases}$
  - Neighboring system: $\mathcal{V}=\{\mathcal{V}_s\}_{s\in S}$
    - Neighborhood: $\mathcal{V}_s = \{t \mid s \not\in \mathcal{V}_s, t \in \mathcal{V}_s \iff s \in \mathcal{V}_t \}$
    - Type:
      - 4-connectivity: cliques of order $1, 2$
      - 8-connectivity: cliques of order $1..4$
  - Set of cliques: $\mathcal{C} = \{c\}_{c\in\mathcal{V}}$
    - $c=\begin{cases}\text{singleton} & \text{card}(c) = 1\\\forall r \neq s \in c \Rightarrow r, s \text{ neighbours} &\text{card}(c) \geq 2\end{cases}$
    - Set of cliques or order/cardinality $k$: $\mathcal{C}_k$
    - Clique potential: $U_c(x)=U_c(x_s, s \in c)$
  - Global energy: $U(x) = \sum\limits_{c\in\mathcal{C}}U_c(x)$
  - Local energy: $U_s(x_s \mid x_t, t\in\mathcal{V}_s) = \sum\limits_{c\in\mathcal{C}\mid s\in\mathcal{c}}U_c(x_s, \mathcal{V}_s)$
- Probabilistic modelling of the image
  - Random field: $X = \{X_s\}_{s \in S}$
  - Random variable associated with $s$: $X_s$
  - Realisation (image): $x = \{x_s\}_{s \in S} = \{x_s\} \cup x^s$
  - Space of realisations: $\Omega = E^{|S|}$
  - Markov random field: A random field $X$ is a Markov field if the local conditional probability at a site depends only on the configuration of the neighborhood of the considered site
    - $P(X_s = x_s \mid X^s = x^s)=P(X_s=x_s \mid x_t, t\in \mathcal{V}_s)$
  - Gibbs field: $P(X=x)=\frac{1}{Z}\exp(-U(x)), Z=\sum\limits_{x\in\Omega}\exp(-U(x))$
    - $U (x) \propto \frac{1}{P (X = x)}$
  - Hammersley-Clifford theorem: for the same $\mathcal{V}$, $X$ is a Markov field, and $P(X = x) > 0\quad  \forall x \in \Omega \iff X$ is a Gibbs field
    - Suppositions
      - $S$ is finite or countable,
      - The neighborhood system $\mathcal{V}$ is bounded,
      - The state space $E$ is discrete.
  - Conditional probability: $P(X_s = x_s \mid X^s=x^s)=\frac{1}{Z^s}\exp(-U_s(x_s \mid \mathcal{V}_s)), Z^s=\sum\limits_{x_s\in E}\exp(-U_s(x_s \mid \mathcal{V}_s))$
- MRF Sampling
  - Gibbs's sampler
