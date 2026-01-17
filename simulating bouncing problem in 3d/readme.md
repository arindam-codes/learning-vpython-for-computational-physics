# Learning Physics by Simulation

## Problem Reflection — Bouncing Particle (Matter & Interactions Chapter 1 •••P79)

This problem took me significant time, not because it was computationally difficult, but because I deliberately chose to solve it **from scratch using first principles**, without copying a ready-made approach.

### Initial Approach (What Didn’t Work)

My first instinct was to think in terms of **angles, unit vectors, and geometric relations**. I tried to reason about the bounce by directly manipulating directions in 3D space. After spending more than 20 minutes stuck in this approach, I realized that although mathematically valid, it was not the *right way to think* about the physics.

At that point, I consciously decided to **change my perspective instead of forcing the same method**.

### Key Insight: Dimensional Decomposition

Even though the motion occurs in **3D**, I noticed that the **bounce itself happens against a plane**. This means the collision can be understood by decomposing the motion into **independent components along the x, y, and z axes**.

By analyzing the motion component-wise, I observed:

* The **x-component of velocity does not change**
* The **component perpendicular to the surface changes sign**

This led to an important general realization:

> To analyze compound motion in 2D or 3D, always decompose it into **independent motions along x, y, and z axes**.

### Question That Changed Everything

At this stage, a deeper question arose:

**If the direction of velocity changes during a bounce, why doesn’t the magnitude of velocity change?**

This forced me to step away from code and revisit **fundamental physics principles**.

### Work–Energy Perspective (Core Physics Insight)

During a collision with a rigid surface:

* The **displacement of the particle is along the surface**
* The **force exerted by the surface is perpendicular (normal) to the surface**

Therefore:

* Force ⟂ displacement
* ( vec F dot vec d = 0 )
* Work done = 0

Using the work–energy theorem:
[
W = Delta K
]

Since total work done is zero:
[
Delta K = 0 -> K_i = K_f -> |v_i| = |v_f|
]

This led to a powerful takeaway:

> **A force perpendicular to motion can change direction without changing speed.**
> **Speed changes come from forces parallel to motion.**

This insight not only explained the bounce but also connected to broader ideas like circular motion and constraint forces.

### Final Implementation

With the physics clear, the correct simulation logic became obvious:

* Use **event-based collision detection (`if`)**
* Dynamically update velocity by flipping only the perpendicular component
* Never hard-code outcomes; encode **physical laws**

### Simulation Link

🔗 **GlowScript Simulation:**
[https://www.glowscript.org/#/user/arindam.bhattacharjee.codes/folder/testing/program/bouncing.py](https://www.glowscript.org/#/user/arindam.bhattacharjee.codes/folder/testing/program/bouncing.py)

### Handwritten Notes

Below are my handwritten derivations and reasoning (apologies for handwriting quality — clarity over aesthetics):

![Handwritten Solution 1](https://github.com/user-attachments/assets/0780eb73-1ee5-4d5a-b998-4cf19cc03dfd)
![Handwritten Solution 2](https://github.com/user-attachments/assets/677175a6-2fce-48f3-a06c-c69642064e40)
![Handwritten Solution 3](https://github.com/user-attachments/assets/ce864a70-1c90-4349-bf5b-cd7bde33e241)

---

### Final Takeaway

This problem reinforced a mindset I want to carry forward:

> **Don’t memorize physics. Decompose it, question it, and simulate it.**

The struggle was the point — and the understanding was worth it.
