---
title: Riemann Curvature Tensor
mathjax: true
abbrlink: 48c07248
date: 2021-11-15 17:24:37
tags:
- physics
- math
- differential geometry
- general relativity
categories: 
- General Relativity
---


<center>
<img style="border-radius: 0.3125em;box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);"  
src="https://gitee.com/spaceofzsj/pictures/raw/master/16DETACHMENT_SPAN-articleLarge.jpg" />
<a href="https://movie.douban.com/subject/5322596/"  target="opentype">超脱</a> (<a href="https://www.imdb.com/title/tt1683526"  target="opentype">Detachment</a>)
</center>

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=22489526&auto=0&height=66"></iframe>
<!--more-->

# Derivative Operator
>**Definition 1.1**  Let $\mathscr{F}_{M}(k,l)$ be the set of all $\mathrm{C}^{\infty}$ tensor field of $(k,l)$ type. The map $\nabla$ : $\mathscr{F}_{M}(k,l)\rightarrow\mathscr{F}_{M}(k,l+1)$ is called the *derivative operator*  on the manifold $M$ if it satisfies the following conditions:
>
>1. Linearity: For all $A$, $B\in\mathscr{F}_{M}(k,l)$ and $\alpha,\beta\in R$,
>$$\begin{equation}\nabla_{c}\left(\alpha A^{a_{1}\cdots a_{k}}_{\quad\quad \ b_{1}\cdots b_{l}}+\beta B^{a_{1}\cdots a_{k}}_{\quad\quad \ b_{1}\cdots b_{l}}\right)=\alpha\nabla_{c}A^{a_{1}\cdots a_{k}}_{\quad\quad \ b_{1}\cdots b_{l}}+\beta B^{a_{1}\cdots a_{k}}_{\quad\quad \ b_{1}\cdots b_{l}}\notag\end{equation}$$
>2. Leibnitz rule: For all $A\in\mathscr{F}(k,l)$,$B\in\mathscr{F}(k',l')$,
>$$\begin{align}&\nabla_{e}\left[A^{a_{1}\cdots a_{k}}_{\quad\quad\ b_{1}\cdots b_{k}} B^{c_{1}\cdots c_{k}}_{\quad\quad\ d_{1}\cdots d_{k}}\right]\notag\\&=\nabla_{e}\left[A^{a_{1}\cdots a_{k}}_{\quad\quad\ b_{1}\cdots b_{k}}\right] B^{c_{1}\cdots c_{k}}_{\quad\quad\ d_{1}\cdots d_{k}}+\nabla_{e}A^{a_{1}\cdots a_{k}}_{\quad\quad\ b_{1}\cdots b_{k}} \left[B^{c_{1}\cdots c_{k}}_{\quad\quad\ d_{1}\cdots d_{k}}\right]\notag\end{align}$$
>3. Commutativity with contraction: For all $A\in\mathscr{F}(k,l), B\in\mathscr{F}(k',l'),$
>$$\begin{equation}\nabla_{d}\left(A^{a_{1}\cdots c\cdots a_{k}}_{\quad\quad\quad\ \  b_{1}\cdots c\cdots b_{l}}\right)=\nabla_{d}A^{a_{1}\cdots c\cdots a_{k}}_{\quad\quad\quad\ \  b_{1}\cdots c\cdots b_{l}}\notag\end{equation}$$
>4. Consistency with the notion of tangent vectors as directional derivatives on scalar fields: For all $f\in\mathscr{F}$ and all $t^{a}\in V_{p}$:
>$$\begin{equation}t(f)=t^{a}\nabla_{a}f\notag\end{equation}$$
>5. Torsion free: For all $f\in\mathscr{F}$,
>$$\begin{equation}\nabla_{a}\nabla_{b}f=\nabla_{b}\nabla_{a}f\notag\end{equation}$$

When we write something like:
$$\begin{equation}\nabla_{a}\left(v^{b}\omega_{b}\right)=v^{b}\nabla_{a}\omega_{b}+\omega_{b}\nabla_{a}v^{b},\notag\end{equation}$$
we have actually used the third condition:
$$\begin{equation}
    \nabla_{a}\left(v^{b}\omega_{c}\right)=\nabla_{a}\left[\mathrm{C}\left(v^{b}\omega_{c}\right)\right]
                                      =\mathrm{C}^{1}_{2}\left(v^{b}\nabla_{a}\omega_{c}\right)+\mathrm{C}^{1}_{2}\left[\left(\nabla_{a}v^{b}\right)\omega_{c}\right]
                                      =v^{b}\nabla_{a}\omega_{b}+\omega_{b}\nabla_{a}b^{b},\notag
                                      \end{equation}$$

