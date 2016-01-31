# Special Cases for Matrix Inversion / Linear Solvers
A repository of matrices with special inversion properties. We are interested in matrices A, such that solving Ax = B has computational complexity under O(n^3). These methods look at both exact and approximate direct solvers.

[NOTE: This page is a work in progress and will never be a finished resource. If you identify any method that should be included please push to the repository. Thank you.]

## Diagnol matrices O(n)
Inverse is a diagnol matrix with each element being the inverse of the corresponding original diagnol element. 

## Block diagnol matrices O(\sum_i n_i^3)
The inverse is also is a block diagnol matrix with each block being the inverse of the corresponding block of the original matrix

## Low rank matrices
These matrices have a fixed rank m << n. In such cases we endeavour to utilise the fact that less singular have to be inverted.

### Nystrom's method O(nm^2)
This method uses subsampling to of the matrix under consideration in order to approximate the eigen spectrum of the full matrix. A great resource for those interested in Nystrom's method is [Nicholas Arcolano's Thesis](http://arcolano.com/wp-content/uploads/2013/10/arcolano2011thesis.pdf).

## Toeplitz matrices O(nlog(n))
Toeplitz matrices have a special structure of their elements whereby each consecutive row is equal to it's previous row but shifted one element to the right. This isn't exactly a rigourous definition but for now I will leave it to [Wikipedia](https://en.wikipedia.org/wiki/Toeplitz_matrix) to explain in greater depth. Check out [A Superfast Algorithm for Toeplitz Systems of Linear Equations](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.116.3297&rep=rep1&type=pdf) for a full description of the solver.

## Vandamonde matrices O(c)
The vandermonde matrix is an interesting matrix where each column is a vector raised to a higher elementwise power. Again for a more formal description check out [Wikipedia](https://en.wikipedia.org/wiki/Vandermonde_matrix). There is a closed form solution for the matrix [inverse](http://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19660023042.pdf) and the determinant is also easily found.

## Hierarchical matrices

### HODLR matrices O(nlog(n))

### Fast Multipole Methods O(nm^2 or nlog(1/\eps))

