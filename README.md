## ☕ BrewForge: Coffee Brewing Physics Simulator

**BrewForge** is the second installment in the Forge Series, shifting focus from the chemical transformation of the roast to the **physics of extraction**. It is a high-fidelity browser-based simulator that models fluid dynamics, thermal decay, and extraction kinetics across multiple brewing methods.

By calculating the interaction between water chemistry, temperature stability, and mechanical agitation, BrewForge predicts the **TDS (Total Dissolved Solids)** and **Extraction Yield** of a simulated cup.

---

## 🛠 Features

* **Multi-Method Physics:** Custom logic for **Espresso, Pour Over, French Press, AeroPress, Cold Brew,** and **Moka Pot**.
* **Extraction Kinetic Engine:** Models flavor emergence based on water hardness (ppm), pressure dynamics, and agitation.
* **Thermal Stability Tracking:** A real-time graphing system that plots the temperature drop (T_{drop}) based on the thermal mass of the coffee bed and ambient cooling.
* **Sensory Prediction:** Translates mathematical extraction data into qualitative markers: **Balance, Body, Clarity, Sweetness,** and **Brightness**.
* **Forge-Link Integration:** Standardized JSON export for pharmacokinetic analysis.

---

## 🔗 The Forge Workflow: Integration with GrindForge

BrewForge does not exist in a vacuum. It is designed to ingest data from **GrindForge**, the series' particle distribution simulator.

1. **RoastForge (Origin):** Defines the bean density and brittleness.
2. **GrindForge (The Bridge):** Takes the roasted bean data to simulate **Particle Surface Area** and **Fines Production**. The specific micron (\mu m) distribution and unimodal vs. bimodal profiles generated in GrindForge serve as the primary "Resistance" variable in the BrewForge extraction model.
3. **BrewForge (The Result):** Uses the surface area data from GrindForge to calculate the speed of the **Solvation Phase** and the diffusion rate of soluble compounds.

> **Note:** Without the precise surface area calculations from **GrindForge**, BrewForge utilizes optimized method-specific presets for grind distribution.

---

## 🧪 The Science Behind the Simulation

### 1. Extraction Theory

BrewForge calculates the Extraction Yield (EY) based on the surface area access defined by the grind profile:



The simulation targets the "Sweet Spot" between **18% and 22%**, modeling how grind-induced "fines" contribute to bitterness (over-extraction) while "boulders" can lead to sourness (under-extraction).

### 2. Thermodynamic Decay

The simulator models the "slurry temperature." It accounts for the energy loss that occurs when water hits the coffee bed, calculated as a function of the **Coffee-to-Water Ratio** and the thermal mass of the brewing vessel.

---

## 🚀 How to Use

1. **Import or Select Method:** Choose your brewing gear.
2. **Sync Grind Profile:** Ensure your **GrindForge** data (Coarse, Medium, or Fine) is set. Note how a finer grind distribution significantly increases the extraction rate but risks clogging the flow.
3. **Dial In Parameters:** Adjust water temperature and hardness.
4. **Monitor the Brew:** Click **"Start Brewing"** to watch the real-time extraction.
5. **Export:** Generate the profile to see estimated **Bioavailability** and **Absorption Rate**.

---

## 📂 Installation

BrewForge is a standalone tool.

1. Save the code as `brewforge.html`.
2. Open in any modern evergreen browser.
3. *No dependencies or libraries.*

---