where $\mathrm{C}$ represents contraction.

From the forth condition, we can see that: 
$$\begin{equation}\nabla_{a}f=(\mathrm{d}f)_{a} \tag{1.1}\label{1.1}\end{equation}$$

In fact, the operator satisfies this five conditions above must exist on any manifold. Now we consider the effects of two different derivative operators $\nabla_{a}$ and $\widetilde{\nabla}_{a}$ on several kinds of tensors. 

From Eq.$\eqref{1.1}$, we know for all $f\in \mathscr{F}_{M}$
$$\begin{equation}\nabla_{a} f=\widetilde{\nabla}_{a} f=\left( \mathrm{d}f \right)_{a}.\tag{1.2}\label{1.2}\end{equation}$$

>**Theorem 1.1**$\quad$ If $p \in M$, $\omega_{b}, \omega_{b}'\in \mathscr{F}(0,1)$ satisfy $\omega_{b}'|_{p}=\omega_b|_{p}$, then
>$$\begin{equation}\left[\left(\widetilde{\nabla}_{a}-\nabla_{a}\right)\omega_{b}'\right]_{p}=\left[\left(\widetilde{\nabla}_{a}-\nabla_{a}\right)\omega_{b}\right]_{p}\notag\end{equation}$$
>**Proof**$\quad$ We only need to prove that
>$$\begin{equation}\left[\nabla_{a}\left(\omega_{b}'-\omega_{b}\right)\right]_{p}=\left[\widetilde{\nabla}_{a}\left(\omega_{b}'-\omega_{b}\right)\right]_{p}.\tag{1.3}\label{1.3}\end{equation}$$
>Assume that $\Omega=\omega_{b}'-\omega_{b}$. We can choose a coordinate system $\left\{ x_{\mu} \right\}$ whose coordinate patch contains $p$，so $\Omega_{\mu}(p)=0$ because $\omega_{b}'|_{p}=\omega_{b}|_{p}$, where $\Omega_{\mu}$'s are the coordinates of $\Omega_{b}$. For $p$,
$$\begin{align}
    \left[\nabla_{a}\left(\omega_{b}'-\omega_{b}\right)\right]_{p}&=\left[\nabla_{a}\Omega_{b}\right]_{p}=\left\{\nabla_{a}\left[\Omega_{\mu}\left(\mathrm{d}x^{\mu}\right)_{b}\right]\right\}|_{p}\notag\\
    &=\Omega_{\mu}(p)\left[\nabla_{a}\left(\mathrm{d}x^{\mu}\right)_{b}\right]_{p}+\left[\left(\mathrm{d}x^{\mu}\right)_{b}\nabla_{a}\Omega_{\mu}\right]|_{p}=\left[\left(\mathrm{d}x^{\mu}\right)_{b}\nabla_{a}\Omega_{\mu}\right]_{p}.\notag
\end{align}$$
In the same way, we have $\left[\widetilde{\nabla_{a}}\left(\omega_{b}'-\omega_{b}\right)\right]_{p}=\left[\left(\mathrm{d}x^{\mu}\right)_{b}\widetilde{\nabla}_{a}\Omega_{\mu}\right]_{p}$. From Eq.$\eqref{1.1}$, we know that $\left[\nabla_{a}\Omega_{\mu}\right]_{p}=\left[\widetilde{\nabla}_{a}\Omega_{\mu}\right]_{p}=\left[(\mathrm{d}\Omega_{\mu})_{a}\right]_{p}$. So Eq.$\eqref{1.3}$ is true.
>
>*Q.E.D.*

*Theorem 1.1* shows that $\left[\left(\widetilde{\nabla}_{a}-\nabla_{a}\right)\omega_{b}\right]_{p}$ depends only on $\omega_{b}|_{p}$. And the value of $\left(\widetilde{\nabla}_{a}-\nabla_{a}\right)$ corresponds to a tenser of type $(1,2)$ $\mathrm{C}^{c}_{\ \ ab}$, which satisfies
$$\left[\left(\widetilde{\nabla}_{a}-\nabla_{a}\right)\omega_{b}\right]_{p}=\mathrm{C}^{c}_{\ \ ab}\omega_{c}|_{p}.$$
Since $p$ is an arbitary point, so the effect of two derivative operators on $\omega_{b}$ only differs by a tensor field of type $(1,2)$ on $M$. To be specific,

>**Theorem 1.2** $\quad$For all $\omega_{b}\in\mathscr{F}(0,1)$:
>$$\begin{align}\nabla_{a}\omega_{b}=\widetilde{\nabla}_{a}\omega_{b}-\mathrm{C}^{a}_{\ \ ab}\omega_{c}\tag{1.4}\label{1.4}\end{align}$$


>**Theorem 1.3**$\quad$ $\mathrm{C}^{c}_{\ \ ab}=\mathrm{C}^{c}_{\ \ ba}$
>
>**Proof**$\quad$ Let $\omega_{b}=\nabla_{b}f=\widetilde{\nabla}_{b}f$, where $f\in\mathscr{F}_{M}$. From Eq.$\eqref{1.4}$, we have $\nabla_{a}\nabla_{b}f=\widetilde{\nabla_{a}}\widetilde{\nabla_{b}}f-\mathrm{C}^{c}_{\ \ ab}\nabla_{c}f$. Exchange the indicies $a$ and $b$ and we have $\nabla_{b}\nabla_{a}f=\widetilde{\nabla_{b}}\widetilde{\nabla_{a}}f-\mathrm{C}^{c}_{\ \ ba}\nabla_{c}f$. Notice the last condition in the *definition 1.1*(torsion free), there is $\mathrm{C}^{c}_{\ \ ab}\nabla_{c}f=\mathrm{C}^{c}_{\ \ ba}\nabla_{c}f$. Let $T^{c}_{\ \ ab}=\mathrm{C}^{c}_{\ \ ab}-\mathrm{C}^{c}_{\ \ ba}$, then $T^{c}_{\ \ ab}\nabla_{c}f=0$ for all $f\in \mathscr{F}_{M}$. Then the coordinate components $T^{\sigma}_{\ \ \mu\nu}=T^{c}_{\ \ ab}\left(\mathrm{d}x^{\sigma}\right)_{c}\left(\frac{\partial}{\partial x^{\mu}}\right)^{a}\left(\frac{\partial}{\partial x^{\nu}}\right)^{b}=0$(the second equality is because $T^{c}_{\ \ ab}\left(\mathrm{d}x^{\sigma}\right)_{c}=T^{c}_{\ \ ab}\nabla_{c}x^{\sigma}=0$ ), so $T^{c}_{\ \ ab}=0$.
>
>*Q.E.D*


>**Theorem 1.4**$\quad$ For all $v^{b}\in\mathscr{F(1,0)}$, $$\begin{align}
    \nabla_{a}v^{b}=\widetilde{\nabla}_{a}v^{b}+\mathrm{C}^{b}_{\ \ ac}v^{c}\notag
\end{align}$$
>
>**Proof** Let $\omega_{b}$ be an arbitary dual vector field on manifold $M$, then
$$
\begin{align}
\nabla_{a}\left(\omega_{b} v^{b}\right)&=\omega_{b}\nabla_{a}v^{b}+v^{b}\nabla_{a}\omega_{b}\notag\\
&=\omega_{b}\nabla_{a}v^{b}+v^{b}\left(\widetilde{\nabla}_{a}\omega_{b}-\mathrm{C}^{c}_{\ \ ab}\omega_{c}\right).\tag{1.5}\label{1.5}
\end{align}$$
On the other hand, $\widetilde{\nabla}_{a}\left(\omega_{b}v^{b}\right)=\omega_{b}\widetilde{\nabla}_{a}v^{b}+v^{b}\widetilde{\nabla}_{a}\omega_{b}$. From Eq.$\eqref{1.2}$, $\nabla_{a}\left(\omega_{b}v^{b}\right)=\widetilde{\nabla_{b}}\left(\omega_{b}v^{b}\right)$ because $\omega_{b}v^{b}$ is a scaler field. Substitute this relation into Eq.$\eqref{1.5}$, we have
$$\begin{align}
    \omega_{b}\nabla_{a}v^{b}=\omega_{b}\widetilde{\nabla}_{a}v^{b}+\mathrm{C}^{c}_{\ \ ab}v^{b}\omega_{c}=\omega_{b}\widetilde{\nabla}_{a}v^{b}+\mathrm{C}^{b}_{\ \ ac}v^{c}\omega_{b}\notag
\end{align}
$$
for all $\omega_{b}\in\mathscr{F}_{M}(0,1)$. So $\nabla_{a}v^{b}=\widetilde{\nabla}_{a}v^{b}+\mathrm{C}^{b}_{\ \ ac}v^{c}$.
>
>*Q.E.D*

This theorem can be generalized.

>**Theorem 1.5**$\quad$ For all $T\in\mathscr{F}_{M}(k,l)$
>$$\begin{align}
    &\nabla_{a}T^{b_{1}\cdots b_{k}}_{\quad\quad\ \ c_{1}\cdots c_{l}}\notag\\
    &=\widetilde{\nabla}_{a}T^{b_{1}\cdots b_{k}}_{\quad\quad\ \ c_{1}\cdots c_{l}}+\sum_{i}\mathrm{C}^{b_{i}}_{\ \ \  ad}T^{b_{1}\cdots d\cdots b_{k}}_{\quad\quad\quad\ \ \  c_{1}\cdots c_{l}}-\sum_{j}C^{d}_{\ \ \ ac_{j}}T^{b_{1}\cdots b_{k}}_{\quad\quad\ \  c_{1}\cdots d\cdots c_{l}}.\tag{1.6}\label{1.6}
\end{align}$$

Any two derivative operators only differ by a tensor field $\mathrm{C}^{c}_{\ \ ab}$. On the other hand, with any derivative operator $\widetilde{\nabla}_{a}$ and a tensor field $\mathrm{C}^{c}_{\ \ ab}$ which is symmetric in down indicies ($\mathrm{C}^{c}_{\ \ ab}=\mathrm{C}^{c}_{\ \ ba}$), we can define a new operator according to Eq.$\eqref{1.6}$ and this new operator will satisfy the definition of a derivative operator.

After choosing a derivative operator $\nabla_{a}$, the manifold will be denoted by $(M,\nabla_{a})$.

Let $\left\{x^{\mu}\right\}$ be a coordinate system on manifold $M$. The mapping $\partial_{a}: \mathscr{F}_{O}(k,l)\rightarrow\mathscr{F}_{O}(k,l+1)$ is defined as:
$$\begin{align} \partial_{a} T^{b}_{\ \ \ c}\equiv\left(\mathrm{d}x^{\mu}\right)_{a}\left(\frac{\partial}{\partial x^{\nu}}\right)^{b}\left(\mathrm{d}x^{\sigma}\right)_{c}\partial_{\mu}T^{\nu}_{\ \ \ \sigma}.\notag\end{align}$$
It can be veryfied that $\partial_{a}$ satisfies **definition 1.1** and we call it *ordinary derivative*.

Althogh, $\partial_{a}$ is a special case of $\nabla_{a}$, it relies on the coordinate itself. We call the $\nabla_{a}$'s independent on the coordinate system *covariant derivative* and $\partial_{a}$ is not a covariant derivative.

>**Definition 1.2**$\quad$The difference between $\nabla_{a}$ and $\partial_{a}$ , i.e. $\mathrm{C}^{c}_{\ \ ab}$ in Eq.$\eqref{1.6}$,is called the *Christoffel symbol* of $\nabla_{a}$ in this coordinate system which is denoted by $\Gamma^{c}_{\ \ ab}$.

Christoffel symbol is a tensor field depends on the coordinate system.(See detailed discussion in《微分几何入门与广义相对论（上）第二版》p59). 

>**Theorem 1.6**$\quad$ 
>$$\begin{align}&v^{\nu}_{\ \ ;\mu}=v^{\nu}_{\ \ ,\mu}+\Gamma^{\nu}_{\ \ \mu\sigma}v^{\sigma}\tag{1.7}\label{1.7}\\
&\omega_{\nu\ \ ;\mu}=\omega_{\nu\ \ ,\mu}-\Gamma^{\sigma}_{\ \ \mu\nu}\omega_{\sigma}\notag
\end{align}$$

# Derivative And Parallel Transport Of Vector Field Along Curve
## Parallel Transport Of Vector Field Along Curve

After choosing a derivative operator on manifold $M$, we have the definition of parallel transport Of vector field along a curve.

>**Definition 2.1** $\quad$ Let $v^{a}$ be a vector field defined on a curve $C(t)$. $v^{a}$ is said to be transported parallelly along $C(t)$ if $T^{b}\nabla_{b}v^{a}=0$ is satisfied along the curve where $T^{a}\equiv\left(\frac{\partial}{\partial t}\right)^{a}$ is the tangent vector of $C(t)$.

>**Theorem 2.1**$\quad$ Let the equation of the curve $C(t)$ be $x^{\mu}(t)$ and $T^{a}=\left(\frac{\partial}{\partial t}\right)^{a}$ , then the vector field $v^{a}$ transports parallelly along $C(t)$ satisfies:
>$$\begin{align}
    T^{b}\nabla_{b}v^{a}=\left(\frac{\partial}{\partial x^{\mu}}\right)^{a}\left(\frac{\mathrm{d}v^{\mu}}{\mathrm{d} t}+\Gamma^{\mu}_{\ \ \nu\sigma}T^{\nu}v^{\sigma}\right)\tag{2.1}\label{2.1}
\end{align}$$
>**Proof**
>$$\begin{align}
    T^{b}\nabla_{b}v^{a}&=T^{b}\left(\partial_{b}v^{a}+\Gamma^{a}_{\ \ bc}v^{c}\right)\notag\\
    &=T^{b}\left[\left(\mathrm{d}x^{\nu}_{b}\right)\left(\frac{\partial}{\partial x^{\mu}}\right)^{a}\partial_{\nu}v^{\mu}+\Gamma^{a}_{\ \ bc}v^{c}\right]\notag\\
    &=T^{\nu}\left(\frac{\partial}{\partial x^{\nu}}\right)^{a}\left(\frac{\partial v^{\mu}}{\partial x^{\nu}}\right)+\Gamma^{a}_{\ \ bc}T^{b}v^{c}\notag\\
    &=\left(\frac{\partial}{\partial x^{\mu}}\right)^{a}\left[T^{\mu}\left(\frac{\partial v^{\mu}}{\partial x^{\nu}}\right)+\Gamma^{\mu}_{\ \ \nu\sigma}T^{\nu}v^{\sigma}\right].\notag
\end{align}$$
>Notice that $T^{\nu}=\frac{\mathrm{d}x^{\nu}(t)}{\mathrm{d}t}$, we have 
>$$\begin{align}
    T^{\nu}\left(\frac{\partial v^{\mu}}{\partial x^{\nu}}\right)&=\left[\frac{\mathrm{d}x^{\nu}(t)}{\mathrm{d}t}\right]\left[\frac{\partial v^{\mu}\left(t(x)\right)}{\partial x^{\nu}}\right]\notag\\
    &=\frac{\mathrm{d}v^{\nu}(t)}{\mathrm{d}t}\notag
\end{align}$$
>Q.E.D


>**Theorem 2.2**$\quad$ A point on the curve $C(t)$ together with a vector at the point determine the only vector field transports parallelly along the curve.
>**Proof**$\quad$From Eq.$\eqref{2.1}$ , we know:
>$$\begin{align}
    \frac{\mathrm{d}v^{\mu}}{\mathrm{d}t}+\Gamma^{\mu}_{\ \ \nu\sigma}T^{\nu}v^{\sigma}=0,\quad \mu=1,2\cdots n.
\end{align}$$
>These are $n$ ODEs of first order and there are enough initial conditions to determine the solution.
>
>Q.E.D

Let $p,q\in M$, then $V_{p}$ and $V{q}$ are two different vector space and any two elements from them can't be compared directly. Given a vector in $p$ (or $q$),we can choose a curve passes $p$ and $q$. Using **Theorem 2.2**, there is only one vector field determine by the curve and the vector. So we can compare the value of the vector field at $p$ (or $q$) with the given vector in $q$ (or $p$). The vector field depend on the choice of the curve. Anyway, $\nabla_{a}$ connects these two vector, so we call $\nabla_{a}$ *connection*.

## Derivative Curvatur Compatible With The Metric




>To be continued...

Download: [PDF](https://gitee.com/spaceofzsj/Notes/raw/master/lecturenotes/A%20Brief%20Summary%20of%20Basic%20Differential%20Geometry%20for%20General%20Relativity/Chapter%203/Chapter%203.pdf)(Updating)