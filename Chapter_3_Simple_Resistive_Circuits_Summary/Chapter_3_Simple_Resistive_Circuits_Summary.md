# Chapter 3: Simple Resistive Circuits — Summary

*Source: Electric Circuits, 12th Edition (James Nilsson, Susan Riedel)*

---

## Chapter Objectives

1. Be able to recognize resistors connected in series and in parallel.
2. Know how to design simple voltage-divider and current-divider circuits.
3. Be able to use voltage division and current division appropriately to solve simple circuits.
4. Be able to determine the reading of ammeters and voltmeters.
5. Understand how a Wheatstone bridge is used to measure resistance.
6. Know when and how to use delta-to-wye equivalent circuits.

---

## Table of Contents

- [3.1 Resistors in Series](#31-resistors-in-series)
- [3.2 Resistors in Parallel](#32-resistors-in-parallel)
- [3.3 The Voltage-Divider and Current-Divider Circuits](#33-the-voltage-divider-and-current-divider-circuits)
- [3.4 Voltage Division and Current Division](#34-voltage-division-and-current-division)
- [3.5 Measuring Voltage and Current](#35-measuring-voltage-and-current)
- [3.6 Measuring Resistance — The Wheatstone Bridge](#36-measuring-resistance--the-wheatstone-bridge)
- [3.7 Delta-to-Wye (Pi-to-Tee) Equivalent Circuits](#37-delta-to-wye-pi-to-tee-equivalent-circuits)
- [Practical Perspective: Resistive Touch Screens](#practical-perspective-resistive-touch-screens)
- [Summary of Key Equations](#summary-of-key-equations)

---

## 3.1 Resistors in Series

### Definition

Two elements connected at a single node with no other elements at that node are said to be in **series**. Series-connected circuit elements carry the **same current**.

### Equivalent Resistance

For $k$ resistors connected in series, the equivalent resistance is the sum of the individual resistances:

$$
\boxed{R_{\text{eq}} = \sum_{i=1}^{k} R_i = R_1 + R_2 + \cdots + R_k}
$$

**Key property:** The equivalent resistance of a series connection is always **larger** than the largest resistor in the connection.

### Derivation

Applying Kirchhoff's voltage law around the loop with $k$ series resistors:

$$
v_s = i_s(R_1 + R_2 + \cdots + R_k) = i_s R_{\text{eq}}
$$

### Black Box Equivalence

The concept of equivalent resistance allows us to replace any collection of series resistors with a single resistor that produces the same terminal voltage-current relationship. This is often visualized using a **black box** — the contents are hidden, and only the terminal behavior matters.


---

## 3.2 Resistors in Parallel

### Definition

Two elements connected at **both** of their nodes are said to be in **parallel**. Parallel-connected circuit elements have the **same voltage** across their terminals.

> **Important:** Do not assume two elements are parallel merely because they appear aligned in parallel in a circuit diagram. The defining characteristic is that they share the **same two nodes**.

### Equivalent Resistance

For $k$ resistors connected in parallel:

$$
\boxed{\frac{1}{R_{\text{eq}}} = \sum_{i=1}^{k} \frac{1}{R_i} = \frac{1}{R_1} + \frac{1}{R_2} + \cdots + \frac{1}{R_k}}
$$

Using conductance ($G = 1/R$):

$$
G_{\text{eq}} = \sum_{i=1}^{k} G_i = G_1 + G_2 + \cdots + G_k
$$

**Key property:** The equivalent resistance of a parallel connection is always **smaller** than the smallest resistor in the connection.

### Special Case: Two Resistors in Parallel

When only two resistors are connected in parallel, the equivalent resistance can be simplified to:

$$
\boxed{R_{\text{eq}} = \frac{R_1 R_2}{R_1 + R_2}}
$$

This form is often easier to use than the reciprocal formula.

### Identifying Parallel Connections

| Configuration | Parallel? | Reason |
|--------------|-----------|--------|
| Two resistors sharing both terminals | Yes | Same voltage across both |
| Resistors lined up visually but not sharing both nodes | No | Different voltages |
| Resistors connected at a single node only | No | They are in series, not parallel |


---

## 3.3 The Voltage-Divider and Current-Divider Circuits

### The Voltage-Divider Circuit

A **voltage divider** consists of two resistors connected in series across a voltage source. It "divides" the source voltage between the two resistors.

$$
v_1 = \frac{R_1}{R_1 + R_2} v_s \quad \text{and} \quad v_2 = \frac{R_2}{R_1 + R_2} v_s
$$

**Key properties:**
- The divided voltages $v_1$ and $v_2$ are always **less than** the source voltage $v_s$
- The voltage ratio is determined solely by the resistance ratio
- An infinite number of resistor pairs can produce the same voltage division

### Effect of Loading on Voltage Dividers

When a load resistor $R_L$ is connected in parallel with $R_2$, the output voltage changes:

$$
v_o = v_s \cdot \frac{R_{\text{eq}}}{R_1 + R_{\text{eq}}} \quad \text{where} \quad R_{\text{eq}} = \frac{R_2 R_L}{R_2 + R_L}
$$

To minimize loading effects: **$R_L \gg R_2$** (load resistance much larger than the divider resistance).


### The Current-Divider Circuit

A **current divider** consists of two resistors connected in parallel across a current source. It "divides" the source current between the two resistors.

$$
i_1 = \frac{R_2}{R_1 + R_2} i_s \quad \text{and} \quad i_2 = \frac{R_1}{R_1 + R_2} i_s
$$

**Key insight:** The current in one resistor equals the entering current multiplied by the **other resistance** divided by the sum. This is the "opposite" of voltage division.


---

## 3.4 Voltage Division and Current Division

### General Voltage Division

For $n$ resistors in series with total voltage $v$ across them, the voltage across any single resistor $R_j$ is:

$$
\boxed{v_j = \frac{R_j}{R_{\text{eq}}} v}
$$

Where $R_{\text{eq}} = R_1 + R_2 + \cdots + R_n$.

### General Current Division

For $n$ resistors in parallel with total current $i$ entering the combination, the current through any single resistor $R_j$ is:

$$
\boxed{i_j = \frac{R_{\text{eq}}}{R_j} i}
$$

Where $1/R_{\text{eq}} = 1/R_1 + 1/R_2 + \cdots + 1/R_n$.

### When to Use

| Technique | Use When | Key Equation |
|-----------|----------|--------------|
| Voltage division | Finding voltage across one resistor in a series string | $v_j = (R_j/R_{\text{eq}}) v$ |
| Current division | Finding current through one resistor in a parallel group | $i_j = (R_{\text{eq}}/R_j) i$ |

> **Caution:** Voltage division applies **only** to series-connected resistors. Current division applies **only** to parallel-connected resistors. Using these tools inappropriately leads to incorrect results.

---

## 3.5 Measuring Voltage and Current

### Analog Meters (d'Arsonval Movement)

Analog meters are based on the **d'Arsonval meter movement**, which consists of a movable coil in a permanent magnet field. The coil is characterized by:
- A **current rating** (e.g., 1 mA) — full-scale deflection current
- A **voltage rating** (e.g., 50 mV) — voltage drop at full scale

### Ammeter Design

An **ammeter** consists of a d'Arsonval movement in **parallel** with a shunt resistor $R_A$:

- The shunt resistor diverts most of the current around the delicate movement
- Full-scale reading is determined by $R_A$
- **Equivalent resistance:** $R_m = R_{\text{movement}} \parallel R_A$ (ideally very small)

### Voltmeter Design

A **voltmeter** consists of a d'Arsonval movement in **series** with a multiplier resistor $R_v$:

- The multiplier resistor limits the voltage across the movement
- Full-scale reading is determined by $R_v$
- **Equivalent resistance:** $R_m = R_v + R_{\text{movement}}$ (ideally very large)

### Meter Loading Effects

All real meters disturb the circuit being measured:

| Meter Type | Ideal Resistance | Actual Behavior | Loading Concern |
|-----------|-----------------|-----------------|-----------------|
| Ammeter | 0 Ω | Small but non-zero resistance | Adds series resistance; use rule of 1/10th |
| Voltmeter | ∞ | Large but finite resistance | Draws small current; adds parallel resistance |

**Rule of 1/10th:** The effective resistance of an ammeter should be no more than 1/10th of the smallest resistance in the circuit being measured.

### Digital Meters

Digital meters offer advantages over analog meters:
- Introduce **less resistance** into the circuit (still nonideal)
- Easier to connect
- More precise measurements due to digital readout
- Measure continuous signals at discrete **sampling times**

---

## 3.6 Measuring Resistance — The Wheatstone Bridge

### Circuit Configuration

The **Wheatstone bridge** is used to precisely measure resistances in the range of 1 Ω to 1 MΩ with accuracies of about ±0.1%.

The bridge consists of:
- Four resistors ($R_1$, $R_2$, $R_3$, $R_x$)
- A DC voltage source
- A detector (galvanometer) to indicate zero current

### Balanced Bridge Condition

The bridge is **balanced** when no current flows through the galvanometer ($i_g = 0$). At balance:

$$
\boxed{R_x = \frac{R_2}{R_1} R_3}
$$

### Derivation

At balance:
- KCL at node a: $i_1 = i_3$
- KCL at node b: $i_x = i_2$
- KVL (galvanometer path with $R_3$ and $R_x$): $i_x R_x = i_3 R_3$
- KVL (galvanometer path with $R_1$ and $R_2$): $i_1 R_1 = i_2 R_2$

Dividing the two KVL equations and eliminating currents yields the balance equation.

### Practical Considerations

- The ratio $R_2/R_1$ is varied in decimal steps (1, 10, 100, 1000) to cover a wide range
- $R_3$ is adjustable from 1 to 11,000 Ω
- Resistances below 1 Ω are difficult to measure (thermoelectric effects)
- Resistances above 1 MΩ are difficult to measure (leakage currents)


---

## 3.7 Delta-to-Wye (Pi-to-Tee) Equivalent Circuits

### The Problem

Some circuits cannot be simplified using series/parallel combinations alone. The **Wheatstone bridge** (with the galvanometer replaced by its resistance) is one example — it contains a network of five resistors with no series or parallel connections.

### Delta (∆) and Wye (Y) Configurations

| Configuration | Also Called | Shape |
|--------------|-------------|-------|
| Delta (∆) | Pi (π) | Triangle — three resistors forming a loop |
| Wye (Y) | Tee (T) | Star — three resistors meeting at a central node |

### ∆-to-Y Transformation

To convert **delta-connected** resistors ($R_a$, $R_b$, $R_c$) to **wye-connected** resistors ($R_1$, $R_2$, $R_3$):

$$
\boxed{R_1 = \frac{R_b R_c}{R_a + R_b + R_c}}
$$

$$
\boxed{R_2 = \frac{R_a R_c}{R_a + R_b + R_c}}
$$

$$
\boxed{R_3 = \frac{R_a R_b}{R_a + R_b + R_c}}
$$

### Y-to-∆ Transformation

To convert **wye-connected** resistors to **delta-connected** resistors:

$$
\boxed{R_a = \frac{R_1 R_2 + R_2 R_3 + R_3 R_1}{R_1}}
$$

$$
\boxed{R_b = \frac{R_1 R_2 + R_2 R_3 + R_3 R_1}{R_2}}
$$

$$
\boxed{R_c = \frac{R_1 R_2 + R_2 R_3 + R_3 R_1}{R_3}}
$$

### When to Use

Use ∆-to-Y (or Y-to-∆) transformation when:
- A circuit cannot be simplified by series/parallel combinations
- A bridge-like structure is present
- You need to reduce a complex resistive network to a single equivalent resistance

**Strategy:** Identify a ∆ or Y configuration in the circuit, transform it to the other form, then use series/parallel simplification on the resulting circuit.


---

## Practical Perspective: Resistive Touch Screens

### Principle of Operation

Many mobile phones and tablets use **resistive touch screens**. The screen contains a resistive grid in both the x- and y-directions. When the screen is touched, it effectively divides the total resistance into two parts.

### X-Direction Analysis

The touch divides resistance $R_x$ into $R_x\alpha$ and $R_x(1-\alpha)$, forming a voltage divider:

$$
V_x = \frac{R_x\alpha}{R_x\alpha + R_x(1-\alpha)} V_s = \alpha V_s
$$

The touch location parameter:

$$
\alpha = \frac{V_x}{V_s}
$$

### Determining Pixel Coordinates

The x-coordinate of the touch point (in pixels):

$$
x = p_x(1 - \alpha) = p_x\left(1 - \frac{V_x}{V_s}\right)
$$

Where $p_x$ is the total number of pixels in the x-direction.

Similarly for the y-direction:

$$
\beta = \frac{V_y}{V_s} \quad \text{and} \quad y = p_y(1 - \beta)
$$

### Key Points
- $V_x = 0$ when touch is at far right ($\alpha = 0$)
- $V_x = V_s$ when touch is at far left ($\alpha = 1$)
- The pixel value is capped at $p_x - 1$ and $p_y - 1$

---

## Summary of Key Equations

| Equation | Description |
|----------|-------------|
| $R_{\text{eq}} = R_1 + R_2 + \cdots + R_k$ | Series equivalent resistance |
| $\dfrac{1}{R_{\text{eq}}} = \dfrac{1}{R_1} + \dfrac{1}{R_2} + \cdots + \dfrac{1}{R_k}$ | Parallel equivalent resistance |
| $R_{\text{eq}} = \dfrac{R_1 R_2}{R_1 + R_2}$ | Two resistors in parallel |
| $v_j = \dfrac{R_j}{R_{\text{eq}}} v$ | Voltage division (general) |
| $i_j = \dfrac{R_{\text{eq}}}{R_j} i$ | Current division (general) |
| $R_x = \dfrac{R_2}{R_1} R_3$ | Wheatstone bridge balance |
| $R_1 = \dfrac{R_b R_c}{R_a + R_b + R_c}$ | ∆-to-Y transformation |
| $R_a = \dfrac{R_1 R_2 + R_2 R_3 + R_3 R_1}{R_1}$ | Y-to-∆ transformation |

---

## Key Terms

| Term | Definition |
|------|-----------|
| **Series connection** | Elements connected at a single node, carrying the same current |
| **Parallel connection** | Elements connected at both terminals, having the same voltage |
| **Equivalent resistance** | A single resistor that produces the same terminal behavior as a network |
| **Voltage divider** | A circuit that divides a voltage between series resistors |
| **Current divider** | A circuit that divides a current between parallel resistors |
| **Loading effect** | The change in circuit behavior when a measurement device is connected |
| **d'Arsonval movement** | The basic mechanism in analog meters — a coil in a magnetic field |
| **Ammeter** | A device for measuring current (connected in series) |
| **Voltmeter** | A device for measuring voltage (connected in parallel) |
| **Wheatstone bridge** | A circuit for precisely measuring unknown resistances |
| **Balanced bridge** | Condition when no current flows through the galvanometer |
| **Delta (∆) connection** | Three resistors forming a triangular loop |
| **Wye (Y) connection** | Three resistors meeting at a central node (star) |
| **Pi (π) connection** | Alternative name for delta connection |
| **Tee (T) connection** | Alternative name for wye connection |

---

## Problem-Solving Tips

1. **Always look for series and parallel combinations first** — this is the simplest way to reduce a circuit.
2. **Use voltage division for series strings** and **current division for parallel groups** — but never mix them up.
3. **Check your intuition:** Series $R_{\text{eq}}$ > largest resistor; Parallel $R_{\text{eq}}$ < smallest resistor.
4. **Consider loading effects** when connecting meters or loads to voltage dividers — the output voltage will change.
5. **Use the Wheatstone bridge** for precise resistance measurements — it requires balancing the bridge (zero galvanometer current).
6. **Apply ∆-to-Y transformation** when a circuit has no obvious series/parallel combinations — especially bridge configurations.
7. **For the two-resistor parallel formula** ($R_{\text{eq}} = R_1R_2/(R_1+R_2)$): the equivalent is always less than the smaller resistor.
8. **Verify your answer** using power balance or by checking boundary conditions (e.g., what happens when one resistance goes to 0 or ∞?).
