# Chapter 1: Circuit Variables — Summary

*Source: Electric Circuits, 12th Edition (James Nilsson, Susan Riedel)*

---

## Chapter Objectives

1. Understand and be able to use SI units and standard prefixes for powers of 10.
2. Know and be able to use the definitions of voltage and current.
3. Know and be able to use the definitions of power and energy.
4. Be able to use the passive sign convention to calculate power for an ideal basic circuit element given its voltage and current.

---

## Table of Contents

- [1.1 Electrical Engineering: An Overview](#11-electrical-engineering-an-overview)
- [1.2 The International System of Units](#12-the-international-system-of-units)
- [1.3 Circuit Analysis: An Overview](#13-circuit-analysis-an-overview)
- [1.4 Voltage and Current](#14-voltage-and-current)
- [1.5 The Ideal Basic Circuit Element](#15-the-ideal-basic-circuit-element)
- [1.6 Power and Energy](#16-power-and-energy)
- [Practical Perspective: Balancing Power](#practical-perspective-balancing-power)
- [Summary of Key Equations](#summary-of-key-equations)

---

## 1.1 Electrical Engineering: An Overview

### Five Major Classifications of Electrical Systems

1. **Communication Systems** — Systems that generate, transmit, and distribute information.
   - Examples: Television equipment, radio telescopes, satellite systems, radar systems, telephone systems.

2. **Computer Systems** — Systems that process information using electric signals.
   - Examples: Calculators, personal computers, supercomputers, networks of integrated circuits.

3. **Control Systems** — Systems that use electric signals to regulate processes.
   - Examples: Temperature/pressure/flow rate controls in oil refineries, fuel-injected engines, elevator mechanisms, autopilot systems.

4. **Power Systems** — Systems that generate and distribute electric power.
   - Examples: Nuclear, hydroelectric, solar, and thermal generators; power distribution grids.

5. **Signal-Processing Systems** — Systems that act on signals to change them in useful ways.
   - Examples: Noise reduction systems, audio/video processing systems.

### Circuit Theory

An **electric circuit** is a mathematical model that approximates the behavior of an actual electrical system. Circuit theory provides the intellectual framework for analyzing and designing electrical systems.

> **Note:** In this text, "electric circuit" always refers to a *model*, unless otherwise stated.

Circuit theory is a **special case of electromagnetic field theory**. It allows us to avoid the cumbersome mathematics of generalized field theory while still obtaining sufficiently accurate solutions.

### Three Basic Assumptions of Circuit Theory

These assumptions allow us to use circuit theory instead of electromagnetic field theory:

1. **Electrical effects happen instantaneously throughout the system** — Electric signals travel at or near the speed of light, so in physically small systems, they affect every point simultaneously. Such systems are called **lumped-parameter systems**.

2. **The net charge on every component is always zero** — No component can collect a net excess of charge (though some can hold equal but opposite separated charges).

3. **No magnetic coupling between components** — Magnetic coupling can occur *within* a component, but not between separate components.

### The Rule of 1/10th for Lumped-Parameter Systems

A system qualifies as lumped-parameter if its physical dimension is less than **1/10th of the wavelength** of its signals:

$$
\lambda = \frac{c}{f}
$$

Where:
- $\lambda$ = wavelength (m)
- $c$ = speed of light ($3 \times 10^8$ m/s)
- $f$ = frequency (Hz)

**Examples:**
- Power system at 60 Hz: $\lambda = 5 \times 10^6$ m (≈ 3,100 miles). Lumped if < 310 miles.
- Radio signals at $10^9$ Hz: $\lambda = 0.3$ m. Lumped if < 3 cm.

---

## 1.2 The International System of Units (SI)

### Seven Basic SI Quantities

| Quantity | Basic Unit | Symbol |
|----------|-----------|--------|
| Length | meter | m |
| Mass | kilogram | kg |
| Time | second | s |
| Electric current | ampere | A |
| Thermodynamic temperature | kelvin | K |
| Amount of substance | mole | mol |
| Luminous intensity | candela | cd |

### Common Derived Units

| Quantity | Unit | Symbol |
|----------|------|--------|
| Force | newton | N (kg·m/s²) |
| Energy/Work | joule | J (N·m) |
| Power | watt | W (J/s) |
| Electric charge | coulomb | C (A·s) |
| Electric potential | volt | V (W/A) |
| Resistance | ohm | Ω (V/A) |
| Frequency | hertz | Hz (1/s) |

### Standard Prefixes for Powers of 10

| Prefix | Symbol | Power | Prefix | Symbol | Power |
|--------|--------|-------|--------|--------|-------|
| atto | a | 10⁻¹⁸ | kilo | k | 10³ |
| femto | f | 10⁻¹⁵ | mega | M | 10⁶ |
| pico | p | 10⁻¹² | giga | G | 10⁹ |
| nano | n | 10⁻⁹ | tera | T | 10¹² |
| micro | μ | 10⁻⁶ | peta | P | 10¹⁵ |
| milli | m | 10⁻³ | exa | E | 10¹⁸ |

> **Engineering convention:** Use prefixes for powers divisible by 3, and choose the prefix that places the base number between 1 and 1000.

---

## 1.3 Circuit Analysis: An Overview

### The Engineering Design Process

The circuit analysis process follows this iterative workflow:

![alt text](image.png)

1. **Need** — Identify the problem or improvement opportunity.
2. **Design Specifications** — Establish measurable characteristics of the proposed design.
3. **Concept** — Develop a design concept through education and experience.
4. **Circuit Model** — Translate the concept into a mathematical model using **ideal circuit components**.
5. **Circuit Analysis** — Apply mathematical techniques to predict the behavior of the circuit model.
6. **Comparison & Refinement** — Compare predicted behavior with desired behavior; refine as needed.
7. **Physical Prototype** — Build and test the actual system; iterate if necessary.

### Key Points

- **Circuit models** use ideal circuit components to represent actual electrical components (batteries, resistors, etc.).
- The components in a circuit model should represent the behavior of actual components to an acceptable degree of accuracy.
- Circuit analysis is applied to circuit models, not directly to physical systems.

---

## 1.4 Voltage and Current

### Definition of Voltage

Voltage ($v$) is the **energy per unit charge** created by the separation of positive and negative charges:

$$
\boxed{v = \frac{dw}{dq}}
$$

Where:
- $v$ = voltage in **volts (V)**
- $w$ = energy in **joules (J)**
- $q$ = charge in **coulombs (C)**

> Voltage represents the energy expended when positive and negative charges are separated. It is also called *electric potential difference* or *electromotive force (emf)*.

### Definition of Current

Current ($i$) is the **rate of charge flow**:

$$
\boxed{i = \frac{dq}{dt}}
$$

Where:
- $i$ = current in **amperes (A)**
- $q$ = charge in **coulombs (C)**
- $t$ = time in **seconds (s)**

> Current is caused by the motion of charges. In conductors, electrons (negative charges) are the charge carriers, but by convention, current is defined as the flow of positive charge.

### Relationship Between Current and Charge

From the definition of current, the total charge transferred is:

$$
q(t) = \int_0^t i(x)\, dx
$$

### Key Properties

- Although current consists of discrete moving electrons, the enormous number of them allows us to treat $i$ as a **continuous variable**.
- A component can be modeled strictly in terms of the **voltage and current at its terminals** — two physically different components with the same terminal behavior are identical for circuit analysis purposes.

---

## 1.5 The Ideal Basic Circuit Element

### Three Attributes

An ideal basic circuit element has:

1. **Only two terminals** — points of connection to other circuit components.
2. **Described mathematically** in terms of current and/or voltage.
3. **Cannot be subdivided** into other elements.

> The word **"ideal"** means it does not exist as a physical component. The word **"basic"** means it cannot be reduced further — these are the building blocks of circuit models.

### Polarity Reference System

For any circuit element, we define:
- **Voltage polarity**: marked with $+$ and $-$ signs (reference direction for voltage drop)
- **Current direction**: marked with an arrow (reference direction for current flow)

**Interpretation of Reference Directions:**

| Variable | Positive Value Means | Negative Value Means |
|----------|---------------------|---------------------|
| $v$ | Voltage drop from terminal 1 to 2 | Voltage rise from terminal 1 to 2 |
| $i$ | Positive charge flowing from terminal 1 to 2 | Positive charge flowing from terminal 2 to 1 |

### The Passive Sign Convention

> **Passive Sign Convention:** Whenever the reference direction for current in an element is in the direction of the reference voltage drop across the element, use a **positive sign** in any expression relating voltage to current. Otherwise, use a **negative sign**.

In other words:
- If current enters the **positive** terminal: use $p = +vi$
- If current enters the **negative** terminal: use $p = -vi$

This convention is essential for correctly calculating power and determining whether an element absorbs or supplies power.

---

## 1.6 Power and Energy

### Definition of Power

Power ($p$) is the **rate of energy transfer**:

$$
\boxed{p = \frac{dw}{dt}}
$$

Where:
- $p$ = power in **watts (W)**
- $w$ = energy in **joules (J)**
- $t$ = time in **seconds (s)**

> 1 watt = 1 joule/second

### Power Equation

From the definitions of voltage and current:

$$
\boxed{p = vi}
$$

Where:
- $p$ = power in watts (W)
- $v$ = voltage in volts (V)
- $i$ = current in amperes (A)

### Applying the Passive Sign Convention to Power

| Configuration | Power Formula | Interpretation when $p > 0$ |
|--------------|---------------|---------------------------|
| Current enters $+$ terminal | $p = +vi$ | Element **absorbs** power |
| Current enters $-$ terminal | $p = -vi$ | Element **absorbs** power |

### Interpreting the Algebraic Sign of Power

> - If $p > 0$ (positive): **Power is being delivered to** (absorbed by) the circuit element.
> - If $p < 0$ (negative): **Power is being extracted from** (supplied by) the circuit element.

*Alternative convention (active element):*
> - If $p > 0$: Power is being supplied by the element.
> - If $p < 0$: Power is being absorbed by the element.

### Energy Calculation

Energy is obtained by integrating power over time:

$$
\boxed{w(t) = \int_0^t p(x)\, dx}
$$

### Power Balance Principle

For any complete circuit, the **total power must balance** (sum to zero):

$$
\sum p_{\text{absorbed}} = \sum p_{\text{supplied}}
$$

Or equivalently:

$$
\sum_{\text{all elements}} p = 0
$$

This principle serves as a critical tool for **verifying circuit analysis results**.

---

## Practical Perspective: Balancing Power

### Overview

One of the most important skills in circuit analysis is the ability to **check your answers** by verifying power balance. For any linear circuit:

$$
\text{Total power in the circuit} = \sum p = 0
$$

If the total power is **zero**, the power balances and the calculations are likely correct. If not, there is an error in the analysis.

### Application: Home Electrical Distribution Model

A simplified model for distributing electricity to a home includes:
- **Components a and b**: The electrical power source
- **Components c, d, e**: Wires carrying current from source to devices
- **Components f, g, h**: Lamps, TVs, appliances, and other devices requiring power

### Power Balance Verification Steps

1. Calculate power for each component using $p = vi$ with proper sign convention.
2. Sum all powers: if the sum equals zero, the power balances.
3. If power does not balance, there is an error in the voltage/current values or signs.

**Example from the text:**
| Component | $v$ (V) | $i$ (A) | $p$ (W) |
|-----------|---------|---------|---------|
| a | 120 | −10 | −1200 (supplying) |
| b | 120 | 9 | −1080 (supplying) |
| c | 10 | 10 | 100 (absorbing) |
| d | 10 | 1 | **10** (absorbing — *error detected!*) |
| e | −10 | −9 | 100 (absorbing) |
| f | 100 | −5 | −500 (supplying) |
| g | 120 | 4 | 480 (absorbing) |
| h | −220 | −5 | 1100 (absorbing) |

The power did not balance (total = −20 W). Dividing by 2 revealed the error: component d's current should have been −1 A instead of +1 A.

---

## Summary of Key Equations

| Equation | Description |
|----------|-------------|
| $v = \dfrac{dw}{dq}$ | Voltage (energy per unit charge) |
| $i = \dfrac{dq}{dt}$ | Current (rate of charge flow) |
| $q(t) = \displaystyle\int_0^t i(x)\,dx$ | Charge from current |
| $p = \dfrac{dw}{dt}$ | Power (rate of energy transfer) |
| $p = vi$ | Power from voltage and current |
| $w(t) = \displaystyle\int_0^t p(x)\,dx$ | Energy from power |
| $\displaystyle\sum_{\text{all}} p = 0$ | Power balance |

---

## Key Terms

| Term | Definition |
|------|-----------|
| **Electric circuit** | A mathematical model that approximates the behavior of an actual electrical system |
| **Lumped-parameter system** | A system small enough that electrical effects happen instantaneously throughout |
| **Voltage** | Energy per unit charge created by charge separation (unit: volt, V) |
| **Current** | Rate of charge flow (unit: ampere, A) |
| **Power** | Rate of energy transfer (unit: watt, W) |
| **Energy** | Capacity to do work (unit: joule, J) |
| **Ideal basic circuit element** | A two-terminal mathematical building block that cannot be subdivided |
| **Passive sign convention** | Convention where $p = +vi$ when current enters the positive terminal |
| **Power balance** | The principle that total power in a circuit must sum to zero |

---

## Problem-Solving Tips

1. **Always assign reference polarities and directions** before writing circuit equations.
2. **Use the passive sign convention consistently** — once chosen, all equations must agree with it.
3. **Check units** at every step using SI units and prefixes.
4. **Verify power balance** to check the validity of your circuit analysis.
5. **Use the rule of 1/10th** to determine if a system can be treated as lumped-parameter.
6. **Remember that reference directions are arbitrary** — the mathematics will yield correct results regardless of the initial choice, as long as you are consistent.
