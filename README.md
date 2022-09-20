# Differential-Geometry

# Tangent Space

Created: September 8, 2022 1:25 PM
Date: September 10, 2022
Email: huzongxiang@yahoo.com
Tags: Personal

## ***Cotangent space***

Given a differentiable structure on a topological manifold, we can approximate a neighborhood of any point by a linear space.

---

### Function germs

Suppose ${p}$ is a fixed point of the m-dimension smooth manifold ${M}$. Let  ${f}$ be a ${C^\infty}$-function ( ${C^\infty}$ is infinitely differentiable) defined in a neighborhood of ${p}$, ${C_p^\infty}$  represents the set of all of these ${f}$ functions at ${p}$. Two functions ${f}$ and ${g}$ usually have different domains but their addition and multiplication are still well-defined if ${p} \in U \bigcap V$, ${U}$ and ${V}$ are domains of ${f}$ and ${g}$, respectively.  If ${f}$ and ${g}$ ${\mathbb\in}$ ${C_p^\infty}$, ${f + g}$ and ${f * g}$ also belong to ${C_p^\infty}$, that is, ${f + g}$ and ${f*g} \in C_p^\infty$. But  ${g|_ {U \bigcap V} = f|_ {U \bigcap V}} = 0$, that the zero is not unique, so ${C_p ^\infty}$ can not be defined as a linear space. If defining an equivalence relation ${f\sim g}$ if and only if existing an open neighborhood ${H}$ of ${p}$ such that ${f|_H=g|_H}$. The ${[f]}$ represents ${f}$’s ${\sim}$ equivalence class in ${C_p^\infty}$, the ${[f]}$ is called the ***function germ*** of the manifold ${M}$ at ${p}$. Let

$$
{\mathscr{F}_p=C_p^\infty/\sim=\{[f]|f\in C_p^\infty\}}.
$$

By introducting addition and scalar multipication into ${\mathscr{F}_p}$, it becomes a linear space, so for ${[f]}$ and ${[g]} \in\mathscr{F}_p$, ${\alpha} \in \mathbb{R}$, define

$$
\begin{cases}
[f] + [g] = [f + g],\\ 
\alpha [f] = [\alpha f].
\end{cases}
$$

---

### Linear space

Suppose ${\gamma (t)}$ is a parameterized curve in manifold ${M}$ through a point ${p}$, ${t \in (-\delta, \delta) \subset \mathbb{R}}$ and ${\gamma (0)=p}$. Denote the set of all these parameterized curves as ${\Gamma_p}$. For any ${\gamma (t) \in \Gamma_p}$, ${[f] \in \mathscr{F}_p}$, Let 

$$
 \ll \gamma, [f]\gg = \left. \dfrac{d(f \circ \gamma)}{dt}\right|_{t=0} \quad, \quad -\delta \ \lt \ t \  \lt \ \delta .
$$

Obviously, the ${\ll \ , \ \gg}$  is linear with respect to the second variable. For arbitrary ${\gamma \in \Gamma_p}$, ${[f]}$ and ${[g] \in \mathscr F_p}$, have

$$
\begin{aligned} \ll \gamma, [f] + [g]\gg &= \ll \gamma, [f]\gg + \ll \gamma, [g]\gg,\\
\ll \gamma, \alpha [f]\gg &= \alpha \ll \gamma, [f]\gg.  \end{aligned}
$$

Thus, Let ${\ll\gamma, [f]\gg=0}$ can get a linear subspace of ${\mathscr{F}_p}$ as

$$
\mathscr{H}_p=\{[f] \in \mathscr{F}_p|{\ll\gamma, [f]\gg=0}，\ {\forall} \gamma \in \Gamma_p\}.
$$

***Theorem 1.*** Suppose ${[f]} \in \mathscr F_p$, for an admissible coordinate chart ${(U,\varphi_U)}$, let

$$
F(x^1, x^2, ..., x^m) = f \circ \varphi_U^{-1}(x^1, x^2, ..., x^m)
$$

then, ${[f] \in \mathscr H_p}$  if and only if

$$
\left.\frac{\partial F}{\partial x^i} \right| _{\varphi_U(p)} = 0, \quad \quad 1 \le \ i \ \le \ m.
$$

Proof. Suppose ${\gamma (t) \in \Gamma_p}$

$$
{(\varphi_U \circ \gamma (t))^i}=x^i(t),\quad \quad 1 \le \ i \ \le \ m.
$$

