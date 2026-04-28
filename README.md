# UNIQuE HHL

This repository contains an **emulated implementation of the Harrow-Hassidim-Lloyd quantum algorithm**.
A complete description of the algorithm can be found in the paper associated with this project: [link forthcoming].

## Table of Contents

- [Introduction](#introduction)
- [Structure](#structure)
- [License](#license)

## Introduction

The Unconventional Noiseless Intermediate Quantum Emulator (UNIQuE) is an open-source quantum computing emulator, introduced in [IEEE CASCON 66301, 00086 (2025)](https://ieeexplore.ieee.org/document/11344284).
As an emulator, UNIQuE performs high-level quantum subroutines using optimized classical algorithms.
This is opposed to quantum simulators that perform all operations via matrix multiplications.
This repository extends the UNIQuE framework through the addition of the Harrow-Hassidim-Lloyd quantum algorithm for sampling from the solution space of linear systems.

## Structure

The repository structure is as follows:

```
adiabatic-simons-algorithm/
├── data/                      # Data files for project
│   ├── counts.txt               # Dictionary of measured counts from experiment
│   ├── data.py                  # Visualizes experimental data
│   ├── output.txt               # Cleaned log of experimental data
│   └── rawData.txt              # Raw experimental Data
├── figs/                      # Figure files
│   ├── em1.png                  # Bar chart from emulation of first experiment
│   ├── em2.png                  # Bar chart from emulation of second experiment
│   ├── hhl.pdf                  # HHL circuit diagram overview image
│   ├── hhl.qpic                 # HHL circuit diagram intermediate representation
│   ├── sim1.png                 # Bar chart from simulation of first experiment
│   └── sim2.png                 # Bar chart from simulation of second experiment
├── src/                       # Source code files
│   ├── comparison.py            # Experimentally compare performance of emulator and simulator
│   ├── eigenValueRatio.ipynb    # Visualization of the experimental eigenvalue ratios
│   ├── emulateHHL.ipynb         # Visualization of the emulated HHL algorithm
│   ├── emulator.py              # Source file for the emulated HHL algorithm
│   ├── plotting.py              # Source file to create PNG images in figs directory
│   └── simulator.py             # Source file for the simulated HHL algorithm
├── LICENSE                    # License file
└── README.md                  # Project description and instructions
```

Of these files, those in the source directory are the most important.
In particular, the `emulateHHL()` function in the `src/emulator.py` file executes the emulated HHL algorithm.
Additionally, the `src/plotting.py` file can be used to recreate the images from the saved experimental data, and the `src/comparison.py` file can be used to generate new experimental data.

## License

This project is licensed under the MIT License — see the LICENSE file for details.

