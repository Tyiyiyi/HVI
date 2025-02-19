# Hemivariational Inequality Problem

This document describes an elastic body within the framework of linear isotropic elasticity. The body occupies a reference domain $\Omega \subset \mathbb{R}^d$ ($d=2,3$), with its boundary $\partial\Omega$ divided into four disjoint parts.

## Boundary Conditions

**Clamped boundary** $\Gamma_D$: The displacement is fully constrained:

$$
u = 0 \quad \text{on} \ \Gamma_D.
$$

**Traction boundary** $\Gamma_N$: A surface load $g_N$ is applied:

$$
\sigma \nu = g_N \quad \text{on} \ \Gamma_N.
$$

**Free boundary** $\Gamma$: No traction acts on this part:

$$
\sigma \nu = 0 \quad \text{on} \ \Gamma.
$$

**Contact boundary** $\Gamma_C$: The body is in contact with a rigid foundation, leading to:

$$
u_{\nu} = 0, \quad -\sigma_{\tau} \in \partial j_{\tau}(x, u_{\tau}) \quad \text{on} \ \Gamma_C.
$$

## Governing Equations

The problem is governed by the following equations:

**Constitutive law**: The stress tensor $\sigma$ is related to the strain tensor $\varepsilon$ through the elasticity operator $\mathbb{C}$:

$$
\sigma = \mathbb{C} \varepsilon \quad \text{in} \ \Omega.
$$

**Equilibrium equation**: The balance of internal stresses and body force $f$:

$$
div \sigma + f = 0 \quad \text{in} \ \Omega.
$$

## Complete Formulation

The equilibrium displacement $u: \Omega \to \mathbb{R}^d$ satisfies the following system:

$$
\begin{aligned}
		\sigma &= \mathbb{C} \varepsilon \quad && \text{in} \ \Omega, \\
		div \sigma + f &= 0 \quad && \text{in} \ \Omega,\\
		u &= 0 \quad  && \text{on} \ \Gamma_D,\\
		\sigma \nu &= g_N \quad && \text{on} \ \Gamma_N,\\
		\sigma \nu &= 0 \quad && \text{on} \ \Gamma,\\
		u_{\nu} &= 0, \quad - \sigma_{\tau} \in \partial j_{\tau}(x, u_{\tau}) \quad && \text{on} \ \Gamma_C.
\end{aligned}
$$

## Notations

- $\varepsilon = \varepsilon(u)$ is the strain tensor.
- $\sigma = \sigma(u)$ is the stress tensor.
- $\mathbb{C}: \Omega \times \mathbb{S}^d \to \mathbb{S}^d$ is the elasticity operator.
- $j_{\tau}$ is a potential functional describing the friction law.

## Cost Functional

- Consider

$$
J(\Omega)= \int_{\Gamma_N}  g_N \cdot  u ,
$$

- Consider

$$
J(\Omega)=\frac{1}{2} \int_{\Omega} \sigma(u):\varepsilon(u) +\int_{\Gamma_C} j_{\tau,\epsilon} (u_{\tau})-\int_{\Omega} f \cdot u - \int_{\Gamma_N} g_N \cdot u.
$$


## Summary

This system defines an **elastic contact problem with friction**, where the goal is to determine the displacement field $u$ that satisfies the equations under the given forces and boundary conditions.

---


