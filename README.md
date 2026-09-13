# Span Lab

Built in an evening to better understand linear independence. 

I explored independent and dependent vectors in 2D and 3D using
Python visualizations, then checked the results with algebraic proofs.


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

# 3D Visualization

In 3D, three vectors pointing in different directions are not necessarily linearly independent.
The first two independent vectors span a plane through the origin. For all three to be independent, the third vector must point outside that plane.
If it lies in the plane, it can be written as a linear combination of the first two.


## Checking the independent case

For the first example, I used these three vectors:

$$
\mathbf{u} =
\begin{bmatrix}
1 \\
0 \\
1
\end{bmatrix},
\qquad
\mathbf{v} =
\begin{bmatrix}
0 \\
1 \\
1
\end{bmatrix},
\qquad
\mathbf{w} =
\begin{bmatrix}
1 \\
1 \\
0
\end{bmatrix}.
$$

The plot looks like their combinations fill a 3D region, but I
wanted to check this algebraically too.

I started with

$$
a\mathbf{u} + b\mathbf{v} + c\mathbf{w} = \mathbf{0}.
$$

For the vectors to be independent, this equation should only work
when all three coefficients are zero.

Looking at each coordinate, I get

$$
\begin{aligned}
a + c &= 0, \\
b + c &= 0, \\
a + b &= 0.
\end{aligned}
$$

The first two equations tell me that $a = -c$ and $b = -c$.
Putting these into the last equation gives

$$
-c-c = -2c = 0.
$$

So $c = 0$, which also makes $a = 0$ and $b = 0$.

Since there is no nonzero choice of coefficients that makes the
sum zero, these vectors are linearly independent. Together,
they span all of 3D space.

## Checking the dependent case

Next, I kept $\mathbf{u}$ and $\mathbf{v}$ the same and changed
the third vector to their sum:

$$
\mathbf{w} = \mathbf{u} + \mathbf{v} =
\begin{bmatrix}
1 \\
1 \\
2
\end{bmatrix}.
$$

This makes the proof much shorter. Rearranging gives

$$
\mathbf{u} + \mathbf{v} - \mathbf{w} = \mathbf{0}.
$$

Here the coefficients are $1$, $1$, and $-1$. They aren't all zero,
so this is enough to show that the vectors are linearly dependent.

I can also rewrite any combination as

$$
a\mathbf{u} + b\mathbf{v} + c\mathbf{w}
= (a+c)\mathbf{u} + (b+c)\mathbf{v}.
$$

So anything I make using all three vectors can already be made
using just $\mathbf{u}$ and $\mathbf{v}$. The third vector adds
nothing to their span.

This explains why the dots stayed on a plane in the plot.
One thing I learned here is that three arrows can point in
different directions and still be dependent. The third vector
has to leave the plane spanned by the first two independent
vectors for all three to be independent.