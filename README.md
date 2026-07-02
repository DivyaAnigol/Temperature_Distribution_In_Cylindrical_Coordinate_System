# 1D Steady-State Radial Heat Conduction in a Cylinder

### Overview:

This project presents a numerical solution of the one-dimensional steady-state heat conduction equation in cylindrical coordinates using the Finite Volume Method (FVM). The governing equation is discretized over the radial direction, converted into a system of linear algebraic equations, and solved using MATLAB.

This work serves as the foundation for understanding finite volume discretization and matrix formulation before progressing to more advanced thermal and plasma flow simulations.

### Governing Equation:

The governing equation for steady-state radial heat conduction in cylindrical coordinates is

<img width="175" height="65" alt="Screenshot 2026-07-02 150428" src="https://github.com/user-attachments/assets/5968500f-e062-4d1e-a716-f47a56884d60" />

### Assumptions:
```
Axisymmetric geometry
One-dimensional radial conduction
Steady-state conditions
Constant thermal conductivity
No internal heat generation
```

### Numerical Method:

The governing equation is discretized using the Finite Volume Method (FVM).

The computational domain is divided into finite control volumes, and governing equations are derived separately for:
```
Zeroth node (centerline)
Interior nodes
Boundary node (outer wall)
```
These equations are assembled into the matrix form
```
[A][T]=[b]
```
which is solved in MATLAB using
```
T = A\b;
```
### Boundary Conditions:
1. Centerline (r = 0)
Symmetry Boundary Condition

<img width="79" height="61" alt="Screenshot 2026-07-02 151205" src="https://github.com/user-attachments/assets/fde7fde0-d8fc-47dd-a0df-1c98c921d2f0" />

2. Outer Surface (r = R)
Dirichlet Boundary Condition

T(R)=300 K

The outer surface is maintained at a constant temperature of 300 K.

### MATLAB Implementation:

The MATLAB code performs the following steps:
```
Define cylinder dimensions
Generate radial discretization
Assemble coefficient matrix A
Assemble source vector b
Solve the linear system
Plot the temperature distribution
```

### Results:

For the assumptions used in this study:
```
Constant thermal conductivity
No heat generation
Steady-state conduction
Symmetry at the centerline
Fixed wall temperature of 300 K
```
The numerical solution predicts a uniform temperature distribution throughout the cylinder.

The solution is
```
T1​=T2​=⋯=Tn​=300 K
```
Therefore, the temperature profile is a horizontal straight line at 300 K, indicating that no radial temperature gradient exists under the specified boundary conditions.

<img width="719" height="460" alt="Screenshot 2026-07-02 152802" src="https://github.com/user-attachments/assets/3d5bc799-1eff-42a2-b4bb-2c74af3efb07" />

### Learning Outcomes:

This project demonstrates:
```
Finite Volume Method (FVM)
Control volume discretization
Matrix formulation of heat conduction equations
Implementation of boundary conditions
Solution of linear systems in MATLAB
Temperature profile visualization
```






















