# Week 2 — The Momentum Principle (CS50-Style Mastery Track)

> **Goal:** Achieve mastery of the Momentum Principle by solving the hardest problems first, reasoning from first principles, and treating physics like executable logic rather than memorized formulas.

This week follows a **CS50-style structure**:

* Fewer problems
* Higher difficulty
* Deep conceptual compression
* Simulation and iteration over algebra

---

## Phase 1: The CS50 Logic Check (State & Update)

**Goal:** Understand that **Force is not motion** — force is what **updates momentum**.

### Problems

* **Q1 (Impulse Logic)**
  Especially focus on cases where force and velocity point in the same or opposite directions.
  This problem forces a clean separation between:

  * Direction of motion
  * Direction of force
  * Change in *magnitude* vs *direction* of momentum

* **Q7 (Direction of Δp)**
  A brief force acts on a moving object.
  The task is to determine the direction of the **change in momentum**, not velocity.

* **••P14 (Perpendicular Kick — Boss Fight)**
  A block moving in one direction is kicked perpendicular to its motion.
  This problem unifies:

  * Impulse
  * Component independence
  * Direction vs magnitude changes
  * Real collision reasoning

**Stop Phase 1 when you can confidently say:**

> *Force changes momentum, not velocity, and only in its own direction.*

---

## Phase 2: The Iterative Loop (The Algorithm)

**Goal:** Be able to **run physics step-by-step**, like a simulation engine.

### Problems

* **••P22 (Mars Probe — Iterative Update)**
  Given position, momentum, and net force, predict the future state using two time steps.

  Core update loop:

  ```
  p = p + F_net * Δt
  r = r + (p / m) * Δt
  ```

* **••P12 (Proton with Tiny Δt)**
  A proton experiences a force over an extremely small time interval.
  This problem forces trust in the Momentum Principle even at microscopic scales.

**Stop Phase 2 when:**
You can write the update loop from memory and explain *why the update order matters*.

---

## Phase 3A: Design & Engineering Thinking (Planning Motion)

**Goal:** Move from solving equations to **planning motion**.

### Choose ONE

* **••P24 (Space Hallway Path Planning)** *(Recommended)*
  Move a heavy load through a 90° hallway using only three impulse blasts.

  This is:

  * Path planning
  * Impulse scheduling
  * Constraint-based reasoning

  There is no single “formula solution” — only good physics decisions.

**OR**

* **••P19 (Asteroid Deflection Feasibility)**
  Estimate whether a rocket can deflect a dangerous asteroid.

  Focus on:

  * Orders of magnitude
  * Assumptions
  * Physical plausibility

---

## Phase 3B: Hardware Stress Test (Collisions)

**Goal:** Understand why real objects break, crumple, and survive.

### Problem

* **••P17 (The Truck Crash)**

  **Setup:**
  A 2500 kg truck traveling at 24 m/s crashes into a concrete wall and crumples by 0.72 m.

  **Goal:**

  * Estimate the **time of collision**
  * Find the **average force** exerted by the wall

  **Mastery Point:**
  Force is **change in momentum divided by time**.

  If the collision time is very small:
  [
  F = \frac{\Delta p}{\Delta t} \rightarrow \text{huge}
  ]

  This is why:

  * Crumple zones increase collision time
  * Increasing Δt saves lives

---

## Phase 4: Computational Capstone (Simulation + Graphs)

**Goal:** Make momentum and force *visible*.

### Problems

* **••P48 (Fan Cart Simulation)**
  Build a VPython model of a cart on a low-friction track acted on by a constant force.

* **••P49 (Graphs of Motion)**
  Add graphs of:

  * Position vs time
  * Momentum vs time

  **Aha Moment:**

  * Constant force → momentum is a straight line
  * Linear momentum → position is a parabola
    Calculus appears *on the screen*, not in equations.

---

## Phase 5: Final Project — Relativistic God-Mode

**The intersection of everything learned so far.**

### •••P51 — The Interstellar Tug (Final Boss)

**The Setup:**
A spacecraft is pulled toward Alpha Centauri with a constant force for many years.

**The Goal:**

* Determine the **maximum speed** at the halfway point
* Determine the **total travel time**

**The Mastery Point:**
You **must** use the **relativistic momentum formula**, not classical momentum.

As the ship approaches the speed of light:

* Momentum continues to increase
* The same force produces **smaller and smaller increases in speed**
* Classical intuition fails completely

> *This problem is the closest thing to reading the source code of space-time.*

---

## Philosophy (Read This)

* You are not aiming for **coverage**
* You are aiming for **compression into understanding**
* Easy problems are sanity checks
* Hard problems contain the chapter

> **If the hardest problems make sense, the chapter is already yours.**

---

## Completion Criteria (CS50-Style)

You have mastered Week 2 if you can:

* Explain momentum change without mentioning acceleration
* Predict direction and magnitude changes from force alone
* Write and trust the iterative update loop
* Explain why perpendicular forces change direction but not speed
* Explain why increasing collision time reduces force
* Explain why relativity becomes unavoidable near (c)

---

**Onward.**
