RKLab provides a suite of Matlab files that implement adaptive-step
explicit, implicit and ImEx Runge-Kutta methods.  This software is designed
for instructional use and has been implemented to be easily understood
and modified.  As a result, certain efficiency-related optimizations
have been omitted.

We currently provide four classes of methods:
(a) explicit Runge-Kutta (ERK),
(b) diagonally-implicit Runge-Kutta (DIRK), and
(c) mixed implicit-explicit additive Runge-Kutta (ARK), and
(d) fully implicit Runge-Kutta (IRK).

In addition to these classes of methods, we provide a large
number of Butcher tables (over 70), holding the coefficients for
existing methods in each of these categories.

For ERK, DIRK and ARK methods, time step adaptivity is enabled for methods
with embeddings (most of the included ERK, DIRK and ARK methods include
embeddings). For IRK methods, time step adaptivity is performed using
a Richardson error estimate (cost of 3 solves per step), but leverages
the additional cost through using the Richardson extrapolation for the
time step solution.  All three classes of methods may be run in
so-called "fixed-step mode", wherein the solver will take steps of a
user-supplied magnitude.

In addition to these sets of solvers, we provide three example
problems that may be used to test different methods, and that may be
used as a template for creating new problems.  These test problems
include:
(a) a non-stiff variant of the Van der Pol oscillator (two-component
    nonlinear ODE system).
(b) a stiff Brusselator problem (three-component nonlinear ODE
    system), and
(c) a PDE variant of the Brusselator problem (two-component nonlinear
    PDE system).

These codes require Matlab v2016b or newer.
