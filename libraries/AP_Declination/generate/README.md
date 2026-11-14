# Declination Table Generator

This script generates the geomagnetic lookup tables using the **IGRF-14** model through the [`ppigrf`](https://pypi.org/project/ppigrf/) Python package.

## Requirements

Python 3 and `ppigrf` version **2.1.0** are required.

Install the dependency with:

```bash
python3 -m pip install ppigrf==2.1.0
```

Alternatively, when using a virtual environment managed by `uv`:

```bash
uv pip install ppigrf==2.1.0
```

Package reference: [ppigrf on PyPI](https://pypi.org/project/ppigrf/)

## Generate the Tables

From the `libraries/AP_Declination` directory, run:

```bash
python3 generate/generate.py
```

This regenerates the `tables.cpp` file containing the magnetic declination, inclination, and intensity lookup tables.

The generator uses a default sampling resolution of 10 degrees and preserves the existing table structure and bilinear interpolation method.