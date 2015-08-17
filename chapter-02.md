# Overview of Supervised Learning

---
Item | Description
--- | ---
Note | [p:12] [para:2] [eq:2.5]
Content | derivative-scalar-by-vector
Authors | [PengjuYan](https://github.com/PengjuYan)
Date | 2015/8/17
Reference | [Wikipedia: Matrix calculus][wikipedia-matrix-calculus]

[wikipedia-matrix-calculus]: https://en.wikipedia.org/wiki/Matrix_calculus

There are 2 _flavors_ of definition of **the derivative of a scalar by a vector** in terms of the form of the resultant vector:

- Row vector: [Wikipedia: Matrix calculus][wikipedia-matrix-calculus], [tirgul3_derivatives.pdf: Derivatives with respect to vectors](http://www.cs.huji.ac.il/~csip/tirgul3_derivatives.pdf)
- Column vector: [IFEM.AppF.pdf: Matrix Calculus](http://www.colorado.edu/engineering/cas/courses.d/IFEM.d/IFEM.AppF.d/IFEM.AppF.pdf), [onlinelibrary: Differentiation with respect to a vector](http://onlinelibrary.wiley.com/doi/10.1002/0471705195.app3/pdf)

This book follows the latter, i.e., the column vector form:

\begin{equation}
\frac{\partial{y}}{\partial{\mathbf{x}}} = \begin{bmatrix} \frac{\partial y}{\partial x_1} \\ \frac{\partial y}{\partial x_2} \\ \vdots \\ \frac{\partial y}{\partial x_n} \end{bmatrix}
\end{equation}

This can also be verified by equation (3.14) in page 45.