$$
\begin{aligned} \ll \gamma, [f]\gg &= (\left. \dfrac{df \circ \gamma}{dt}) \right| _{t=0} \\
&= \left.\dfrac{d}{dt}F(x^1,x^2,...,x^m)\right| _{t=0}  \\
&= \sum \limits_i^m \left( \frac{\partial f \circ \varphi_U^{-1}}{\partial u^i}\right) _{\varphi_U(p)} \cdot \left.\dfrac{d (\varphi_U \circ \gamma(t))^i}{dt} \right| _{t=0} \\
&= \sum\limits_i^m \left.\frac{\partial F}{\partial x^i} \right| _{\varphi_U(p)}\cdot \left.\frac{dx^i}{dt}\right| _{t=0} \end{aligned}
$$

because ${\gamma (t) \in \Gamma_p}$ is an arbitary curve, so $\Large {\frac{dx^i}{dt} \Large|\normalsize_{t=0}}$ is arbitary real value. For arbitary ${\gamma (t) \in \Gamma_p}$  , a necessary and sufficent condition for ${\ll\gamma, [f]\gg=0}$ is

$$
\left.\frac{\partial F}{\partial x^i} \right| _{\varphi_U(p)} = 0, \quad \quad 1 \le \ i \ \le \ m.
$$

Theorem 1 indicates that subspace ${\mathscr H_p}$ is exactly the linear space of germs of smooth functions whose partial derivatives with respect to local coordinates all vanish at  ${p}$.

---

### Definition

The quotient space ${\mathscr F_p/\mathscr H_p}$  is called ***Cotangent Space*** of ${M}$ at ${p}$, denoted by ${T_p^* (M)}$ or ${T _p^*}$. The ${\mathscr H_p}$-equivalence class of the function germ ${[f]}$ is denoted by ${[\widetilde{f\ }]}$ or ${(df)_p}$, and is called a cotangent vector on ${M}$ at ${p}$.

${T_p^*(M)}$ is a linear space. It has a linear structure induced from the linear space ${\mathscr F_p}$, i.e. for ${[f]}$ and ${[g] \in \mathscr F_p}$,  we have

$$
\begin{cases}
[\widetilde{f\ }] + [\widetilde{g }] = [\widetilde{f +g\ }],\\
\alpha[\widetilde{f\ }] = \widetilde{\alpha[f\ }].\\
\end{cases}
$$

---

***Theorem 2.***  Suppose ${f^1}$, ${f^2}$, …, ${f^s} \in C_p^\infty$ and  ${F(y^1, y^2, …, y^s)}$  is a smooth function in a neighborhood of ${(f^1(p), f^2(p), ..., f^s(p)) \in \mathbb R^s}$. Then ${f=F(f^1, f^2, …, f^s) \in C_p^\infty}$ and 

$$
df_p = \sum \limits_k^s (\frac{\partial F}{\partial f^k})_{(f^1(p), f^2(p), ..., f^s(p))} \cdot (df^k)_p
$$

Proof. ${f(p)=F(f^1(p), f^2(p), ..., f^s(p))}$, since ${f=F(f^1, f^2, …, f^s) \in C_p^\infty}$ so ${f(p) \in C_p^\infty}$, let

$$
{a_k = \left( \frac{\partial F}{\partial f^k} \right) _{(f^1(p), f^2(p), ..., f^s(p))}}
$$

for an arbitrary ${\gamma(t)}$,

$$
\begin{aligned} \ll \gamma, [f]\gg &= \left. \dfrac{d(f \circ \gamma)}{dt} \right|_{t=0} \\
&= \sum \limits_k^s \left( \frac{\partial F}{\partial f^k}\right) _{(f^1(p), f^2(p), ..., f^s(p))} \cdot \left.\dfrac{d(f^k \circ \gamma(t))}{dt} \right| _{t=0} \\
&= \sum \limits_k^s a_k \cdot \ll \gamma, [f^k] \gg. 
\end{aligned}
$$

Thus,

$$
 [f] -\sum \limits_k^s a_k [f^k]=0,
$$

i.e.

$$
(df)_p = \sum \limits_k^s a_k (df^k)_p.
$$

---

Corollary 1. For any ${[f]}$, ${[g] \in C_p^\infty}$,  ${a \in \mathbb R}$, have

$$
\begin{aligned} &d(f+g)_p=(df)_p + (dg)_p, \\
&d(af)_p=a \cdot(df)_p, \\
&d(fg)_p=g\cdot(df)_p + f\cdot (dg)_p. \end{aligned}
$$

Proof. …

Corollary 2. ${dim (T_p^*)=m}$.

