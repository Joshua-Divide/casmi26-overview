# Enveda CASMI 2026 - Molecule ID From Mass Spectra

Comprehensive competition overview, background reference, and evaluation documentation for the Kaggle **Enveda CASMI 2026 - Molecule ID From Mass Spectra** challenge.

Official Kaggle Competition: [enveda-CASMI26-molecule-id-mass-spectra](https://www.kaggle.com/competitions/enveda-CASMI26-molecule-id-mass-spectra/overview)

---

## Executive Summary

| Attribute | Specification |
|---|---|
| **Challenge** | Critical Assessment of Small Molecule Identification (CASMI) 2026 |
| **Task** | Predict 2D chemical structures (`SMILES`) from LC-MS/MS tandem mass spectra |
| **Evaluation Metric** | **MRR@25** (Mean Reciprocal Rank @ 25) evaluated on **Connectivity** (First 14 characters of InChIKey / `InChIKey14`) |
| **Stereoisomer Policy** | Stereochemistry is ignored during scoring; all stereoisomers collapse to the same InChIKey14 |
| **Submission Format** | CSV with `molecule_id` and up to 25 semicolon-separated `smiles` candidates (ranked best first) |
| **Compute Constraint** | Kaggle Notebooks only; $\le$ 9 hours runtime (CPU/GPU); internet disabled during scoring |

---

## Repository Contents

- **[`Enveda_CASMI26_Molecule_ID_Overview.pdf`](Enveda_CASMI26_Molecule_ID_Overview.pdf)**: Complete 3-page publication-grade PDF containing the full overview, MS/MS principles, scoring rules, candidate formatting, and code submission requirements.
- **[`Enveda_CASMI26_Overview.html`](Enveda_CASMI26_Overview.html)**: Self-contained standalone HTML report formatted with exact A4 print styles and embedded base64 figures.
- **`figure1_spectrum.png`**: Illustration of tandem mass spectrometry (precursor ion selection, collision-induced dissociation, and fragment ion spectrum).
- **`kerneler.png`**: Official competition artwork badge.

---

## Document Outline

1. **Description**: Predicting natural product small molecule structures directly from biological extract tandem mass spectra (novel and known compounds).
2. **Background — Principles of Mass Spectrometry**:
   - Ionization modes (positive vs. negative) and adduct formations ($[\text{M}+\text{H}]^+$, $[\text{M}+\text{NH}_4]^+$, $[\text{M}-\text{H}]^-$).
   - Precursor ion selection and Collision-Induced Dissociation (CID).
   - Precursor mass vs. fragment peak interpretation.
3. **Evaluation**:
   - Mean Reciprocal Rank top-25 ($\text{MRR@25}$).
   - InChIKey14 connectivity matching (why stereocenters and cis/trans isomers are scored identically).
   - Exact submission CSV format and strict validation criteria.
4. **Code Requirements**:
   - Submission via committed Kaggle Notebooks.
   - Resource limits (CPU/GPU $\le$ 9 hours).
   - External data & pre-trained models permissions.
5. **Acknowledgements**: CASMI founding history (Emma Schymanski & Steffen Neumann, 2012–2022).
