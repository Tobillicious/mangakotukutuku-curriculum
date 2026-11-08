# Te Whare Wānanga o Mangakōtukutuku
## Kaiako Guide & Wānanga Solutions Manual
### Pedagogical Architecture, Discussion Frameworks & Worked Mathematical Solutions
*Edition 1.0 (2026) · Dedicated to the Kaiako and Tauira of Mangakōtukutuku College*

---

## 1. Pedagogical Architecture: The Wānanga Method

Teaching advanced science and mathematics through Te Ao Māori is not about adding superficial cultural decoration. It is about recognizing that **ancestral Māori epistemologies and frontier 21st-century science describe the same physical reality.**

### Three Principles for the Classroom:
1. **Tuakana–Teina (Collaborative Mastery):**  
   Pair students who have stronger abstract algebra intuition with students who excel in physical or conceptual storytelling. Advanced problem sets should be tackled in small whānau groups.
2. **Kōrero Pono (No Dumbing Down):**  
   Our students deserve vertical depth. Do not hide the matrices, the differential equations, or the quantum states. Teach them the notation as a language—just as they learn Te Reo Māori.
3. **Whakapapa as Structural Foundation:**  
   Always ground the mathematics back in relation: *"Who is affected? Where does the energy flow? What is the consequence (utu) on the whole system?"*

---

## 2. Complete Worked Solutions & Discussion Guides

### Unit 1: Ngā Taura Whakapapa (The Relational Web)

#### Discussion Guide:
* **Whakapapa as an Append-Only Ledger:** Highlight that whakapapa cannot be overwritten; new generations are appended to historical roots. In computer science, this is an immutable directed acyclic graph (DAG) or blockchain. Authentic mana is grounded in this verifiable continuity.
* **The Myth of Free Disposal:** Connect BCRD Axiom P1 (no outside) to environmental chemistry. When a factory dumps runoff into an awa, the matter does not disappear. It alters the chemical potential and ecology of the entire catchment.

#### Worked Solutions to Mathematical Exercises:
**Exercise 1: Graph Laplacian of the 4-Node Ecosystem**
* Given Adjacency Matrix $\mathbf{A}$:
  $$\mathbf{A} = \begin{pmatrix} 0 & 1 & 1 & 1 \\ 1 & 0 & 1 & 0 \\ 1 & 1 & 0 & 1 \\ 1 & 0 & 1 & 0 \end{pmatrix}$$
* **Degree Matrix $\mathbf{D}$:**  
  Row sums:
  - Node 1 (Awa): $0 + 1 + 1 + 1 = 3$
  - Node 2 (Flora/Fauna): $1 + 0 + 1 + 0 = 2$
  - Node 3 (Community): $1 + 1 + 0 + 1 = 3$
  - Node 4 (Sensor Network): $1 + 0 + 1 + 0 = 2$  
  *Result:* Node 1 (Awa) and Node 3 (Community) share highest degree centrality ($d = 3$).
* **Graph Laplacian $\mathbf{L} = \mathbf{D} - \mathbf{A}$:**
  $$\mathbf{L} = \begin{pmatrix} 3 & -1 & -1 & -1 \\ -1 & 2 & -1 & 0 \\ -1 & -1 & 3 & -1 \\ -1 & 0 & -1 & 2 \end{pmatrix}$$
* **Eigenvalue Analysis:**
  - The rows sum to zero, confirming that $\lambda_1 = 0$ with eigenvector $\vec{v}_1 = (1, 1, 1, 1)^T$.
  - The second eigenvalue (algebraic connectivity / Fiedler value) is $\lambda_2 \approx 1.586 > 0$.
  - *Physical Meaning:* Because $\lambda_2 > 0$, the graph is fully connected. Perturbations or restoration efforts injected at any node disperse across the whole community network.

---

### Unit 2: Te Mauri me te Hihiko (Energy, Entropy & Erasure)

#### Worked Solutions to Mathematical Exercises:
**Exercise 1: Landauer Power Bill of a Smartphone**
* Number of bit erasures per second: $\dot{N} = 10^{11}\text{ bits/s}$.
* Temperature: $T = 300\text{ K}$.
* Theoretical minimum heat dissipation:
  $$P_{\text{Landauer}} = \dot{N} \cdot k_B T \ln 2$$
  $$P_{\text{Landauer}} = (10^{11}\text{ s}^{-1}) \cdot (1.3806 \times 10^{-23}\text{ J/K}) \cdot (300\text{ K}) \cdot (0.69315)$$
  $$P_{\text{Landauer}} \approx 2.87 \times 10^{-10}\text{ Watts} = 0.287\text{ nanoWatts}$$
* **Comparison to Battery Power ($\approx 2\text{ W}$):**
  $$\text{Ratio} = \frac{2.87 \times 10^{-10}\text{ W}}{2\text{ W}} \approx 1.4 \times 10^{-10} = 0.000000014\%$$
