# base::outer


## Description

Generate an **outer product** of the array `X` and array `Y` applying
with a function.

$$
A = 
\begin{bmatrix}
   a_1 \\
   a_2 \\
   a_3 
\end{bmatrix}
\otimes
\begin{bmatrix} 
    b_1 & b_2 & b_3 
\end{bmatrix}
=
\begin{bmatrix}
    a_1b_1 & a_1b_2 & a_1b_3 \\
    a_2b_1 & a_2b_2 & a_2b_3 \\
    a_3b_1 & a_3b_2 & a_3b_3
\end{bmatrix}
$$

## Arguments

``` r
base::outer(
    X = c(1, 2, 3),  # typically a vector or array
    Y = c(2, 3, 4),  # typically a vector or array
    FUN = "*"  # a function apply to the arrays, default is "*"
)
```

## Examples

``` r
base::outer(
    X = c(letters[1:3]),
    Y = c(letters[1:3]),
    FUN = function(x, y) paste(x, y, sep = "-")
)
```

         [,1]  [,2]  [,3] 
    [1,] "a-a" "a-b" "a-c"
    [2,] "b-a" "b-b" "b-c"
    [3,] "c-a" "c-b" "c-c"
