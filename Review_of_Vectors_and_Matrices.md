# Review of Statistics and Matrices
### 30/09/24
### Dr Fazil Baksh

## Definitions
### A Matrix
Matrix = Any rectangular array of numbers, complex numbers or functions
For Example:

$` A = \begin{bmatrix}
 a_{1,1}& a_{1,2} & ... & a_{1,m} \\
 a_{2,1}& a_{2,2} & ... & a_{2,m} \\
 ...& ... & ... & ... \\
 a_{n,1}& a_{n,2} & ... & a_{n,m} \\
\end{bmatrix}
`$

Where **A** is a matrix of n rows and m column with element $` a_{i,j} `$ in the *ith* row and *jth* row
**A** is a matrix to be of order (or dimension) n x m
Convention dictates that rows are listed first, then columns

**A** is a square matrix if m=n. In a square matrix, the elements {$` a_{1,1} `$,$` a_{2,2} `$,...,$` a_{n,n} `$}

The size of the dataset is really important. In most cases, this is a pretty good place to start when it comes to debugging. It should be noted that R will not throw up an error if incorrect Matrix sizes are used in, for example, elementary operations or Matrix multiplication. Further R related comments will go in a seperate document for the sake of clarity

### Special Matrices
Special Matricesa have a specific combination of zeros and "patterns". It is desirable to use computational techniques to convert the source data matrices into these special matrices as it makes it easier to work with and also reduces computational workload

#### Diagonal Matrix
Matrices that only have values in the diagonal

$` A = \begin{bmatrix}
 2 & 0 & 0 \\
 0 & 3 & 0 \\
 0 & 0 & 4 \\
\end{bmatrix}
`$

#### Upper Triangle Matrix
Matrices that only have values in the Upper Diagonal

$` A = \begin{bmatrix}
 1 & 3 & 2 \\
 0 & 3 & 4 \\
 0 & 0 & 4 \\
\end{bmatrix}
`$

#### Lower Triangle Matrix
Matrices that only have values in the Lower Diagonal

$` A = \begin{bmatrix}
 2 & 0 & 0 \\
 3 & 1 & 0 \\
 4 & 6 & 0 \\
\end{bmatrix}
`$

#### Scalar Matrix
Matrices that only have values in the diagonal and the values are all the same

$` A = \begin{bmatrix}
 2 & 0 & 0 \\
 0 & 2 & 0 \\
 0 & 0 & 2 \\
\end{bmatrix}
`$

#### Identity Matrix
Matrices that only have the value 1 in the diagonal

$` A = \begin{bmatrix}
 1 & 0 & 0 \\
 0 & 1 & 0 \\
 0 & 0 & 1 \\
\end{bmatrix}
`$

#### Zero Matrix
Matrices that are filled with zeros

$` A = \begin{bmatrix}
 0 & 0 & 0 \\
 0 & 0 & 0 \\
 0 & 0 & 0 \\
\end{bmatrix}
`$

#### Equal Matrices
If Matrices A and B are exactly identical, i.e have the number of rows and columns and also have identical values within the matrices

### Elementary Operations

#### Addition
Matrix addiction (and subtraction) is only possible for matrices of the same (see definition of matrix)
The resulting Matrix is also of the same order

#### Multiplication
##### By Scalar:
**R** = *k*x**A**
In the above example, Matrix **R** is the result of multiplying every element of Matrix **A** by scalar factor k.
Matrix multiplication is distributive. For all rules, see [Matrix Reference Sheet]()

##### By Matrix
Matrix multiplication is only possible under very specific circumstances. If Matries A (of order a,b) and B (of order x,y) are to be multiplied, b and x must be the same. The resulting matrix will be of size a,y.

$`  A = \begin{bmatrix}
 2 & 1 & 3 \\
 1 & 4 & 1 \\
\end{bmatrix}, B = \begin{bmatrix}
2 & 1 \\
0 & 3 \\
1 & 2 \\
\end{bmatrix} `$

$` AB = \begin{bmatrix}
(2*2)+(1*0)+(3*1) & (2*1)+(1*3)+(3*2) \\
(1*2)+(4*0)+(1*1) & (1*1)+(4*3)+(1*2) \\
\end{bmatrix} `$

$` = \begin{bmatrix}
7 & 11 \\
3 & 15 \\
\end{bmatrix} `$

### Matrix Functions
A matrix function maps a matrix to another matrix
#### Power Function