* *Pedagogical Takeaway:* Over $99.999999\%$ of a phone's energy is wasted as resistive joule heating in conventional CMOS wires! Fundamental information physics shows that computation could theoretically be billions of times more efficient if designed reversibly.

**Exercise 2: Toffoli Reversible Logic Gate**
* Mapping: $(x, y, z) \mapsto (x,\, y,\, z \oplus (x \land y))$.
* Input: $(1, 1, 0)$.
  - $x = 1, y = 1, z = 0$.
  - $x \land y = 1 \land 1 = 1$.
  - New $z' = 0 \oplus 1 = 1$.
  - *Output:* $(1, 1, 1)$.
* **Feeding output back into Toffoli:**
  - Inputs to second gate: $x' = 1, y' = 1, z' = 1$.
  - $x' \land y' = 1 \land 1 = 1$.
  - New $z'' = 1 \oplus 1 = 0$.
  - *Recovered State:* $(1, 1, 0)$.
  - *Conclusion:* Because the operation is self-inverse ($\mathbf{T}^2 = \mathbb{I}$), historical state is preserved without entropy dissipation.

---

### Unit 3: Te Hurihanga Nui (Quantum Unitarity & Recurrence)

#### Worked Solutions to Mathematical Exercises:
**Exercise 1: Schwarzschild Radius Calculations**
* Formula: $r_s = \frac{2GM}{c^2}$ where $\frac{2G}{c^2} \approx 1.485 \times 10^{-27}\text{ m/kg}$.
* **Human Being ($M = 70\text{ kg}$):**
  $$r_s = (1.485 \times 10^{-27}\text{ m/kg}) \cdot (70\text{ kg}) \approx 1.04 \times 10^{-25}\text{ meters}$$
  *(This is 10 orders of magnitude smaller than a single proton: $\approx 10^{-15}\text{ m}$!)*
* **The Moon ($M = 7.35 \times 10^{22}\text{ kg}$):**
  $$r_s = (1.485 \times 10^{-27}\text{ m/kg}) \cdot (7.35 \times 10^{22}\text{ kg}) \approx 0.109\text{ millimeters}$$
* *Pedagogical Takeaway:* To create an event horizon, enormous mass must be crushed into microscopic scales against intense quantum electron/neutron degeneracy pressure. Failure to reach $r_s$ leads naturally to bounce, dispersal, or stable remnants—not infinite oblivion.

**Exercise 2: Unitary Matrix Verification**
* Given:
  $$\mathbf{U} = \frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix}$$
* Conjugate Transpose: $\mathbf{U}^\dagger = \mathbf{U}$ (matrix is real and symmetric).
* Product $\mathbf{U}^\dagger \mathbf{U}$:
  $$\mathbf{U}^\dagger \mathbf{U} = \frac{1}{2} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & -1 \end{pmatrix} = \frac{1}{2} \begin{pmatrix} 1+1 & 1-1 \\ 1-1 & 1+1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \mathbb{I}$$
* Determinant: $\det(\mathbf{U}) = \frac{1}{2}((-1) - (1)) = -1$.
  Since $|\det(\mathbf{U})| = 1$, vector lengths and quantum probabilities are strictly conserved.

---

### Unit 4: Te Ture o te Kaitiaki (The Law of the Guardian & AI Safety)

#### Worked Solutions to Mathematical Exercises:
**Exercise 1: Reach-Before-Harm Buffer Geometry**
* Given:
  - $v_{\text{harm}} = 0.5c = 1.5 \times 10^8\text{ m/s}$
  - $v_{\text{signal}} = c = 3.0 \times 10^8\text{ m/s}$
  - $\tau_{\text{resp}} = 10^{-5}\text{ s}$
* Denominator: $1 - \frac{v_{\text{harm}}}{v_{\text{signal}}} = 1 - 0.5 = 0.5$.
* Minimum Safe Buffer:
  $$r_{\text{safe}} > \frac{(1.5 \times 10^8\text{ m/s}) \cdot (10^{-5}\text{ s})}{0.5} = \frac{1500\text{ m}}{0.5} = 3000\text{ meters} = 3.0\text{ kilometers}$$
* *Pedagogical Takeaway:* Physical safety in autonomous networks requires geographic or topological distance so that cryptographic quorum consensus can engage before harm fronts arrive.

**Exercise 2: Discounted Repeated Payoffs**
* Payoff for Permanent Care ($G$):
  $$\text{Payoff}(G) = 10 + \frac{0.9}{1 - 0.9} \times 10 = 10 + 9 \times 10 = 100$$
* Payoff for Single Defection then Quarantine ($D$):
  $$\text{Payoff}(D) = 12 + \frac{0.9}{1 - 0.9} \times 1 = 12 + 9 \times 1 = 21$$
* *Conclusion:*
  $$100 \gg 21$$
  Mutual care ($G$) produces nearly **five times** the long-term utility of predatory defection ($D$). Reciprocity dominance is mathematically unassailable.

---
*Mangakōtukutuku College Non-Commercial Educational Resources · Edition 1.0 (2026)*

