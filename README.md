#  Whale Activity vs UNI Price

This mini-project investigates whether tracking whale activity (large transfers of UNI tokens) can reveal useful signals about price movements and volatility.  

The core question was:  
 *Do whales move the market, or do they just stir the waters?*  

---

## Project Overview

- **Data Collected:**
  - Whale transfer volumes (USD equivalent).
  - UNI token historical price (daily close).

- **Methodology:**
  1. **Whale Transfer Volume (USD):**  
     - Aggregated daily sum of UNI transfers above a “whale threshold.”  
     - Provides a proxy for big-money activity in the ecosystem.  

  2. **UNI Price:**  
     - Daily closing price of UNI.  
     - Used to compare whale movements with market direction.  

  3. **Volatility (7-day rolling standard deviation of returns):**  
     - Measured daily UNI log returns.  
     - Applied a 7-day rolling window to capture “turbulence.”  
     - Helps test if whale spikes correlate with noisier price action.  

  4. **Overlay Visualization:**  
     - Whale transfer volumes plotted as bars.  
     - UNI price plotted as a line on secondary axis.  
     - Makes it easy to visually identify coincidences.  

---

##  Key Findings

- **Price Direction:**  
  Whale transfers alone do **not** consistently predict whether UNI price goes up or down afterward.  

- **Volatility Signal:**  
  Spikes in whale transfers often **coincide with short-term jumps in volatility**, i.e., more erratic price swings (both directions).  

- **Interpretation:**  
  Think of whale transfers as **shockwaves**: they don’t tell you which way the ship will move, but they tell you the waters won’t stay calm.  

---

## So What?

For analysts and traders:  
- **Don’t treat whale moves as buy/sell signals.**  
- Instead, **treat them as risk alerts**: brace for turbulence, hedge exposure, or scale risk accordingly.  
- The real edge lies not in predicting price direction, but in anticipating **when markets may stop behaving “normally.”**  

---

## Future Improvements

- Analyze at **hourly granularity** instead of daily to capture faster reactions.  
- Expand analysis across multiple tokens (cross-token whale impact).  
- Add **machine learning** models to test predictive power on volatility regimes.  
- Build **real-time monitoring + alerting system** for whale spikes.  

---

## 📂 Repository Structure

```

├── data/              # Raw and processed datasets
├── notebooks/         # Jupyter notebooks with analysis
├── charts/            # Visualizations (PNG outputs)
├── src/               # Supporting Python scripts
└── README.md          # Project documentation

````

---

## Quick Preview

Example chart from the project:  

![Whale Transfers vs UNI Price](./charts/output.png)  

---

## ⚙️ How to Run

1. **Clone this repository**
   ```bash
   git clone https://github.com/your-username/whale-uni-analysis.git
   cd whale-uni-analysis
````

2. **Set up a virtual environment & install dependencies**

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # on macOS/Linux
   .venv\Scripts\activate      # on Windows

   pip install -r requirements.txt
   ```

3. **Run the notebooks**
   Open JupyterLab or Jupyter Notebook and run the files in `/notebooks/`.

   ```bash
   jupyter lab
   ```

4. **Reproduce the charts**
   Executing the notebooks will generate updated visualizations in the `/charts/` folder.

---

## 📝 License

MIT License. Free to use, modify, and share.

```
```

