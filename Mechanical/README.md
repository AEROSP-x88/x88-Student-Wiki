# Mechanical Hand Calculations

## Reference Equation Sheets

- [General Mechanical Equation Sheet — Missouri S&T](https://web.mst.edu/jthomas/classes/2210/formulas/formula_sheet.pdf)
- [General Thermal Equation Sheet — Purdue University](https://engineering.purdue.edu/ME200/files/current_semester/ME200_Eqn_Spring2020.pdf)

---

# CORE MECHANICS

## Properties

| Property | Equation | Notes |
|---|---|---|
| Density | `ρ = m/V` | kg/m³ |
| Weight | `W = mg` | `g ≈ 9.81 m/s²` |
| Young's Modulus | `E = σ/ε` | Material stiffness |
| Shear Modulus | `G = E/[2(1+ν)]` | Requires Poisson's ratio |
| Poisson's Ratio | `ν = -ε_transverse/ε_axial` | Dimensionless |
| Safety Factor | `FoS = Failure / Applied` | Typically `FoS > 1` required |

---

# STRESS & STRAIN

## Normal Stress

**Equation:**

`σ = F/A`

Where:

- `σ` = normal stress
- `F` = axial force
- `A` = cross-sectional area

Used for axial loading.

---

## Normal Strain

**Equation:**

`ε = ΔL/L`

Where:

- `ε` = normal strain
- `ΔL` = change in length
- `L` = original length

**Notes:**

- Strain is dimensionless.
- Positive strain → tension
- Negative strain → compression

---

## Young's Modulus

**Equation:**

`E = σ/ε`

Where:

- `E` = Young's modulus
- `σ` = normal stress
- `ε` = normal strain

Describes the stiffness of a material under axial loading.

---

## Shear Stress — Average

**Equation:**

`τ = V/A`

Where:

- `τ` = average shear stress
- `V` = internal shear force
- `A` = area resisting shear

---

## Beam Shear Stress

**Equation:**

`τ = VQ/(It)`

Where:

- `V` = internal shear force
- `Q` = first moment of area
- `I` = area moment of inertia
- `t` = thickness at the location being evaluated

Used to determine the shear stress distribution within a beam.

---

## Bearing Stress

**Equation:**

`σ_b = F/(td)`

Where:

- `F` = applied force
- `t` = material thickness
- `d` = pin/bolt diameter

Common applications:

- Bolts
- Pins
- Rivets
- Joints

---

# DEFORMATION

## Axial Deformation

**Equation:**

`δ = FL/(AE)`

Where:

- `δ` = axial deformation
- `F` = applied force
- `L` = original length
- `A` = cross-sectional area
- `E` = Young's modulus

Common applications:

- Trusses
- Rods
- Bolts
- Structural members

---

## Thermal Expansion

**Equation:**

`ΔL = αLΔT`

Where:

- `ΔL` = change in length
- `α` = coefficient of thermal expansion
- `L` = original length
- `ΔT` = change in temperature

### Fully Constrained Member

If thermal expansion is completely prevented:

`σ = EαΔT`

---

# AREA MOMENT OF INERTIA

The area moment of inertia describes how the area of a cross-section is distributed relative to an axis.

Common applications:

- Beam bending
- Beam deflection
- Buckling
- Structural analysis

**Common relationships:**

`I_x = ∫y² dA`

`I_y = ∫x² dA`

For composite sections, use the parallel-axis theorem:

`I = I_centroid + Ad²`

Where:

- `I_centroid` = moment of inertia about the shape's centroidal axis
- `A` = area
- `d` = distance between axes

> **Insert beam/area moment of inertia table here**

---

# BENDING

## Bending Stress

**General equation:**

`σ = Mc/I`

Where:

- `σ` = bending stress
- `M` = bending moment
- `c` = distance from neutral axis
- `I` = area moment of inertia

### Maximum Bending Stress

`σ_max = Mc/I`

Maximum stress occurs at the point farthest from the neutral axis.

---

# BEAM DEFLECTION

For common beam-loading cases:

| Loading Condition | Maximum Deflection |
|---|---:|
| Cantilever — End Load | `PL³/(3EI)` |
| Simply Supported — Center Load | `PL³/(48EI)` |
| Simply Supported — Uniform Load | `5wL⁴/(384EI)` |

Where:

- `P` = applied point load
- `w` = distributed load
- `L` = beam length
- `E` = Young's modulus
- `I` = area moment of inertia

> **Insert beam deflection/loading table here**

---

# TORSION

## Polar Moment of Inertia

### Solid Circular Shaft

`J = πd⁴/32`

### Hollow Circular Shaft

`J = π(D⁴ − d⁴)/32`

Where:

- `J` = polar moment of inertia
- `D` = outer diameter
- `d` = inner diameter

---

## Rotating Power

`P = Tω`

Where:

- `P` = power
- `T` = torque
- `ω` = angular velocity

For rotational systems:

`ω = 2πf`

---

## Angle of Twist

`θ = TL/(JG)`

Where:

- `θ` = angle of twist
- `T` = applied torque
- `L` = shaft length
- `J` = polar moment of inertia
- `G` = shear modulus

---

# BUCKLING

## Euler Buckling

`P_cr = π²EI/(KL)²`

Where:

- `P_cr` = critical buckling load
- `E` = Young's modulus
- `I` = area moment of inertia
- `K` = effective-length factor
- `L` = unsupported length

### Effective-Length Factors

| End Condition | `K` |
|---|---:|
| Fixed–Fixed | 0.5 |
| Fixed–Pinned | 0.699 |
| Pinned–Pinned | 1.0 |
| Fixed–Free | 2.0 |

**Important:** Euler buckling applies primarily to slender columns and assumes elastic buckling behavior.

---

# PRESSURE VESSELS

## Thin-Wall Assumption

A common preliminary assumption is:

`t < D/20`

Where:

- `t` = wall thickness
- `D` = vessel diameter

---

## Hoop Stress

`σ_h = Pr/t`

For a thin-walled cylindrical pressure vessel, using radius:

`σ_h = Pr/t`

Where:

- `P` = internal pressure
- `r` = internal radius
- `t` = wall thickness

---

## Longitudinal Stress

`σ_l = Pr/(2t)`

For a closed-end cylindrical pressure vessel:

`σ_h = 2σ_l`

Therefore, **hoop stress is approximately twice the longitudinal stress**.

---

## Required Wall Thickness

For preliminary sizing:

`t = Pr/σ_allow`

Where:

- `σ_allow` = allowable material stress

> Apply the appropriate design standard and safety factor for final pressure-vessel sizing.

---

# LEAKAGE

## Volumetric Leak Rate

`Q = ΔV/Δt`

Where:

- `Q` = volumetric leak rate
- `ΔV` = change in volume
- `Δt` = elapsed time

---

## Mass Leak Rate

`ṁ = Δm/Δt`

Where:

- `ṁ` = mass leak rate
- `Δm` = change in mass
- `Δt` = elapsed time

---

## Pressure-Decay Approximation

For a fixed-volume system under appropriate assumptions:

`Q ≈ V(ΔP)/(Δt)`

Where:

- `Q` = approximate leak rate
- `V` = system volume
- `ΔP` = pressure change
- `Δt` = elapsed time

> For gas systems, the relationship between pressure and leak rate depends on temperature, gas properties, and whether the flow is viscous, molecular, or transitional.

---

## Ideal Gas Law

`PV = nRT`

Where:

- `P` = pressure
- `V` = volume
- `n` = number of moles
- `R` = universal gas constant
- `T` = absolute temperature

### Common Leak-Rate Units

- sccm
- L/min
- cc/sec

---

# ENERGY

## Potential Energy

`PE = mgh`

---

## Kinetic Energy

`KE = ½mv²`

---

## Rotational Kinetic Energy

`KE_rot = ½Iω²`

Where:

- `m` = mass
- `v` = linear velocity
- `h` = height
- `I` = mass moment of inertia
- `ω` = angular velocity

---

# VIBRATIONS

## Natural Frequency

`ω_n = √(k/m)`

Where:

- `ω_n` = natural angular frequency
- `k` = spring stiffness
- `m` = mass

---

## Natural Frequency

`f_n = ω_n/(2π)`

Where:

- `f_n` = natural frequency in Hz
- `ω_n` = natural angular frequency in rad/s

---

## Period

`T = 2π√(m/k)`

Where:

- `T` = period
- `m` = mass
- `k` = stiffness

---

# COMPRESSIBLE FLOW

## Mach Number

`M = v/a`

Where:

- `M` = Mach number
- `v` = flow velocity
- `a` = speed of sound

### Interpretation

| Mach Number | Flow Regime |
|---|---|
| `M < 0.3` | Generally treated as incompressible |
| `M < 1` | Subsonic |
| `M = 1` | Sonic |
| `M > 1` | Supersonic |

---

## Speed of Sound

`a = √(γRT)`

Where:

- `a` = speed of sound
- `γ` = ratio of specific heats
- `R` = specific gas constant
- `T` = absolute temperature

---

## Choked Flow

Choked flow occurs when the flow reaches:

`M = 1`

At the controlling location, typically the smallest flow area.

Once choked, increasing downstream pressure reduction does not continue to increase mass flow in the same way; the flow is limited by the sonic condition at the throat.

---

# QUICK DESIGN CHECK

Before moving from hand calculations to detailed simulation, check:

- [ ] Loads and boundary conditions are defined
- [ ] Material properties are appropriate
- [ ] Stresses are below allowable limits
- [ ] Deformation is acceptable
- [ ] Buckling has been considered
- [ ] Thermal expansion has been considered
- [ ] Pressure loads have been checked
- [ ] Leakage requirements have been checked
- [ ] Vibration/natural frequency has been considered
- [ ] Flow regime and Mach number have been checked
- [ ] Appropriate safety factors have been applied
- [ ] Units are consistent
- [ ] Results are physically reasonable

> **Hand calculations are a first-pass engineering tool.** If the hand calculation indicates a design may be close to a limit, perform a more detailed analysis before proceeding with the design.
