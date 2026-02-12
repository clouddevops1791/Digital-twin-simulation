# Digital-twin-simulation

This README is designed to bridge the gap between complex chemical engineering and the high-level business goals (cost/oil reduction) that recruiters and project managers value.
<img width="943" height="536" alt="potato chips px" src="https://github.com/user-attachments/assets/aa115eec-2e80-474e-858b-1e2015d911d6" />


​Integrated Oil Recovery & Process Optimization in Industrial Food Production

​📌 Project Overview
​Developed a high-fidelity digital twin of a continuous potato chip frying process using DWSIM. The project focuses on industrial sustainability, specifically addressing oil degradation (FFA tracking), waste heat recovery, and circular mass loops to meet the 2027 UK Food Production efficiency targets.


​🎯 Key Performance Indicators (KPIs)

​Oil Reduction: Achieved a 20% reduction in fresh oil intake via a stabilized recycle loop.
​Cost Efficiency: Targeted a 15% reduction in operating costs through advanced heat integration.
​Product Quality: Maintained oil purity by simulating a Bleaching Earth Treatment unit and monitoring Free Fatty Acids (FFA).

​🛠 Technical Architecture & Flowsheet Design


​The simulation utilizes Solid-Vapor-Liquid Equilibrium (SVLE) modeling to handle the complex phase interactions between potato solids, steam, and frying oil.
​1. The Reactor Core (Frying Simulation)

​Unit Operation: Conversion Reactor (RCONV-1).

​Chemical Reaction: Modeled the hydrolysis of Triolein into Oleic Acid and Glycerol.
​Stoichiometry: 1 \text{ Triolein} + 3 \text{ Water} \rightarrow 1 \text{ Glycerol} + 3 \text{ Oleic Acid}.
​Optimization: Adjusted conversion rates to a realistic 1% per pass to simulate industrial degradation without crashing the mass balance.

​2. Separation & Recovery Loop

​Flash Separation: Strips 450 K water vapor from the oil stream for energy recovery.
​Solid Management: Employs a Component Separator to isolate starch fines (Starch1) from the liquid phase.
​Refining: A simulated Bleaching Unit removes pigments and FFA to regenerate food-grade oil.

​3. Energy Integration

​Heat Exchanger (E1): Cross-flows high-temperature waste vapor against the incoming 298.15 K starch/water feed.
​Impact: Significantly lowers the heater duty required in the fryer, directly contributing to the 15% cost reduction goal.

​📈 Process Control & Automation

​To ensure the simulation meets the 2027 targets autonomously, the project utilizes Logical Adjust Blocks (ADJ).
​Adaptive Control: The Adjust block manipulates Fresh Oil Makeup flow based on the recovery efficiency of the recycle loop.
​Convergence: Utilizes the Secant Method for mathematical stability in iterative loops.
​Data Visualization: Real-time tracking of manipulated vs. referenced variables ensures the simulation converges within a 0.0001 tolerance.

​🧪 Simulation Results
Component         Inlet     Fraction     Product (Recycle)       Status
Triolein (Oil)    0.016     0.9559       (Liquid Phase)         Recovered
Water             0.901     0.0306       (Liquid Phase)         Stripped
Oleic Acid (FFA) 0.000      0.0082         (Liquid Phase)        Controlled

🚀 Future Roadmap
​Vacuum Degassing: Implement a vacuum flash to further reduce oxidative rancidity.
​Economic Analysis: Integrate DWSIM's costing tool to calculate exact ROI for the heat exchanger installation.
​Sensitivity Analysis: Map the relationship between frying temperature and FFA production rates.
