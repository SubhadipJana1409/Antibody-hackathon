# Rational Antibody Design for PD-1 Checkpoint Inhibition

**Author:** Subhadip Jana  
**Event:** Antibody Hackathon 2025

This repository contains the submissions for the **Antibody Hackathon**, focusing on the computational design of antibodies targeting the **PD-1 checkpoint inhibitor** for cancer immunotherapy.

## Repository Structure

-   **Challenge1/**: "Remix Keytruda" - Redesigning CDRs of the parental drug while maintaining binding.
-   **Challenge2/**: "De Novo Design" - Designing novel binders with low germline identity.
-   **pitch/**: Presentation materials and outline summarizing the approach and key findings.

## Project Overview

Our approach utilized a **rational design strategy** focusing on conservative mutations to the CDR-H3 loop of the Keytruda antibody. By performing a single strategic mutation (Tyrosine to Phenylalanine, **Y→F**) at position 5 of the CDR-H3 loop, we successfully generated a candidate that satisfies the requirements for both challenges simultaneously.

### Key Strategy
-   **Original CDR-H3**: `CARRDYRFDMGFDYWGQG`
-   **Designed CDR-H3**: `CARRDFRYDMGFDYWGQG`
-   **Mutation**: Y5F (Maintains aromatic stacking while introducing novelty).

---

## Challenge 1: Remix Keytruda (Results)
*Goal: Redesign Keytruda CDRs to differ from the parent drug while maintaining binding affinity.*

**Status: ALL METRICS PASSED ✓**

| Metric Category | Metric | Value | Threshold | Result |
| :--- | :--- | :--- | :--- | :--- |
| **Binding** | **ipSAE** | **0.73** | ≥ 0.60 | **PASS** (High Confidence) |
| **Structure** | **DockQ** | **0.80** | ≥ 0.23 | **PASS** (Medium-High Quality) |
| **Developability** | **NetSolP** | **0.54** | ≥ 0.50 | **PASS** (Soluble) |
| **Novelty** | **Seq Identity** | **88.9%** | < 95% | **PASS** (11.1% Novel) |

---

## Challenge 2: De Novo Design (Results)
*Goal: Design an antibody with low identity to human germline sequences.*

**Status: ALL METRICS PASSED ✓**

| Metric Category | Metric | Value | Threshold | Result |
| :--- | :--- | :--- | :--- | :--- |
| **Binding** | **ipSAE** | **0.73** | ≥ 0.60 | **PASS** (High Confidence) |
| **Affinity** | **ΔG (PRODIGY)** | **-11.8 kcal/mol** | ≤ -6.0 | **PASS** (Strong Binding) |
| **Developability** | **NetSolP** | **0.54** | ≥ 0.50 | **PASS** (Soluble) |
| **Novelty** | **Germline ID** | **77.4%** | < 95% | **PASS** (22.6% vs Germline) |

---

## Directory Contents

### `Challenge1/` & `Challenge2/`
-   **`metrics/`**: Detailed summary files of the validation metrics.
-   **`sequences/`**: FASTA files containing the designed sequences.
-   **`structures/`**: 
    -   `*_complex.pdb`: Predicted complex structure (Antibody + Antigen).
    -   `*_pae.json`: Predicted Aligned Error (PAE) files from AlphaFold.

### `pitch/`
-   **`Subhadip_Jana_presentation.pptx`**: The hackathon pitch deck.
-   **`presentation_outline.txt`**: Text outline of the presentation content.
