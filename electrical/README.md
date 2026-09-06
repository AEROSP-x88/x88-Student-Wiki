# Electrical Hand Calculations

## CORE ELECTRICAL

### Basic Circuit Relationships

- V = IR
- P = VI = I²R = V²/R
- R_series = R₁ + R₂ + ...
- 1/R_parallel = 1/R₁ + 1/R₂ + ...

### Capacitors

- Q = CV
- i = C(dV/dt)
- E = ½CV²

#### Capacitor Combinations

- C_parallel = C₁ + C₂ + ...
- 1/C_series = 1/C₁ + 1/C₂ + ...

---

## RC CHARGING / DISCHARGING

### Time Constant

**τ = RC**

### General Capacitor Voltage

**V_c(t) = V_f + (V_i − V_f)e^(−t/RC)**

### Current

**i(t) = ((V_f − V_i)/R)e^(−t/RC)**

### Approximate Charging

| Time | % Charged |
|---|---:|
| 1τ | 63% |
| 2τ | 86% |
| 3τ | 95% |
| 5τ | 99% |

### DC Steady State

**Initially:**

- Capacitor behaves like a **SHORT circuit**.

**Long after switching:**

- Capacitor behaves like an **OPEN circuit**.

**Important:**

- Capacitor voltage cannot change instantaneously.

---

## PCB POWER

### Trace Voltage Drop and Power

- V_drop = I × R_trace
- P_trace = I² × R_trace
- R_Cu = ρ × L / A

### Notes

- Use trace-width tables or IPC calculators for final sizing.
- Use wider copper or planes for high-current paths.
- Keep power loops short and wide.

---

## THERMAL CHECKS

- ΔT = P × θ
- P_reg = (V_in − V_out) × I_out
- P_FET = I² × R_DS(on)

### Notes

- Check resistor, regulator, and MOSFET margins.
- Confirm temperature rise under worst-case load.

---

## COMMON CIRCUITS

- V_out = V_in × R₂ / (R₁ + R₂)
- τ = RC
- ΔV ≈ I / (fC)
- R_LED = (V_s − V_f) / I

---

## SAFETY CONCERNS

- **Power paths:** Use traces wide enough for the expected current. Keep loops short and minimize voltage drop.
- **Grounding:** Provide clear return paths. Separate noisy and sensitive returns when necessary.
- **Decoupling:** Place capacitors close to IC power pins.
- **Thermals:** Consider copper area, vias, airflow, or heatsinking as needed.
- **Safety:** Check creepage, clearance, isolation, and voltage ratings.
- **Release:** Review the schematic, pass DRC, verify footprints, and confirm Gerbers are ready.