Proof. Choose an admissible coordinate chart ${(U, \varphi_U)}$, and define local coordinates ${u^i}$ by

$$
u^i(p) = f^i(p) = (\varphi_U(p))^i
$$

as Theorem 2 have

$$
\begin{aligned}f &= F(f^1(p), f^2(p), ...,f^m(p)) \\
&= F(u^1(p), u^2(p), ...,u^m(p)) \end{aligned}
$$

then

$$
\begin{aligned}(df)_p &= \sum \limits_i^s \left( \frac{\partial F}{\partial u^i} \right) _{(u^1(p), u^2(p), ..., u^s(p))} \cdot(du^i)_p \\
&= \sum \limits_i^s a_i (du^i)_p \\
where \quad &a_i = \left( \frac{\partial F}{\partial u^i}\right) _{(u^1(p), u^2(p), ..., u^s(p))} \end{aligned}
$$

**Thus, any ${(df)_p}$ is a linear combination of the ${(du^k)_p}$, ${1 \le \ k \ \le \ m}$, if there have real values ${a_k}$, such that**

$$
\sum \limits_i^s a_i (du^i)_p = 0  
$$

i.e.

$$
\sum \limits_i^s a_i [u^i] \in \mathscr H_p
$$
so for any ${\gamma_(t) \in \Gamma_p}$, have

$$
\ll \gamma(t), \sum \limits_i^s a_i [u^i] \gg \ = \ \sum \limits_i^s a_i \left. \frac{d(u^i \circ \gamma(t))}{dt}\right| _{t=0} \normalsize =0
$$

select ${\lambda_k(t) \in \Gamma_p}$, ${1 \le \ k \ \le \ m}$, let

$$
u^i \circ \lambda_k(t) = u^i(p) + \delta_k^it,
$$

where

$$
\quad \delta_k^i =\begin{cases} 1, \quad i=k, \\ 
0, \quad i \neq k. \end{cases}
$$

then

$$
\quad \quad \left.  \dfrac{d(u^i \circ \lambda_k(t))}{dt}\right|_{t=0} = \delta_k^i,
$$

so

$$
\begin{aligned} \ll \lambda_k(t), \sum \limits_i^s a_i [u^i] \gg \ &= \ \sum \limits_i^s a_i \left. \dfrac{d(u^i \circ \lambda_k(t))}{dt}\right|_{t=0} \\
&= \sum \limits_i^s a_i \delta_k^i = 0.\end{aligned}
$$

hence  ${\{a_k=0,\ 1 \ \le k \ \le \ m\}}$,  ${\{(du^i)_p,\ 1 \ \le i \ \le \ m\}}$ is linearly independent. Therefore it forms a basis for ${T_p^* (M)}$ , called the natural basis of ${T_p^* (M)}$  with respect to the local coordinate system ${u^i}$. Thus ${T_p^* (M)}$ is an m-dimensional linear space.

---

---

## ***Tangent space***

### Definition

${[f] - [g] \in \mathscr H_p}$ if and only if ${\ll \gamma, [f] \gg = \ll \gamma, [g] \gg}$ for any ${\gamma \in \Gamma_p}$, so can define

$$
\ll \gamma, (df)_p \gg \ = \ \ll \gamma, [f] \gg, \quad \gamma \in \Gamma_p, \quad (df)_p \in T_p^*.
$$

The same problem as linearization of the space of ${f}$  that zero is not unique when linearizing the space of ${\gamma}$, so can define an equivalence relation ${\sim}$ in ${\Gamma_p}$ as follow,

$$
\ll \gamma, (df)_p \gg \ = \ \ll \gamma', (df)_p \gg, \quad \gamma, \gamma' \in \Gamma_p, \quad \forall(df)_p \in T_p^*.
$$

Denote the equivalence class of ${\gamma}$ as ${[\gamma]}$, so define

$$
<[\gamma], (df)_p > \ = \ \ll \gamma, (df)_p \gg.
$$

${\{[\gamma]| \gamma \in \Gamma_p\}}$ is the dual space of cotangent space ${T_p^*}$. The proof is as follows

Under the local coordinates ${u^i}$, suppose ${\gamma \in \Gamma_p}$, is given by the functions ${u^i = u^i(t) = (\varphi_U \circ \gamma(t))^i, 1 \le \ i \ \le m}$. From Theorem 1, ${f \circ \varphi^{-1}(u^1, u^2, …,u^m) = F(u^1, u^2, …,u^m)}$ , then can derive that

