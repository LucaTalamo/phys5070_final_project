# Quantum optimal control of cavity optomechanical systems using Krotov's method

This repository recreates the key results from [Quantum Optimal Control for Mixed State Squeezing in Cavity Optomechanics](https://arxiv.org/pdf/1807.04718.pdf) by Basilewitsch et al. The paper is the first to use Krotov's method, a method from optimal control theory, to optimize control sequences in a cavity optomechanics setting. In particular, the authors design a two-tone optical pulse sequence that speeds up optomechanical squeezing of a mechanical object's motion inside an optical cavity. 

We use the `krotov` package, which is a well-documented OCT package built upon the open system quantum simulation package `qutip`. This repository is divided into two sections.

1. The `test` folder. This contains two scripts with tutorials on using the packages required by the project. 

    I. `test_qutip_examples.ipynb` teaches you how to use the `qutip` package to simulate the dynamics of various quantum systems. We simulate 3 systems, and compare to known analytic results:
    
        i. Rabi oscillations in a two-level system. This provides a gentle introduction to using the package.
        ii. Adiabatic transfer in a two-level system. Here, you learn how to simulate using time-dependant Hamiltonians.
        iii. The Jaynes-Cummings model. You learn how to simulate tensor states.
        
    II. `test_krotov.ipynb` teaches you how to implement Krotov's algorithm using the `krotov` package. It goes over the requisite amount of theory to do this. It also introduces you to `qutip` simulations using the Liouvillian paradigm, which is preferred by the `krotov` package. More specifically, we generalize a pure-state [example](https://qucontrol.github.io/krotov/v1.0.0/notebooks/01_example_simple_state_to_state.html), given by the developers, to open mixed state systems.

2. `mixed_state_optomechanical_squeezing.ipynb` is the main script in the repository. We use the `krotov` package to recreate Basilewitcsch et al.'s key results. We outline the requisite theory in this notebook and reference the `test` folder files where necessary.
