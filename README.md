# 🧠 Brain Network Modelling with TVB

--------

## 📝 Short introduction on the project
Hi everyone! I'm Susanna, I worked on this project with my colleague and friend Claudia for our Brain Modelling course (BSc in Artificial Intelligence). Our goal was to explore how the dynamic activity of the brain (*Functional Connectivity*) emerges from its fixed physical "wiring" (*Structural Connectivity*). To do this, we simulated whole-brain activity using two radically different mathematical models (the Reduced Wong-Wang and the Wilson-Cowan models) inside **The Virtual Brain (TVB)** simulator. 

--------

## 🛠️ Technologies/tools used
* **Python 3** - The core language for our simulations and data analysis.
* **The Virtual Brain (TVB)** - An amazing neuroinformatics platform for full-brain network simulations.
* **Jupyter Notebook** - Used to write the code, run simulations, and display results interactively.
* **NumPy & Pandas** - For data manipulation and matrix calculations.
* **Matplotlib & Seaborn** - To visualize complex brain connectivity matrices and correlation plots.

--------

## ✨ Features
* **Whole-Brain Simulation:** We successfully simulated brain activity based on real anatomical constraints (white matter tracts).
* **Model Comparison:** A deep dive into two different mean-field models:
  * *Reduced Wong-Wang (RWW):* Great for capturing slow, attractor-like dynamics and robust synchronization.
  * *Wilson-Cowan (WC):* A two-population (excitatory-inhibitory) model that preserves richer local dynamics.
* **Parameter Optimization:** We tuned the global coupling parameter (`G`) to find the "sweet spot" where simulated functional connectivity best matches real brain behavior.
* **Mathematical Evaluation:** We used spatial correlation metrics to objectively compare how well our simulated brain states mirrored theoretical expectations.

--------

## 🚀 Process
We started by loading the brain's physical "wiring diagram" (Structural Connectivity) into The Virtual Brain simulator. Then, we applied our two mean-field models (RWW and WC) to these physical connections. 
We ran computational simulations to generate artificial brain activity. After generating the data, we computed the Functional Connectivity (FC) matrices. The most challenging and rewarding part was the optimization phase: we iteratively adjusted the global coupling parameter to see how the mathematical brain reacted, eventually finding the optimal balance between physical constraints and dynamical freedom.

--------

## 🧠 What I learned
From a technical perspective, I learned how to use *The Virtual Brain* framework and how to translate complex differential equations into Python code to simulate neural populations. 

But conceptually, I learned something even more interesting: anatomical structure is necessary, but not enough on its own to explain full brain dynamics. I discovered that the biological brain likely operates near a "critical bifurcation point" which is a perfect balance where fixed physical structures and flexible, dynamic thoughts coexist. Realizing that we could simulate this biological phenomenon using code was an incredibly rewarding experience.

--------

## 🔧 How could it be improved
If we had more time to expand this research, I would love to:
* **Test on Patient Data:** Apply these simulations to empirical data from patients (e.g., comparing a healthy connectome to one with a neurological condition like Alzheimer's).
* **Try Other Models:** Experiment with different neural mass models, like the Kuramoto or Jansen-Rit models, to see how they handle brain oscillations.
* **Longer Simulations:** Run much longer simulations on high-performance computers to capture even slower, more complex brain wave patterns.

--------
## ▶️ How to run the project
I highly recommend exploring the notebook to see the brain matrices and optimization results!

1. **Clone the repository:**
   Open your terminal and run:
   ```bash
   git clone [https://github.com/SusannaMazzocchi/Brain_Simulation_TVB.git](https://github.com/SusannaMazzocchi/Brain_Simulation_TVB.git)
   cd Brain_Modelling_TVB

2. Check the requirements:
Please read the requirements.txt file carefully. It contains all the instructions to set up your virtual environment and install TVB along with the necessary plotting libraries.

3. Load the right Connectome:
When setting up the simulation in the notebook, make sure to use the data connectivity 76 (which represents the default TVB connectome featuring 76 distinct brain regions).

4. Open the Notebook:
Start Jupyter to view and run the simulation code:
   ```bash
    jupyter notebook brain_modeling.ipynb
(Alternatively, you can upload the notebook and run it directly in Google Colab!).
------------
Please read our complete report; inside, you will find all the in-depth data analysis, the mathematical evaluations, and the graphs we generated to compare the RWW and WC models.
