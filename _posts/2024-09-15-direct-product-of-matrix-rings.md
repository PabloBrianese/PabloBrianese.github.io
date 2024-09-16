---
layout: mathematics-post
title: "Producto directo de anillos de matrices"
date: 2024-09-15 21:27:50 -0300
categories: [mathematics, algebra]
---

En el estudio del álgebra abstracta, los anillos de matrices desempeñan un papel fundamental en la comprensión de estructuras algebraicas más complejas. El teorema de Artin-Wedderburn afirma que todo anillo semisimple es isomorfo a un producto directo finito de anillos de matricies sobre anillos de división (heterogéneos). Una construcción que me parece interesante en el caso homogéneo es cómo el producto directo de anillos de matrices puede ser embebido en un anillo de matrices más grande mediante matrices bloque diagonales. En este artículo, exploraremos esta idea y demostraremos cómo se establece este monomorfismo.

## Matrices Bloque Diagonales

Consideremos dos anillos de matrices sobre un anillo \\( R \\):

- \\( M_n(R) \\): el anillo de matrices de tamaño \\( n \\times n \\).
- \\( M_m(R) \\): el anillo de matrices de tamaño \\( m \\times m \\).

Una **matriz bloque diagonal** en \\( M_{n+m}(R) \\) es una matriz que tiene ceros en todas las posiciones excepto en dos bloques diagonales. Formalmente, se representa como:

\\[
   D = \begin{pmatrix} A & 0 \\\\ 0 & B \end{pmatrix}
\\]

donde \\( A \\in M_n(R) \\) y \\( B \\in M_m(R) \\).

## Definición del Monomorfismo

Definimos un homomorfismo de anillos:

\\[
   \phi: M_n(R) \\times M_m(R) \\to M_{n+m}(R)
\\]

tal que:

\\[
   \phi(A, B) = \begin{pmatrix} A & 0 \\\\ 0 & B \end{pmatrix}
\\]

### Propiedades del Homomorfismo

1. **Preservación de la Adición**:
    \begin{align\*}
        \phi((A_1, B_1) + (A_2, B_2))
        &= \phi(A_1 + A_2, B_1 + B_2) \\\\\\\\
        &= \begin{pmatrix} A_1 + A_2 & 0 \\\\ 0 & B_1 + B_2 \end{pmatrix} \\\\\\\\
        &= \begin{pmatrix} A_1 & 0 \\ 0 & B_1 \end{pmatrix} + \begin{pmatrix} A_2 & 0 \\ 0 & B_2 \end{pmatrix} \\\\\\
        &= \phi(A_1, B_1) + \phi(A_2, B_2)
   \end{align*}

2. **Preservación de la Multiplicación**:
    \begin{align\*}
        \phi((A_1, B_1) \cdot (A_2, B_2))
        &= \phi(A_1 A_2, B_1 B_2) \\\\\\\\
        &= \begin{pmatrix} A_1 A_2 & 0 \\\\ 0 & B_1 B_2 \end{pmatrix} \\\\\\\\
        &= \begin{pmatrix} A_1 & 0 \\\\ 0 & B_1 \end{pmatrix} \cdot \begin{pmatrix} A_2 & 0 \\\\ 0 & B_2 \end{pmatrix} \\\\\\\\
        &= \phi(A_1, B_1) \cdot \phi(A_2, B_2)
   \end{align*}

3. **Inyectividad**:
    Si \\( \phi(A, B) = 0 \\), entonces:

    \\[
    \begin{pmatrix} A & 0 \\\\ 0 & B \end{pmatrix}
    =
    \begin{pmatrix} 0 & 0 \\\\ 0 & 0 \end{pmatrix}
    \\]

    Lo que implica que \\( A = 0 \\) y \\( B = 0 \\). Por lo tanto, \\( \\phi \\) es inyectivo.

## Interpretación

La imagen de \\( \phi \\) consiste en todas las matrices bloque diagonales en \\( M_{n+m}(R) \\) con bloques de tamaños \\( n \\) y \\( m \\). Esto nos permite ver \\( M_n(R) \times M_m(R) \\) como un subanillo de \\( M_{n+m}(R) \\).

## Aplicaciones y Relevancia

- **Comprensión Estructural**: Esta embebición proporciona una visión clara de cómo los anillos de matrices más pequeños se combinan para formar anillos más grandes.
- **Teoría de Módulos**: En la teoría de representaciones y módulos, estas estructuras ayudan a analizar módulos al descomponerlos en componentes más simples.
- **Simplificación de Problemas**: Permite abordar problemas con matrices de tamaño mayor al reducirlos a problemas con matrices de tamaño menor.

## Conclusión

El monomorfismo \\( \phi: M_n(R) \times M_m(R) \to M_{n+m}(R) \\) a través de matrices bloque diagonales es una construcción que ilustra cómo los productos directos de anillos de matrices pueden integrarse en anillos de matrices más grandes.

---

**Referencias**:

- Grillet, P. A. *Álgebra Abstracta*. Un texto introductorio que cubre las estructuras algebraicas, incluyendo anillos y módulos, y discute en detalle conceptos como productos directos y anillos de matrices.
