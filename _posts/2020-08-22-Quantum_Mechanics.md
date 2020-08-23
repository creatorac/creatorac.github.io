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

$$\mathcal{J}(dx'')\mathcal{J}(dx') = \mathcal{J}(dx''+dx') $$

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

The finite translation operator is given by:

\begin{align}
\mathcal{J}(\Delta x' \mathbf{x})|x'\rangle &= |x' + \Delta x' \mathbf{x}\rangle \\
&= \exp(-\frac{ip_x \Delta x'}{\hbar})
\end{align}

(**Note**: Rotations about different axes do _not_ commute)

**Anbelian** group : Whenever the generators of transformations commute. 

$$|p'\rangle$$
is an eigen ket of 
$$\mathcal{J}$$
because 
$$[p,\mathcal{J}]= 0$$ . 

**Dirac's rule** : Classical poisson bracket relationships turn into quantum commutator relationship with a scaling factor of $\hbar$. 

**Jacobi's identity**: [A,[B,C]] +[B,[C,A]]+[C,[A,B]] = 0

**Wave function**: 
$$ \psi_{\alpha}(x') = \langle x'|\alpha \rangle $$
$$ \langle \beta|\alpha\rangle = \int dx' \psi^*_{\beta}(x')\psi_{\alpha}(x') $$

$$\langle\beta|f(x)|\alpha\rangle = \int dx' \psi^*_{\beta}(x')f(x')\psi_{\alpha}(x')$$

Action of momentum operator:
$$\langle\beta|p|\alpha\rangle = \int dx' \psi^*_{\beta}(x')(-i\hbar\frac{\partial}{\partial x'})\psi_{\alpha}(x')$$

Now:

$$\langle x'|p|p'\rangle  = -i\hbar\frac{\partial}{\partial x'}\langle x'|p'\rangle = p' \langle x'|p'\rangle $$

$$\langle x'|p'\rangle = N \exp(\frac{ip'x'}{|hbar}) $$


**Time evolution operator**

$$U(t_0 +dt,t_0) = 1 - \frac{iHdt}{\hbar} $$

**Schrodinger equation** 

\begin{align}
U(t+dt,t_0) &= (1-\frac{iHdt}{\hbar})U(t,t_0)\\
U(t+dt,t_0)- U(t,t_0)&= -\frac{iHdt}{\hbar}U(t,t_0)
i\hbar\frac{\partial}{\partial t}U(t,t_0) &=H U(t,t_0) \\
i\hbar\frac{\partial}{\partial t}|\alpha\rangle = H|\alpha\rangle
\end{align}


**Unitary operator for time dependent self commuting hamiltonian**

$$U(t,t_0) = \exp(-\frac{i}{\hbar})\int_{t_0}^t dt'H(t'))$$

When the Hamiltonian at different times do not commute, we get **Dyson series**

$$U(t,t_0) = 1 + \Sigma_{n=1}^{\inf}(\frac{-i}{\hbar})^n\int_{t_0}^{t}dt_1\int_{t_0}^{t_1}dt_2 ...\int_{t_0}^{t_{n-1}}dt_n H(t_1)H(t_2)...H(t_n)$$

**Stationary state**: An energy eigen state. 

**Heisenberg equation of motion**

$$\frac{dA^{(H)}}{dt}=\frac{1}{i\hbar}[A^{(H)},H].$$

**Simple Harmonic Oscillator**

**Aniihilation operator**(non Hermitian)
$$ a = \sqrt{\frac{m\omega}{2\hbar}}(x + \frac{ip}{m\omega})$$

$$[a,a^{\dagger}]=1$$

$$H = \hbar \omega(N+\frac{1}{2})$$


N and H are time-independent operators. 

**BCH** formula: 
$$ \exp(iG\lambda)A\exp(-iG\lambda) = A + i\lambda[G,A] + (\frac{i^2\lambda^2}{2!})[G,[G,A]]+...+...$$
Where G is a Hermitian operator and $\lambda$ is real. 

**Coherent state**

$$a|\lambda\rangle = \lambda|\lambda\rangle$$

$$|\lambda\rangle = \Sum_{n=0}^{|inf}f(n)|n\rangle

$$ |f(n)|^2 $$
follows Poissonian distribution. 
In an SHO a gaussian state is a coherent state. It is also the minimum uncertainity state. 

**The Classical Limit**: Evolution of the phase of the wave function follows the _Hamilton-Jacobi equation_.

**Free particle in 3D**:

$$\nabla^2 u_E(\mathbf{x})=-\frac{2mE}{\hbar^2}u_E(\mathbf{x})$$

Define: 
$$ \mathbf{k}^2 \equiv \frac{2mE}{\hbar^2} = \frac{\mathbf{p}^2}{\hbar^2}$$

Using separation of variables, 
$$u_E(x) = Ce^{ik\cdot x}.$$

Confining the boundary conditions to a finite cubical box,
$$ u_E(x)=\frac{1}{L^{3/2}}e^{ik\cdot x}$$

the energy eigen values would be:
$$E = \frac{p^2}{2m} = \frac{\hbar^2}{2m}(\frac{2\pi}{L})^2(n_x^2 + n_y^2 + n_z^2).$$

**Theory of Angular momentum**

**Hydrogen Atom**

**Identical Particles**






**Questions**
1. How does one normalize an infinite dimensional vector ?
1. Why are x,y,z position vectors independent ?





