---
layout: Blog
title: Free Algebras
---

# Free Algebras

## 1. Words and Free Monoid

Let \( X = \{ x_i \mid i \in I \} \) be a nonempty (possibly indexed) set.

- A **word** over \( X \) is a finite sequence of elements from \( X \), written as  
  \( x_{i_1} x_{i_2} \cdots x_{i_m} \).
- The **empty word** is denoted by \( 1 \) and has length 0.
- Define multiplication by juxtaposition:  
  \( (x_{i_1} \cdots x_{i_m}) \cdot (x_{j_1} \cdots x_{j_n}) := x_{i_1} \cdots x_{i_m} x_{j_1} \cdots x_{j_n} \)

With this multiplication, the set of all words forms a **monoid** (with identity 1), denoted \( X^* \), called the **free monoid** on \( X \).

Each element \( w \in X^* \) (i.e., a word) can be uniquely written as  
\( w = x_{i_1}^{k_1} x_{i_2}^{k_2} \cdots x_{i_r}^{k_r} \)  
with \( x_{i_j} \in X \), \( k_j \in \mathbb{N} \), and \( x_{i_j} \neq x_{i_{j+1}} \).

### Equality in \( X^* \)

Two words \( w, w' \in X^* \) are equal if they consist of the **same sequence of symbols in the same order**.

---

## 2. Free Algebra

Let \( \mathbb{F} \) be a field. The **free algebra** on \( X \) over \( \mathbb{F} \), denoted \( \mathbb{F} \langle X \rangle \), is defined as the **monoid algebra** \( \mathbb{F}[X^*] \).

### Elements

An element \( f \in \mathbb{F} \langle X \rangle \) is a finite linear combination of words:  
\[
f = \sum_{i=1}^m \lambda_i w_i, \quad \lambda_i \in \mathbb{F},\; w_i \in X^*
\]

Two such expressions are equal if the coefficients of equal words (after combining) match.

### Operations

- **Addition:** Combine like monomials
- **Scalar multiplication:**  
  \( \lambda f = \sum \lambda \lambda_i w_i \)
- **Multiplication:** Extended bilinearly:  
  \( (\lambda w)(\mu v) = (\lambda \mu)(wv) \), where \( wv \) is concatenation in \( X^* \)

### Algebra Axioms

\( \mathbb{F} \langle X \rangle \) is an associative unital algebra over \( \mathbb{F} \), satisfying:

- Associativity (addition and multiplication)
- Distributivity
- Scalar compatibility
- Identity: \( 1 \in \mathbb{F} \langle X \rangle \)

---

## 3. Monomials, Degree, and Homogeneity

### Monomial

A **monomial** is a nonzero scalar multiple of a word: \( \lambda w \), where \( \lambda \in \mathbb{F} \), \( w \in X^* \)

### Length and Degree

- Length of a word \( w = x_{i_1} \cdots x_{i_m} \):  
  \( \ell(w) := m \), and \( \ell(1) := 0 \)
- Degree of a nonzero polynomial \( f = \sum \lambda_i w_i \):  
  \( \deg(f) := \max \{ \ell(w_i) \mid \lambda_i \neq 0 \} \)

### Homogeneous Polynomial

A polynomial is **homogeneous** if all its monomials have the same degree.

### Multilinear Polynomial

A polynomial is **multilinear** if each variable appears exactly once in each monomial:  
\[
f(x_1, \ldots, x_n) = \sum_{\sigma \in S_n} \lambda_\sigma x_{\sigma(1)} \cdots x_{\sigma(n)}
\]

---

## 4. Universal Property

Let \( A \) be any unital \( \mathbb{F} \)-algebra and \( f: X \to A \) a function.

Then there exists a unique **unital algebra homomorphism**  
\[
\tilde{f}: \mathbb{F} \langle X \rangle \to A
\]  
such that \( \tilde{f}(x) = f(x) \) for all \( x \in X \).

This is called the **universal property** of \( \mathbb{F} \langle X \rangle \). It makes \( \mathbb{F} \langle X \rangle \) the **free object** in the category of unital \( \mathbb{F} \)-algebras.

---

## 5. Evaluation

Given \( f(x_1, \ldots, x_n) \in \mathbb{F} \langle X \rangle \) and elements \( a_1, \ldots, a_n \in A \),  
the **evaluation** is:

\[
f(a_1, \ldots, a_n)
\]

obtained by substituting \( x_i \mapsto a_i \), preserving order.

**Example:**  
If  
\[
f = x_1^2 x_2 x_1 - x_2 x_3 + 1
\]  
then  
\[
f(a_1, a_2, a_3) = a_1^2 a_2 a_1 - a_2 a_3 + 1 \in A
\]

---

## 6. Domain Property

The free algebra \( \mathbb{F} \langle X \rangle \) is a **domain**, meaning:

If \( f, g \in \mathbb{F} \langle X \rangle \) are nonzero, then  
\[
\deg(fg) = \deg(f) + \deg(g)
\]