$$
\begin{aligned} <[\gamma], (df)_p > \ &= \ \sum \limits_i^m \left( \frac{\partial f \circ \varphi_U^{-1}}{\partial u^i}\right) _{\varphi_U(p)} \cdot \left .\dfrac{d (\varphi_U \circ \gamma(t))^i}{dt} \right| _{t=0} \\
&= \ \sum \limits_i^m \left(\frac{\partial f \circ \varphi_U^{-1}}{\partial u^i}\right) _{\varphi_U(p)} \cdot \left(\dfrac{d u^i(t)}{dt}\right) _{t=0} \\
&= \ \sum \limits_i^m a_i \xi^i \end{aligned}
$$

where

$$
a_i=\left(\frac{\partial f \circ \varphi_U^{-1}}{\partial u^i}\right) _{\varphi_U(p)}, \quad \xi^i=\left(\dfrac{d u^i(t)}{dt}\right) _{t=0}
$$

Due to ${\gamma \in \Gamma_p}$ is arbitrary, so ${\{\xi^i\}}$ can be arbitrary real values such that ${<[\gamma, \cdot>]}$ is all of the linear mappings on ${T_p^*}$. The ${[\gamma]}$ forms a dual space of ${T_p^*}$, called the tangent space of ${M}$ at ${p}$.

