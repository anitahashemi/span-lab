# Span Lab

A visual exploration of linear independence using Python.


## Why are these vectors linearly independent?

Two vectors are linearly independent if the only solution to

$$
a\mathbf{u} + b\mathbf{v} = \mathbf{0}
$$

is $a = b = 0$.

For our vectors,

$$
\mathbf{u} =
\begin{bmatrix}
2 \\
1
\end{bmatrix},
\qquad
\mathbf{v} =
\begin{bmatrix}
1 \\
2
\end{bmatrix}
$$

the equation becomes

$$
2a + b = 0,
\qquad
a + 2b = 0.
$$

From the first equation, $b = -2a$. Substituting into the second:

$$
a + 2(-2a) = -3a = 0.
$$

Therefore $a = 0$ and $b = 0$. The vectors are linearly independent.

Geometrically, they point in different directions, so their linear combination
spans the entire plane. 


## Then what changes when the vectors are dependent?

$$
\mathbf{u} =
\begin{bmatrix}
2 \\
1
\end{bmatrix},
\qquad
\mathbf{v} =
\begin{bmatrix}
4 \\
2
\end{bmatrix}.
$$

Since $\mathbf{v} = 2\mathbf{u}$,

$$
2\mathbf{u} - \mathbf{v} = \mathbf{0}.
$$

We found a solution with nonzero coefficients: $a = 2$ and $b = -1$.
Therefore the vectors are linearly dependent.

Every linear combination simplifies to

$$
a\mathbf{u} + b\mathbf{v} = (a + 2b)\mathbf{u}.
$$

All combinations are on the same line from the origin. 