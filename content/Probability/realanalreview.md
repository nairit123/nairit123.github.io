---
title: "Part 0: Real Analysis Review"
---

We will state the nesssary definitions and theorems. Feel free to skip this and use as a reference while going through the subsequent notes.

### Definitions.


#### Supremum.

A supremum of a set is the lowest upper bound. More formally, $$\sup(S) = \min(\{u : u\ge S\})$$

#### Infimum.

An infimum of a set is the greatest lower bound. More formally, $$\inf(S) = \max(\{u : u\le S\})$$

#### Supremum Property.

We say a set has the supremum property if every bounded set has a supremum (and infimum). Note that we are abusing notation slightly. The formal definition introduces the notion of a partially ordered set, but for most cases we actually care about here, we can asssume that we are working in a field (or at least a ring) so the supremum property is equivalent to the "infimum property" by existence of additive inverses, and the order is almost always obvious.

#### Metric Space.

We say $(E, \rho)$ is a metric space if $\rho : E\times E\to\mathbb{R}$ and TFH for all $x, y, z\in E$:

1. $\rho(x, x) = 0$
2. if $x\neq y$ then $\rho(x, y) > 0$
3. $\rho(x, y) = \rho(y, x)$
4. $\rho(x, z)\le \rho(x, y) + \rho(y, z)$

#### Bounded Set.

In a metric space $(E, d)$, we say that $A\subseteq E$ is bounded when $x, y\in A\implies d(x, y) < C$ for some fixed $C$.

#### Open Ball.

Given a metric space $(E, d)$, define $B(x, r) = \{y \in E : d(x, y) < r\}$.

#### Open Set.

Given a metric space $(E, d)$, we say that $A\subseteq E$ is open when for all $x\in A$, there exists $\epsilon > 0$ such that $B(x, \epsilon)\subseteq A$.

#### Closed Set.

Given a metric space $(E, d)$, we say that $A\subseteq E$ is closed if $A^c = E\setminus A$ is open. Importantly, note that this property is **not** a negation of the previous property.

#### Convergent Sequence.

A sequence $\{x_n\}\subseteq E$ converges to $x$ if for all $\epsilon > 0$ there exists $N\in\mathbb{N}$ such that $d(x, x_k) < \epsilon$ for all $k\ge N$

#### Sequentially Closed Set.

Given a metric space $(E, d)$, we say that $A\subseteq E$ is sequentially closed if every convergent sequence $\{x_n\}\in A$ converges to a value in $A$.

#### Compact Set.

The formal definition can be unwieldy, but the subsequent theorems will hopefully make this notion more clear.

Given a metric space $(E, d)$, we say that $A\subseteq E$ is compact if every open cover has a finite subcover.

More formally, if $A\subseteq \bigcup_{S\in C} S$ then $A\subseteq \bigcup_{S\in F} S$ where $C$ is a (not necessarily finite or countable) collection of open sets in $E$ and $F$ is a finite subset of $C$.

#### Sequentially Compact Set.

Given a metric space $(E, d)$, we say that $A\subseteq E$ is sequentially compact if every sequence in $E$ has a convergent subsequence .

### Theorems.

These theorems make life easier when working in $\mathbb{R}^n$.

#### Heine-Borel: Compact = closed and bounded for $E=\mathbb{R}^n$.

Note that the metric function is given to be the standard Euclidean distance function. This is a very helpful theorem since it allows us to simplify our definition of compactness signfiicantly (we will usually work in the Euclidean space). This theorem should also not be a surprise since compactness seeks to generalize the notion of closed and bounded to non-Euclidean metric spaces.

#### Compact equivalent to seq. compact

The two different definitions arise from the generalization of compactness onto topological spaces.

#### Closed equivalent to seq. closed

Same as above.

### Examples.

The rationals do not satisfy the supremum property. The reader should convince themselves that the set $$\{x : \mathbb{Q} : q < \sqrt{2}\}$$ does not have a supremum and is bounded.

The reals satisfy the supremum property by construction.

The set $(0, 1)$ is open.

The set $[0, 1]$ is compact.

The set $E$ is always open and closed.

Obviously there is a lot more to real analysis than just this, but we will add onto this as needed.