A necessary and sufficient condition for ${[\gamma] = [\gamma']}$ for ${u^i(t) = u'^i(t)}$ is

$$
\left( \dfrac{d u^i(t)}{dt} \right) _{t=0} = \left( \dfrac{d u'^i(t)}{dt} \right) _{t=0}
$$

Thus, the geometric meaning of tangent vectors means that these two parametrized curves have the same tangent vector at the point ${p}$.

So far,

$$
 \ll X, (df)_p \gg \quad X=[\gamma] \in T_p, \quad (df)_p \in T_p^*.
$$

is a bilinear mapping of both ${T_p}$ and ${T_p^*}$.

select ${\lambda_k \in \Gamma_p}$ as

$$
u^i \circ \lambda_k(t) = u^i(p) + \delta_k^it,
$$

then

$$
<[\lambda_k],(du^i)_p> \ = \ \delta_k^i.
$$

so ${\{[\lambda_k]| 1 \le \ k \ \le m\}}$ can be viewed as the dual baisis of ${\{(du^i)_p| 1 \le \ i \ \le m\}}$.

---

### P**artial differential operators**

Furthermore,

$$
\begin{aligned} <[\lambda_k], (df)_p > \ &= \ \left<[\lambda_k],\sum \limits_i^m \left(\frac{\partial f \circ \varphi_U^{-1} }{\partial u^i}\right) _p \cdot (du^i)_p \right> \\
&= \sum \limits_i^m \left(\frac{\partial f \circ \varphi_U^{-1} }{\partial u^i}\right) _p \ \cdot<[\lambda_k],(du^i)_p> \\
&= \sum \limits_i^m \left(\frac{\partial f \circ \varphi_U^{-1} }{\partial u^i}\right) _p \cdot \delta_k^i \\
&= \left(\frac{\partial f \circ \varphi_U^{-1} }{\partial u^k}\right) _p \end{aligned}
$$

Thus, the ${[\lambda_k]}$ are the partial differential operators ${(\partial/\partial u^k)}$ on the function germs ${[f]}$. Then

$$
<[\lambda_k],(du^i)_p> \ = \ \left<\left.\frac{\partial}{\partial u^k}\right| _{p}, (du^i)_p \right> = \delta_k^i. 
$$

We call the basis of  ${\{ (\partial/\partial u^i)_p, 1 \le \ i \ \le m\}}$ in ${T_p}$ the Natural Basis of the tangent space under the local coordinate system ${u^i}$.

So from ${<[\gamma], (df)_p > = \sum \limits_i^m a_i \xi^i}$ , have

$$
[\gamma] = \sum \limits_i^m \xi^i \left. \frac{\partial}{\partial u^i}\right|_{p}
$$

the ${\{\xi^i, 1 \le \ i \ \le m\}}$ are componets of the tangent vector ${[\gamma]}$ regards to natural basis ${\{ (\partial/\partial u^i)_p, 1 \le \ i \ \le m\}}$.
** 

---

## *T**angent map***

Under local coordinates ${u^i}$, a tangent vector ${X=[\gamma] \in T _p}$ and a cotangent vector ${a=df \in T _p^*}$ have linear representations in terms of natural bases:

$$
X = \sum \limits_i^m \xi^i \frac{\partial}{\partial u^i}, \quad a = \sum \limits_i^s a_i du^i
$$

where

$$
\xi^i = \frac{\partial (u^i \circ \gamma)}{\partial u^i}, \quad a _i = \dfrac{df}{du^i}
$$

Under another local coordinate system ${u^{'i}}$, if the components of ${X}$ and ${a}$ with respect to the corresponding natural bases are ${\xi^{'}}$ and ${a^{'}}$, respectively, then they satisfy the following transformation rules:

$$
\xi^{'j} = \sum \limits_i^m \xi ^i \dfrac{d u^{'j}}{d u^i}, \quad a _i = \sum \limits_i^m a _j^{'} \cdot \dfrac{du^{'j}}{du^i}
$$

where

$$
\dfrac{d u^{'j}}{d u^i} = \frac{\partial (\varphi _U^{'} \circ \varphi _U^{-1})^j}{\partial u^i}
$$

Smooth maps between smooth manifolds induce linear maps between tangent spaces and between cotangent spaces. Suppose ${F : M \rightarrow N}$ is a smooth map, ${p \in  M}$, and ${q = F(p)}$. Define the map ${F^*: T _q^* \rightarrow T _p^*}$ as follows:

$$
F^* (df) = d (d \circ F), \quad \quad df \in T _q^*
$$

Obviously this is a linear map, called the differential of the map ${F}$.

Consider next the adjoint of ${F^*}$, namely the tangent map ${F _*: T _p \rightarrow T _q}$ defined for ${X \in T _p^*}$, ${\alpha \in T _p}$ as follows:

$$
<F _\ast X,\alpha> = <X, F^{*} \alpha>
$$

Suppose ${u ^i}$ and ${v ^ \alpha}$ are local coordinates near ${p}$ and ${q}$, respectively. Then

$$
v^\alpha = F^\alpha(u ^1, u^2, \cdots,u^m) \quad \quad 1 \le \ \alpha \ \le n
$$

Thus the action of ${F^*}$ on the natural basis ${\{dv ^\alpha, 1 \le \alpha \le n\}}$ is given by

$$
\begin{aligned} F^* (dv^\alpha) &= d(v^\alpha \circ F) \\ 
&= \sum \limits_{i=1}^m \left(\frac{\partial F^\alpha}{\partial u^i} \right) _p \cdot du^i \end{aligned}
$$

The matrix representation of ${F^*}$ in the natural bases ${dv^\alpha}$ and ${du^i}$ is exactly the Jacobian matrix ${(dF^\alpha/du^i)}$.

$$
\begin{aligned} <F _* \left(\frac{\partial}{\partial u^i} \right), (dv^\alpha)> \ &= \ <\frac{\partial}{\partial u^i},\  F^*(dv^\alpha)> \\ 
&= <\frac{\partial}{\partial u^i},\  \sum \limits _{j=1}^m \left(\frac{\partial F^\alpha}{\partial u^j} \right) _p \cdot du^j> \\ 
&= \sum \limits _{j=1}^m <\frac{\partial}{\partial u^i},\ du^j> \cdot \left(\frac{\partial F^\alpha}{\partial u^j} \right) _p \\ 
&= \sum \limits _{j=1}^m \delta _i^j \cdot \left(\frac{\partial F^\alpha}{\partial u^j} \right) _p \\ 
&= \left(\frac{\partial F^\alpha}{\partial u^i} \right) _p \\ 
&= <\sum \limits _{\beta=1}^n \left(\frac{\partial F^\beta}{\partial u^i} \right) _p \cdot \frac{\partial}{\partial v^\beta},\ dv^\alpha> \\ 
&= \sum \limits _{\beta=1}^n \left(\frac{\partial F^\beta}{\partial u^i} \right) _p \cdot <\frac{\partial}{\partial v^\beta},\ dv^\alpha> \\ 
&= \sum \limits _{\beta=1}^n \left(\frac{\partial F^\beta}{\partial u^i} \right) _p \cdot \delta _\beta^\alpha \end{aligned}
$$

i.e.

$$
F _* \left(\frac{\partial}{\partial u^i} \right) =  \sum \limits _{\beta=1}^n \left(\frac{\partial F^\beta}{\partial u^i} \right) _p \cdot \frac{\partial}{\partial v^\beta}
$$

Hence the matrix representation of the tangent map ${F}$, under the natural bases $*{\{\partial / \partial u^i\}}$* and ${\{\partial / \partial v^\alpha\}}$ is still the Jacobian matrix ${(\partial F^\alpha / \partial u^i)}.$
