# Overview of Supervised Learning

---
Item | Description
--- | ---
Note | [p:12] [para:2] [eq:2.5]
Content | derivative-scalar-by-vector
Authors | [PengjuYan](https://github.com/PengjuYan)
Date | 2015/8/18
Reference | [Wikipedia: Matrix calculus][wikipedia-matrix-calculus]

[wikipedia-matrix-calculus]: https://en.wikipedia.org/wiki/Matrix_calculus

There are 2 _flavors_ of definition of **the derivative of a scalar by a vector** in terms of the form of the resultant vector:

- Row vector: [Wikipedia: Matrix calculus][wikipedia-matrix-calculus], [tirgul3_derivatives.pdf: Derivatives with respect to vectors](http://www.cs.huji.ac.il/~csip/tirgul3_derivatives.pdf)
- Column vector: [IFEM.AppF.pdf: Matrix Calculus](http://www.colorado.edu/engineering/cas/courses.d/IFEM.d/IFEM.AppF.d/IFEM.AppF.pdf), [onlinelibrary: Differentiation with respect to a vector](http://onlinelibrary.wiley.com/doi/10.1002/0471705195.app3/pdf)

This book follows the latter, i.e., the column vector form:

\begin{equation}
\frac{\partial{y}}{\partial{\mathbf{x}}} = \begin{bmatrix} \frac{\partial y}{\partial x_1} \\ \frac{\partial y}{\partial x_2} \\ \vdots \\ \frac{\partial y}{\partial x_n} \end{bmatrix}
\end{equation}

This can also be verified by equation (3.14) on page 45.

---
Item | Description
--- | ---
Note | [p:15] [para:-2]
Content | knn-degrees-of-freedom
Authors | [PengjuYan](https://github.com/PengjuYan)
Date | 2015/8/20
Reference | [Wikipedia: Degrees of freedom][wikipedia-degrees-of-freedom]

[wikipedia-degrees-of-freedom]: https://en.wikipedia.org/wiki/Degrees_of_freedom_%28statistics%29

In the paragraph of interest, it is said that:

> ... we will see that the _effective_ number of parameters of $k$-nearest neighbors is $N/k$ ... To get an idea of why, note that if the neighborhoods were nonoverlapping, there would be $N/k$ neighborhoods and we would fit one parameter (a mean) in each neighborhood.

In order to understand this paragraph quantitatively, we may need to refer to [Wikipedia: Degrees of freedom][wikipedia-degrees-of-freedom] and equation (3.50) on page 68. In many regression tasks, including $k$-nearest-neighbors, the prediction on training data can be given by a linear combination of target values of the training samples:

\begin{equation}
\hat{\mathbf{y}} = \mathbf{H}\mathbf{y}
\end{equation}

A general definition of the **effective degrees of freedom** is given by the trace of the **hat** matrix $\mathbf{H}$:

\begin{equation}
\mathrm{tr}(\mathbf{H}) = \sum_{i} h_{ii}
\end{equation}

In a $k$-nearest-neighbor fit, each row of the hat matrix $\mathbf{H}$ contains exactly $k$ non-zero cells with the value of $1/k$, and the diagonal cell is always $1/k$ because the nearest neighbor of each data sample is of course itself. Therefore, the trace of the hat matrix is naturally $N/k$.

