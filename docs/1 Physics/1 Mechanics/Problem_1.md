This is a great interdisciplinary physics-computation project. Here's how you can approach **Problem 1: Investigating the Range as a Function of the Angle of Projection** in a structured, insightful way.

---

# 📘 **Projectile Motion Analysis: Range vs Angle of Projection**

---

## 1. **Theoretical Foundation**

### 📌 Assumptions (Ideal Case):

* No air resistance
* Constant gravitational acceleration $g$
* Initial height $h = 0$
* 2D motion in a vertical plane

### ✅ Deriving Equations of Motion

**From Newton’s laws:**
Let:

* $v_0$: Initial speed
* $\theta$: Angle of projection
* $g$: Gravitational acceleration

#### Component velocities:

* Horizontal: $v_{0x} = v_0 \cos(\theta)$
* Vertical: $v_{0y} = v_0 \sin(\theta)$

#### Equations of motion:

* Horizontal displacement:

  $$
  x(t) = v_0 \cos(\theta) \cdot t
  $$
* Vertical displacement:

  $$
  y(t) = v_0 \sin(\theta) \cdot t - \frac{1}{2}gt^2
  $$

#### Time of flight (until $y(t) = 0$):

$$
t_f = \frac{2v_0 \sin(\theta)}{g}
$$

#### Range $R$:

$$
R = x(t_f) = v_0 \cos(\theta) \cdot \frac{2v_0 \sin(\theta)}{g}
$$

$$
\boxed{R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}}
$$

---

## 2. **Analysis of the Range**

### 🔍 How Range Depends on the Angle:

The function:

$$
R(\theta) = \frac{v_0^2 \sin(2\theta)}{g}
$$

* Maximized when $\sin(2\theta) = 1 \Rightarrow \theta = 45^\circ$
* Symmetry: $R(\theta) = R(90^\circ - \theta)$

### 📊 Effect of Other Parameters:

* **Increasing $v_0$**: Increases range quadratically.
* **Increasing $g$** (e.g., other planets): Decreases range.

---

## 3. **Practical Applications**

Real-world scenarios often **deviate** from the ideal model:

| Scenario                      | Key Modifications                                       |
| ----------------------------- | ------------------------------------------------------- |
| Uneven terrain                | Solve for $y = 0$ at a different height                 |
| Air resistance                | Introduce drag force $F_d = -kv$                        |
| Wind                          | Adjust horizontal velocity $v_{0x} \pm v_{\text{wind}}$ |
| Launch from height $h \neq 0$ | Quadratic formula needed to find time of flight         |

---

## 4. **Implementation in Python**

We’ll implement a simple simulation and visualization using `matplotlib` and `numpy`.

### ✏️ Python Code
![alt text](<download (1).png>)

## 📈 Example Visualization:

The plot will show a symmetric parabola peaking at 45°, affirming the theoretical result.

---

## 🧩 Limitations of the Ideal Model

| Limitation           | Real-World Factor                           |
| -------------------- | ------------------------------------------- |
| No drag              | Air resistance can drastically reduce range |
| Flat terrain         | Real terrain is uneven                      |
| Constant g           | Varies slightly with altitude               |
| Instantaneous launch | Real objects take time to accelerate        |

---

## 🔄 Extensions & Realistic Modeling Ideas

* Add air resistance (numerical ODE solutions using `scipy.integrate`)
* Vary launch height and solve $y(t) = 0$ using quadratic formula
* 3D projectile motion (with azimuthal angle)
* Monte Carlo simulations for uncertain launch conditions

---

## ✅ Deliverables Summary

* ✅ Markdown/Python notebook with code
* ✅ Equations derived step-by-step
* ✅ Plot of range vs angle
* ✅ Discussion of model limitations and improvements

---

