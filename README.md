# Pulley Momentum Calculator

A web-based physics calculator for analyzing pulley systems with hanging masses. This interactive tool allows users to explore the relationship between linear and rotational motion in pulley systems.

## Overview

This application calculates key rotational dynamics quantities for a pulley system where a hanging mass descends under gravity. As the mass falls, it causes the pulley to rotate, converting gravitational potential energy into both linear and rotational kinetic energy.

## Physics Concepts

The calculator implements fundamental physics principles including:

- **Conservation of Energy**: Total mechanical energy is conserved as potential energy converts to kinetic energy
- **Rotational Kinematics**: Relationships between angular displacement, velocity, and acceleration
- **Linear-Angular Motion**: The connection between linear motion of the hanging mass and angular motion of the pulley

## Calculated Metrics

The application computes the following quantities when the hanging mass reaches the bottom of its descent:

### Rotational Quantities (Pulley)
1. **Angular Displacement (θ)**: Total angle through which the pulley rotates (in radians)
2. **Angular Speed (ω)**: Final rotational speed of the pulley (in rad/s)
3. **Angular Momentum (L)**: Rotational momentum of the pulley system (in kg⋅m²/s)
4. **Angular Energy (KE_rot)**: Rotational kinetic energy of the pulley (in Joules)

### Linear Quantities (Hanging Mass)
5. **Fall Duration (t)**: Time required for the mass to fall the height h (in seconds)
6. **Linear Acceleration (a)**: Constant acceleration of the hanging mass (in m/s²)
7. **Final Velocity (v)**: Linear velocity of the mass when it reaches the bottom (in m/s)

## Input Parameters

Users can customize the following system parameters:

- **Pulley Radius (r)**: Physical radius of the pulley wheel (in meters)
- **Moment of Inertia (I)**: Rotational inertia of the pulley (in kg⋅m²)
- **Hanging Mass (m)**: Mass of the falling weight (in kg)
- **Descent Height (h)**: Distance the mass falls (in meters)

## Physics Derivations

The calculator implements two equivalent approaches to derive the angular velocity ω:

### Method 1: Energy Conservation Approach

Based on conservation of mechanical energy:

```
Initial Energy = Final Energy
mgh = ½mv² + ½Iω²

Using v = ωr:
mgh = ½m(ωr)² + ½Iω²
mgh = ½ω²(mr² + I)

Solving for ω:
ω = √(2mgh/(mr² + I))
```

### Method 2: Force Analysis Approach

Using Newton's laws and rotational dynamics:

```
Forces on hanging mass:    mg - T = ma
Torque on pulley:         τ = Tr = Iα
No-slip condition:        a = αr, so α = a/r

From pulley rotation:     Tr = I(a/r)
Solving for tension:      T = Ia/r²

Substituting into force equation:
mg - Ia/r² = ma
mg = a(m + I/r²)
a = mg/(m + I/r²)

Using kinematics v² = 2ah:
v = √(2ah) = √(2gmh/(m + I/r²))

Using kinematics h = ½at² for fall duration:
t = √(2h/a) = √(2h(m + I/r²)/(mg))

Converting to angular velocity:
ω = v/r = √(2gmh/(mr² + I))
```

### Additional Key Equations

```
Angular Displacement: θ = h/r
Angular Momentum: L = Iω
Rotational Energy: KE_rot = ½Iω²
Linear Acceleration: a = mg/(m + I/r²)
Final Linear Velocity: v = √(2gmh/(m + I/r²))
Fall Duration: t = √(2h(m + I/r²)/(mg))
```

### Physical Insights

- The system acceleration `a = mg/(m + I/r²)` is always less than free fall `g`
- More pulley inertia (larger I) results in slower acceleration and final speeds
- The no-slip condition couples linear and angular motion: `v = ωr`
- Both derivation methods yield identical results, demonstrating the equivalence of energy and force approaches

## Usage

1. Open `index.html` in a web browser
2. Adjust the input sliders or enter values directly
3. Observe real-time calculations as parameters change
4. Results update automatically with each parameter modification

## Files

- `index.html`: Complete web application with HTML, CSS, and JavaScript
- `README.md`: This documentation file
- `Pully Momentum Problem.jpg`: Reference diagram (if available)

## Educational Value

This tool is ideal for:
- Physics students learning rotational dynamics
- Visualizing energy conservation in mechanical systems
- Understanding the relationship between linear and angular motion
- Exploring how system parameters affect motion characteristics

## Browser Compatibility

The application uses standard HTML5, CSS3, and JavaScript and should work in all modern web browsers. 