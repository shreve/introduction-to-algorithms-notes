Chapter 3. Growth of Functions
==============================

In this chapter, we're looking at the running time of algorithms as the number
of inputs approaches infinity. As such, the functions considered to represent
these will accept a natural number of inputs (`N = {0, 1, 2, ...}`).

## Definitions

**Asymptote**

> A line or function that another function continually approaches, but never
> reaches within a finite distance.

## 3.1 Asymptotic Notation

Let's consider an insertion sort. An insertion sort has a running time of
`an^2 + bn + c` for some constants `a`, `b`, and `c` and a number of inputs to
sort, `n`. Those constants depend on the implementation, but we know that `a` is
non-zero if the implementation is correct, so the `n^2` term is present. As `n`
increases toward the limit, it's the only one that really matters in affecting
the output. As such, we can simplify this representation to `\Theta n^2`.

If an algorithm `f` is `\Theta g`, it means there are some constants where
`f(n) > c_1 g(n)` and `f(n) < c_2 g(n)`. More simply, the growth of `f` keeps
pace with `g`.

If an algorithm `f` is `O g` (Big Oh), it means `f` has an asymptotic upper bound of `g`,
or simply that `f` will never outgrow `c_1 g` where c is any non-zero constant.

If an algorithm `f` is `\Omega g`, it means that `f` has an asymptotic lower
bound of `g` or simply that the growth of`f` will at least match `c_1 g` where c
is any non-zero constant.

Therefore, `f = \Theta g` if and only if `f = O g` and `f = \Omega g`.

### Loose Asymptote Notation

The `\Theta` asymptote is inherently a tight bound because the same base
function must be the upper and lower bound.

It's possible, however, for the use of `O` or `\Omega` notation to be correct,
but a less realistic representation of a function. For example, `2n^2 = O n^2`
is tight, but `2n = O n^2` is not. It's true, but it leaves a lot more room for
error than necessary. There is more notation for this scenario.

If an algorithm `f` is `o g`, it means that for any non-zero value of `c`, `f <
c g` as `n` goes to infinity. To illustrate this, take the case above.

No matter how low the constant is, `2n` is still less.

```
       2n = o n^2
       2n < 0.001 n^2
 2 \Infty < 0.001 \Infty^2
```

There is a case, however, that would lead to `2n^2` being greater

```
2n^2 = o n^2
2n^2 < 0.001 n^2
2 \Infty^2 > 0.001 n^2
```

The opposite definition is the case for `\omega`.

If an algorithm `f` is `\omega g`, it means that for any non-zero value of `c`,
`f > c g` as `n` goes to infinity.

TODO: Copy the tables from the "Comparing functions" section.
TODO: 3.1 Exercises


## 3.2 Standard Notations and Common Functions

### Monotonicity

A monotonic function is one that is one that is either always increasing, or
always decreasing. More mathematically, one could say that if a function is
monotinically increasing, any value of the function is greater than or equal to
any previous value in the series.

### Modular arithmetic

For any integer `a` and any positive integer `n`, `a` mod `n` is the remainder
of the quotient `a/n`. When you remove all the complete multiples of `n` from
`a`, what value is left? This means `0 <= a` mod `n < n`.

If two numbers have the same remainder for the same divisor, they are
equivalent.

If `a mod n == b mod n`, then `a === b` (mod `n`).

For example, `11` mod `5 = 1`, and `16` mod `5 = 1`, so `11 === 16` (mod `5`).

### Polynomials

If a function `f(n)` is the sum of terms equal to `c_i n^k_i` where `c_i` is a
given constant, paired with `k_i`, a given non-negative integer, then `f(n)` is
a polynomial.


TODO: Exponentials, Logarithms, Factorials, Functional iteration, The iterated
log function, Fibonacci numbers
TODO: 3.2 Exercises
