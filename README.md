# Supporting Information

**Theoretical Computational Study on the Electronic Structure of Ni(III) Dithiolene Complexes**

*Electronic Structure • Multi-Reference Character • Spin Polarization*

---

## Computational Details

### Methods & Protocols

| Category | Method | Basis Set | Software |
|----------|---------|------------|----------|
| **Geometry Optimization** | UDFT/TPSSh | Ni: LANL2DZ<br>C,N,S: def2-TZVP | PySCF |
| **Single-Point Analysis** | UDFT/TPSSh | As above | PySCF |
| **Multi-Reference** | CASSCF(11e,11o)<br>+ NEWPT2 | As above | PySCF |
| **Topological Analysis** | AIM/ELF | As above | Multiwfn |
| **Population Analysis** | Mulliken/Hirshfeld | As above | PySCF + Multiwfn |

###  Active Space Selection

The CASSCF calculations employed an **(11e, 11o)** active space comprising:

- **5 orbitals**: Ni 3d orbitals
- **6 orbitals**: ligand π/π* orbitals from dithiolene backbone
- **Covered excitations**: d-d, π-π*, metal-ligand charge transfer

**Rationale**: This space captures both static correlation and dynamic charge fluctuations essential for describing the non-innocent ligand behavior.

---

## Key Computational Findings

###  Spin Density Distribution

| Center | Spin Population | Orbital Character |
|--------|-----------------|-------------------|
| Ni | 0.305 | Predominantly $d_{x^2-y^2}$ |
| S (per atom) | ~0.144 | Primarily 3p orbitals |
| Total (4S) | 0.597 | Ligand-centered |

**Mechanism**: Spin polarization induces negative s-orbital spin density ($\rho_s^{\text{ind}} \approx -0.01$) at sulfur nuclei, explaining large $^{33}$S hyperfine coupling.

###  Multi-Reference Diagnostics

| Metric | Value | Interpretation |
|--------|-------|----------------|
| $D_{MR}$ | 4.09 | Strong multi-reference character |
| $C_{\text{max}}^2$ | 0.470 | Single configuration insufficient |
| Configurations (90%) | 108 | Complex wavefunction required |
| $\langle S^2 \rangle$ | 0.750 | Pure $S = 1/2$ ground state |

### Bonding Analysis

**AIM Results (Ni–S BCP)**:
- $\rho(r) = 0.2569$ a.u.
- $\nabla^2\rho(r) = +0.6963$ a.u.  
- $H(r) = -0.3074$ a.u.
- **Conclusion**: Covalent bonding character

**ELF/Delocalization**:
- $DI(\text{Ni–S}) \approx 0.74$
- Moderate ELF values (0.3–0.6)
- **Conclusion**: Delocalized covalent interaction

