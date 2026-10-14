# Roadmap: the path to the opencalculus Target

This is the path, not the code. Each milestone says what you learn, what you build, and how you know it works. Pick one and open a pull request. See [CONTRIBUTING.md](../CONTRIBUTING.md).

## Session 4: Romberg integration

**You will learn:** How combining trapezoid sums at several step sizes cancels error terms.

**You will build:** A Romberg table that builds higher-order rules from the trapezoid rule.

**Checkpoint (not met by the shipped code):** The area of e^x on [0, 1] to an error below 1e-12 using at most 17 function evaluations (the shipped Simpson rule with 17 evaluations gives 1.5e-7).

**Difficulty:** intermediate

## Session 5: Gaussian quadrature

**You will learn:** Why well-chosen sample points beat equally spaced ones.

**You will build:** A Gauss-Legendre integrator with a handful of nodes.

**Checkpoint (not met by the shipped code):** The same area of e^x on [0, 1] to an error below 1e-11 using only 5 function evaluations (the shipped Simpson rule with 5 evaluations gives 3.7e-5).

**Difficulty:** intermediate

## Session 6: Derivatives without subtraction

**You will learn:** How complex numbers give a derivative with no cancellation error.

**You will build:** A derivative routine that avoids the round-off limit of Session 3.

**Checkpoint (not met by the shipped code):** d/dx sin x at x = 1 with an error below 1e-14 (the best shipped difference gives 6e-13).

**Difficulty:** advanced

## Session 7: Derivatives of noisy data

**You will learn:** Local polynomial fitting and the trade-off between smoothness and lag.

**You will build:** A smoothing differentiator for the speedometer log of the mini-project.

**Checkpoint (not met by the shipped code):** RMS acceleration error below 0.15 m/s^2 on the 60 s log (ignoring 3 s at each end); a 4 s moving average gives 0.19 and a 2 s one 0.37.

**Difficulty:** advanced

## Session 8: Solve the braking ODE

**You will learn:** Integrating a differential equation step by step with an error-controlled solver.

**You will build:** A solver for a braking car with drag, v' = -c v^2, and the distance it travels.

**Checkpoint (not met by the shipped code):** For c = 0.01 per m and v(0) = 30 m/s, the distance after 10 s equals the exact ln(1 + c * 30 * 10) / c = 138.63 m to an error below 1e-6 m.

**Difficulty:** advanced

## The final step

Combine the milestones: an animation that draws any function you type in with its derivative and integral traced live, computed by your own error-controlled numerical methods, with a convergence plot showing their orders. If your result looks like the Target animation, open a pull request and tell us how you did it.
