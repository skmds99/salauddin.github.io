---
layout: blog
title: Ramification Part 1
---

## Dense Right Ideals

Let \( R \) be a ring and \( M \) a right \( R \)-module. A right ideal \( I \subseteq R \) is said to be **dense** in \( R \) (with respect to \( M \)) if:

> For every \( m \in M \) and every nonzero \( r \in R \), there exists \( i \in I \) such that \( mi \ne 0 \).

In particular, if \( M = R_R \), the regular right module, then \( I \) is dense if for every nonzero \( r \in R \), there exists \( i \in I \) with \( r i \ne 0 \).

### Properties of Dense Right Ideals

- If \( I \) is dense in \( R \), then \( I \) is essential in \( R_R \).
- If \( R \) is right nonsingular, the dense right ideals form a directed system.
- The intersection of dense right ideals is again dense.
- Every essential right ideal is dense, but the converse is not always true.

### Example

Let \( R = \mathbb{Z} \). Then every nonzero ideal \( (n) \subseteq \mathbb{Z} \) is dense.

For any nonzero \( r \in \mathbb{Z} \) and \( n \ne 0 \), we have \( r n \ne 0 \). So \( (n) \) is dense in \( \mathbb{Z} \).

---

## Maximal Right Ring of Quotients

The **maximal right ring of quotients** \( Q^r_{\text{max}}(R) \) extends \( R \) in a way that ensures the inclusion of "enough" elements to allow for a well-behaved extension with respect to right ideals.

### Motivation

In the commutative case, the field of fractions of an integral domain \( R \) is the smallest field containing \( R \). For noncommutative rings, a more general construction is needed.

### Construction

Let \( E(R_R) \) be the injective hull of \( R \) as a right \( R \)-module. Define

\[
Q^r_{\text{max}}(R) := \text{End}_R(E(R_R))
\]

This is the ring of endomorphisms of the injective hull of \( R \) (as a right \( R \)-module).

### Properties

- \( R \subseteq Q^r_{\text{max}}(R) \) as a subring.
- \( Q^r_{\text{max}}(R) \) is right self-injective.
- Every dense right ideal of \( R \) becomes essential in \( Q^r_{\text{max}}(R) \).
- \( Q^r_{\text{max}}(R) \) is the largest right ring of quotients of \( R \) with respect to dense right ideals.

---

## Summary

Dense right ideals are used to identify "non-negligible" subsets of a ring which are crucial for extending modules and constructing overrings. The maximal right ring of quotients generalizes the concept of field of fractions to the noncommutative setting.

---

## References

1. M. Brešar, *Rings, Modules and Linear Algebra*, De Gruyter, 2014.  
2. T. Y. Lam, *Lectures on Modules and Rings*, Springer GTM 189, 1999.  
3. N. Jacobson, *Basic Algebra II*, W. H. Freeman, 1989.  
4. J. Lambek, *Lectures on Rings and Modules*, Blaisdell, 1966.
