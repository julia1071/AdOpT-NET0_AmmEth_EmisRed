[![Documentation Status](https://readthedocs.org/projects/adopt-net0/badge/?version=latest)](https://adopt-net0.readthedocs.io/en/latest/?badge=latest)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
![Testing](https://github.com/UU-ER/AdOpT-NET0/actions/workflows/00publish_tests.yml/badge.svg?branch=main)
[![PyPI version](https://badge.fury.io/py/adopt-net0.svg)](https://pypi.org/project/adopt-net0/)

# AdOpT-NET0: Ammonia–Ethylene Emission Reduction

This repository contains the code, data, and results used in the paper:

**Tiggeloven, J. L.**, Faaij, A. P. C., Kramer, G. J., & Gazzani, M. (2025).  
*Optimizing Emissions Reduction in Ammonia–Ethylene Chemical Clusters: Synergistic Integration of Electrification, Carbon Capture, and Hydrogen.*  
Industrial & Engineering Chemistry Research, 64, 4479–4497. DOI:[10.1021/ACS.IECR.4C03817](https://doi.org/10.1021/ACS.IECR.4C03817)

This repository is **based on the original AdOpT-NET0 tool**, but includes adaptations specific to this work. It contains all input datasets, case studies, and raw results required to reproduce the analyses in the paper. Users can regenerate the results by running the corresponding scripts, e.g., `run_{case_study}.py`.

## Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/julia1071/AdOpT-NET0_AmmEth_EmisRed.git
cd AdOpT-NET0_AmmEth_EmisRed
pip install -r requirements.txt
```

Additionally, you need a [solver installed, that is supported by pyomo](https://pyomo.readthedocs.io/en/stable/solving_pyomo_models.html#supported-solvers)
(we recommend gurobi, which has a free academic licence).

Note for mac users: The export of the optimization results require a working
[hdf5 library](https://www.hdfgroup.org/solutions/hdf5/). On windows this should be
installed by default. On mac, you can install it with homebrew:

```brew install hdf5```

## Usage and documentation
The documentation and minimal examples of how to use the package can be found 
[here](https://adopt-net0.readthedocs.io/en/latest/index.html). We also provide a 
[visualization tool](https://resultvisualization.streamlit.app/) that is compatible 
with AdOpT-NET0.

## Dependencies
The package relies heavily on other python packages. Among others this package uses:

- [pyomo](https://github.com/Pyomo/pyomo) for compiling and constructing the model
- [pvlib](https://github.com/pvlib/pvlib-python) for converting climate data into 
  electricity output
- [tsam](https://github.com/FZJ-IEK3-VSA/tsam) for the aggregation of time series

## Credits
This tool was developed at Utrecht University.
