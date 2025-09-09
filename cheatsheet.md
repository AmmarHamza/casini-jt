# Cheatsheet — Core formulas & concepts (Casini + JT hybrid project)

**Author:** Ammar Hamza Saad Abdulraheem  
**Purpose:** Quick reference for the hybrid Casini (relative entropy) + JT island project.

---

## Quantum information basics
**Von Neumann entropy**
\[
S(\rho) = -\mathrm{Tr}\, (\rho \ln \rho)
\]

**Relative entropy (quantum Kullback–Leibler)**
\[
S(\rho \| \sigma) = \mathrm{Tr}\,(\rho \ln \rho) - \mathrm{Tr}\,(\rho \ln \sigma) \ge 0
\]
(positivity: equality iff \(\rho = \sigma\).)

**Key identity (Casini-style)**
If \(\sigma = e^{-K}/\mathrm{Tr}(e^{-K})\) (modular state), define
\[
\Delta S = S(\rho) - S(\sigma), \qquad \Delta K = \mathrm{Tr}(K\rho) - \mathrm{Tr}(K\sigma).
\]
Then
\[
S(\rho\|\sigma) = \Delta K - \Delta S \ge 0 \quad\Rightarrow\quad \Delta S \le \Delta K.
\]

---

## Modular Hamiltonian (intuition & common forms)
- **Definition (formal):** \(\sigma = e^{-K}/\mathrm{Tr}(e^{-K})\); \(K\) is the modular Hamiltonian for \(\sigma\).  
- **Rindler wedge (heuristic, QFT vacuum restricted to \(x>0\)):**
\[
K = 2\pi \int_{x>0} x\, T_{00}(x)\, dx
\]
(This gives the intuitive weight-by-distance factor appearing in Casini's arguments.)

- **Interval in 1+1D CFT:** modular Hamiltonian is known for an interval in a CFT; uses conformal maps — see references.

---

## Bekenstein-style bound (schematic)
For a weakly gravitating localized system of energy \(E\) and size \(R\), a common schematic form is
\[
S \le 2\pi \frac{E R}{\hbar}
\]
Casini's derivation recasts such bounds in terms of relative entropy and modular Hamiltonians in QFT.

---

## JT gravity (very short sketches)
**JT action (schematic, conventions vary):**
\[
I_{\mathrm{JT}} = -\frac{1}{2}\int d^2x\sqrt{-g}\,\phi(R+2) + \text{boundary terms}
\]
where \(\phi\) is the dilaton field.

**Island formula (schematic):**
For radiation region \(\mathrm{Rad}\),
\[
S(\mathrm{Rad}) = \min_{\text{islands}} \mathrm{Ext}_I\left[ \frac{\mathrm{Area}(\partial I)}{4G_N} + S_{\text{matter}}(\mathrm{Rad}\cup I) \right]
\]
(Used to compute fine-grained entropy of radiation including semiclassical gravitational saddle contributions.)

---

## Useful symbolic/numeric checks (toy ideas)
- Compute relative entropy between two Gaussians as a toy model:
  \(S(p\|q)=\int p(x)\ln\frac{p(x)}{q(x)}dx\) — analytically tractable and good for series expansion checks.
- For modular Hamiltonian checks, compare \(\Delta K\) integrals for small excitations to the perturbative expansion of \(\Delta S\) (relative entropy series).

---

## Short list of references (start here)
1. H. Casini, "Relative entropy and the Bekenstein bound" (2008).  
2. R. Bousso, "The holographic principle" (Rev. Mod. Phys., 2002).  
3. Almheiri / Engelhardt / Marolf / Maxfield / Penington papers (2019–2020) — replica wormholes & islands.  
4. Lecture notes: David Tong (QFT), Srednicki (entanglement intro), Maldacena/Stanford (SYK/JT notes).

---

## Quick reminders
- Keep units consistent (I often use \(\hbar = c = 1\) in derivations; restore factors when comparing to physical bounds).  
- If analytic integrals diverge, isolate vacuum divergence and compute finite differences (Casini’s method subtracts vacuum contributions to get finite ΔS).  
- Always provide a short README and a 1-page non-technical summary for supervisors.

---

*If you want, I can also create a printable PDF of this cheatsheet and put it in the repo.*
