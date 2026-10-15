# Li/Li<sub>6</sub>PS<sub>5</sub>Cl interface

Data for T. Yuan, Z. Chen and J. A. Dawson, *Reversible Ion Transport Through an Irreversibly Percolating Li<sub>2</sub>S Interphase at the Li/Li<sub>6</sub>PS<sub>5</sub>Cl Interface*, ChemRxiv (2026), [10.26434/chemrxiv.15010110/v1](https://doi.org/10.26434/chemrxiv.15010110/v1).

## Contents

```
Li-LPSCL-Interface/
├── README.md
├── source/
│   └── train-local-huber-05-23-2025.pth.tar   fine-tuned CHGNet model
└── example/
    └── Argy010-Li100/
        ├── ready.g96                          initial interface structure (GROMOS-96 format)
        ├── lmp.data                           same structure as a LAMMPS data file
        └── in.lammps_chgnet                   LAMMPS input for the field-free simulation
```
## Usage

Requires LAMMPS built with the CHGNet interface (`pair_style gnnp`). Set the `pair_style` path in the input to your build, then:

```bash
cd example/Argy010-Li100
echo 12345 > rng.xvg
lmp -in in.lammps_chgnet
```

Other data are available from the corresponding author on reasonable request.

## Contact
Tianmu Yuan (tianmu.yuan@newcastle.ac.uk)
James A. Dawson (james.dawson@newcastle.ac.uk)
