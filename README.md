# EQUIL3 Python: Modernized Urine Ion Supersaturation Calculator

This repository provides a modern Python implementation of the original EQUIL2 program, historically written in BASIC. EQUIL2 was one of the first software tools used for calculating the relative supersaturation (RSS) of urine ions, aiding in the understanding of urinary stone formation.

## 📖 Background
Relative supersaturation (RSS) values are essential for evaluating the risk of urinary stone formation. While older RSS calculation programs were compiled and lacked transparency regarding their coefficients, this Python version provides an open-source, adaptable alternative.

This work is based on:
> **Anthony, R. M., Davidson, S., MacLeay, J. M., Brejda, J., Werness, P., & Jewell, D. E. (2023).**  
> *Comparison of two software programs used to determine the relative supersaturation of urine ions.*  
> [Frontiers in Veterinary Science, 10, 1146945](https://doi.org/10.3389/fvets.2023.1146945)

## 🚀 Features
- **Modern Python implementation** of the original BASIC-based EQUIL2 model.
- **Open-source and modifiable**, allowing researchers to inspect and update parameters.
- **Supports iterative equilibrium calculations** for key urine ion species.
- **Designed for veterinary applications**, but adaptable for broader chemical equilibrium analysis.

## 🔧 Installation
To use this program, clone the repository and ensure you have Python 3.x installed. Required dependencies include `numpy`:
```sh
git clone https://github.com/yourusername/equil3-python.git
cd equil3-python
pip install -r requirements.txt
```
## 🛠️ Usage
You can run equilibrium calculations by providing input parameters in a dictionary format:

```python
from equil2 import equilibrium_calculations

A = {
    'pH': 7.4,
    'Na': 140,
    'K': 4.5,
    'Ca': 2.5,
    'Mg': 1.2,
    'Cl': 100,
    'CO2': 0.02,
    'NH4': 0.001,
    'P': 0.002,
    'S': 0.001,
}

results = equilibrium_calculations(A)

for species, conc in results.items():
    print(f"{species}: {conc:.6f} M")
```
📌 License
This project is released under the Creative Commons Attribution License (CC BY).

📬 Contact
For questions or contributions, please open an issue or submit a pull request
