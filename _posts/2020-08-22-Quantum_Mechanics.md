---
layout: post
author: rac
---
The foundations of quantum mechanics shall be discussed in this post. 

First thing: About the Schrodinger equation-- How does one arrive at this equation and what is its significance?

Notes following J.J. Sakurai's Modern Quantum mechanics book.

**Position** : Position is defined as the collection of points in 3D space where the particle is supposed to be.

**Time** : Forward going - clock counting - t.

Given these two quantities. I will define a continuous vector space for position given by:

$$ x|x'\rangle = x' |x'\rangle $$

Here x is the position operator, which when acted upon its eigen vector provides the eigen value $x'$.
A simultaneous _eigen-ket_ in 3D space is given by:

$$ |\mathbf{x}'\rangle = |x',y',z'\rangle $$

*Implicit assumption* - that the three components of the position vector can be measured simultaneously(?)

**Spatial Translation**

$$\mathcal{J}(d\mathbf{x}')|\mathbf{x}'\rangle = |\mathbf{x}' + d\mathbf{x}'\rangle $$

Properties of the translation operator:

$$\mathcal{J}^{\dagger}(dx')\mathcal{J}(dx') = 1 $$

$$\mathcal{J}(dx'')\mathcal{J}(dx') = \mathcal(J)(dx''+dx') $$

$$\mathcal{J}(-dx') = \mathcal{J}^{-1}(dx')$$

$$ \lim_{dx' \to 0} \mathcal{J}(dx') = 1 $$

Let $\mathcal{J}(dx') = 1 - i\mathbf{K}\cdot dx'$, this satisfies all the above mentioned properties. 

$$[\mathbf{x},\mathcal{J}(dx)] = dx'$$
This gives us :
$$ [x_i, K_j] = i\delta_{ij} $$

An infinetisimal translation can be regarded by:

$$ x_{new} = X = x+dx , p_{new} = P = p $$

The generating function for this will be:

$$ F(x,P) = x\cdot P + p\cdot dx $$






**Questions**
1. How does one normalize an infinite dimensional vector ?
1. Why are x,y,z position vectors independent ?





