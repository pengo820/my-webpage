# My Webpage
This webpage records some of my insights, ideas, and projects.

Treat it as an **infinite ladder**, so the key trick is **self‑similarity**: “the part after the first section looks exactly like the whole network” 🔁

---

## 1) Define the equivalent resistance
Let the equivalent resistance seen by the source be \(X\).

Look at the first “cell”:

- First there is a **series** resistor \(R\).
- After that node, there is:
  - one **shunt** resistor \(R\) to the bottom rail, **in parallel** with
  - the rest of the ladder, whose equivalent is again \(X\) (because it’s infinite and repeats).

So from that node to ground, the equivalent is:
\[
R \parallel X = \frac{RX}{R+X}
\]

Therefore the total input resistance is:
\[
X = R + (R \parallel X)= R + \frac{RX}{R+X}
\]

---

## 2) Solve the equation
\[
X = R + \frac{RX}{R+X}
\]
Multiply both sides by \((R+X)\):
\[
X(R+X)=R(R+X)+RX
\]
\[
XR+X^2 = R^2+RX+RX = R^2+2RX
\]
Bring all terms to one side:
\[
X^2 - RX - R^2 = 0
\]

Quadratic in \(X\):
\[
X=\frac{R\pm \sqrt{R^2+4R^2}}{2}
= \frac{R\pm R\sqrt{5}}{2}
\]
Take the positive root:
\[
X = \frac{R(1+\sqrt{5})}{2}
\]

With \(R=10\,\Omega\):
\[
X = 10\cdot \frac{1+\sqrt{5}}{2} \approx 16.18\,\Omega
\]

---

## 3) Get the current
\[
I=\frac{V}{X}=\frac{10}{16.18}\approx 0.618\ \text{A}
\]

✅ **Answer:** \(\boxed{I \approx 0.618\ \text{A}}\)

---

If you want, send the exact original problem statement (sometimes the ladder has a slightly different first/last section), and I’ll map the recurrence precisely ⚙️
