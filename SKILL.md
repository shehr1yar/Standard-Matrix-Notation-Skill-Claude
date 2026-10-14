---
description: Format matrices and vectors using standard mathematical
  notation instead of programming-language list notation. Use for linear
  algebra, determinants, inverses, row reduction, eigenvalues, and
  worked math examples.
name: standard-matrix-notation
---

# Standard Matrix Notation

## Purpose

When explaining mathematics, write matrices in conventional mathematical
notation. Do **not** represent a matrix as a nested programming-language
list such as `[[3, -3, 4], [2, -3, 4], [0, -1, 1]]` in the mathematical
explanation.

## Core rules

1.  **Use LaTeX for every matrix or vector.** Prefer
    `\begin{bmatrix} ... \end{bmatrix}` for matrices and column vectors.
2.  **Never use nested square-bracket lists as the main representation
    of a matrix.** Avoid forms like `A = [[1, 2], [3, 4]]`, even in
    headings, summaries, or final answers.
3.  **Display important matrices on their own line** using display math
    (`\[ ... \]`) so rows and columns are easy to distinguish.
4.  **Keep row and column alignment correct.** Separate columns with `&`
    and rows with `\\`.
5.  **Use standard notation for related objects:** determinants with
    vertical bars, transposes with `^{T}`, inverses with `^{-1}`, and
    the identity matrix with `I`.
6.  **For multi-step calculations, show the mathematical steps
    clearly**, rather than compressing everything into one line.
7.  **If a matrix is too wide**, split the calculation across lines
    using `aligned`, or explain the steps separately. Do not switch to
    list notation to save space.
8.  **When referring to entries**, use notation such as (a\_{ij}), not
    list indices such as `A[0][1]`, unless explicitly explaining code.
9.  **When showing augmented matrices for row reduction**, use an
    augmented-matrix layout, for example: \[ `\left[\begin{array}{cc|cc}
    1 & 0 & 2 & 1 \\
    0 & 1 & -1 & 3
    \end{array}\right]`{=tex}. \]
10. **Keep explanations beginner-friendly.** After displaying a
    mathematical expression, explain what it means in plain language
    when helpful.

## Preferred formatting examples

### Defining a matrix

**Avoid:**

`A = [[3, -3, 4], [2, -3, 4], [0, -1, 1]]`

**Use:**

\[ A =
```{=tex}
\begin{bmatrix}
3 & -3 & 4 \\
2 & -3 & 4 \\
0 & -1 & 1
\end{bmatrix}
```
\]

### Showing a determinant calculation

**Avoid:**

`|A| = 3(-3 + 4) + 3(2 - 0) + 4(-2 - 0) = 1`

**Use:**

\[
```{=tex}
\begin{aligned}
\det(A)
&= 3(-3+4)+3(2-0)+4(-2-0) \\
&= 3+6-8 \\
&= 1.
\end{aligned}
```
\]

Use (`\det`{=tex}(A)) or (\|A\|) consistently. For a matrix determinant,
vertical bars are acceptable mathematical notation; do not confuse them
with programming syntax.

### Showing the cofactor matrix, adjugate, and inverse

For a worked example, display each object as a proper matrix:

\[ C =
```{=tex}
\begin{bmatrix}
1 & -2 & -2 \\
-1 & 3 & 3 \\
0 & -4 & -3
\end{bmatrix}
```
\]

\[ `\operatorname{adj}`{=tex}(A)=C\^T=
```{=tex}
\begin{bmatrix}
1 & -1 & 0 \\
-2 & 3 & -4 \\
-2 & 3 & -3
\end{bmatrix}
```
\]

Then show the inverse in standard notation:

\[ A\^{-1}=`\frac{1}{\det(A)}`{=tex}`\operatorname{adj}`{=tex}(A) =
```{=tex}
\begin{bmatrix}
1 & -1 & 0 \\
-2 & 3 & -4 \\
-2 & 3 & -3
\end{bmatrix}
```
, `\qquad `{=tex}`\det`{=tex}(A)=1. \]

### Showing a column vector

\[ `\mathbf{x}`{=tex} =
```{=tex}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3
\end{bmatrix}
```
\]

### Showing a system of equations as a matrix equation

\[
```{=tex}
\begin{bmatrix}
2 & 1 \\
-1 & 3
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
```
=
```{=tex}
\begin{bmatrix}
5 \\
4
\end{bmatrix}
```
\]

## When code notation is allowed

Only use nested lists or array syntax when the user specifically asks
about programming, data structures, NumPy, Python, or how to enter a
matrix into code. Even then, show the standard mathematical matrix first
when it helps clarify the concept.

## Final check before responding

Before sending a math explanation, verify:

-   Every matrix is displayed in standard mathematical notation.
-   Rows and columns are visually aligned.
-   Important matrices are not buried inside a sentence as nested lists.
-   Multi-step work is broken into readable lines.
-   No matrix has accidentally been transposed or had its entries
    rearranged while formatting.
