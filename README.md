# Investigating the Viability of Machine Learning Models for Risk Prediction with Datix & Supporting Data

**MSci Research Project | University of Portsmouth | September 2025**  
**Research collaboration:** University of Portsmouth and St Andrew's Healthcare

## Overview

This repository accompanies an MSci research project investigating whether machine learning can use routinely collected clinical information to estimate the probability of a violent or aggressive incident involving a psychiatric inpatient within the following **24 hours**.

The work explores a potential early-warning approach to support, rather than replace, clinical judgement and established risk assessment practices in secure and forensic mental healthcare. The research is retrospective and exploratory: **the models have not been prospectively clinically validated and must not be used for patient care, risk assessment, or decisions about restrictive interventions.**

## Dissertation

The full dissertation provides the research background, literature review, data preparation methodology, model development, evaluation, explainability analyses, clinical discussion, limitations, and conclusions.

**[Read the full dissertation (PDF)](Investigation%20MLM%20and%20Crisis%20Prevention%20UP2302645.docx-2.pdf)**

> If the PDF is renamed before publication, update the link above to match its final repository filename.

## Research objectives

- Investigate the feasibility of predicting short-term violence and aggression from routinely collected inpatient data.
- Evaluate recurrent neural-network architectures capable of learning from longitudinal clinical records.
- Compare model performance using discrimination, classification, and probabilistic evaluation metrics.
- Explore explainable AI techniques to help interpret model behaviour.
- Consider how probabilistic early warnings might fit into clinical workflows, alongside their limitations and governance requirements.

## Data and prediction task

The research uses pseudonymised Datix incident information and supporting patient data supplied for the approved research project. The data sources discussed in the dissertation include demographic and clinical information, recorded incidents, medication histories, and meaningful-activity records.

The modelling objective is to estimate the **probability of a violent or aggressive incident within a 24-hour prediction horizon**, using information available in the patient's preceding history.

The source data are **not included** in this repository. Pseudonymisation was part of the research data-governance arrangements; it does not mean that patient-level records are suitable for unrestricted public redistribution.

## Modelling approach

The dissertation investigates temporal machine-learning approaches, with particular emphasis on **gated recurrent units (GRUs)** and a **GRU architecture incorporating an attention mechanism**. Transformer-based experiments are also discussed.

The research includes:

- Cleaning and restructuring heterogeneous clinical records for longitudinal modelling.
- Recurrent neural-network experiments and model comparison.
- Evaluation using metrics such as AUROC, F1 score, confusion matrices, precision–recall curves, and Brier score.
- Explainability investigations, including SHAP and partial-dependence approaches.
- Consideration of how predictions and explanations could be presented to clinical users.

## Selected reported results

The dissertation reports the following results for the final **GRU with attention** experiment:

| Metric | Reported value |
| --- | ---: |
| AUROC | 0.9586 |
| F1 score | 0.8974 |
| Brier score | 0.0884 |

These are **retrospective experimental results**, as reported in the dissertation, and should not be interpreted as evidence of prospective clinical effectiveness, external generalisability, or readiness for deployment. See the dissertation for the evaluation setup, model comparisons, interpretation, and limitations.

## Repository contents

The repository contains research notebooks and supporting material documenting data preparation, exploratory analysis, model development, evaluation, and explainability. The complete dissertation is supplied as a PDF.

Notebooks are intended as a record of the experimental methodology. **They are not a self-contained, executable reproduction of the original experiments**, because the confidential source data and trained model artefacts are not distributed. Some code may refer to local dataset paths or research-specific dependencies that are unavailable publicly. 

All notebooks and distributed files have been sanitised before sharing.

## Why trained model weights are not included

The final trained models and intermediate checkpoints are deliberately **not published**. Although sharing trained weights is common in machine-learning research, these models were fitted to sensitive, longitudinal psychiatric healthcare records.

Model parameters do not ordinarily contain readable patient records, but releasing them can create additional privacy considerations, including possible membership-inference and other model-based information-disclosure attacks. Omitting weights is a precautionary **data-minimisation and research-governance decision**, not evidence that a specific privacy attack has succeeded against these models.

For the same reasons, this repository does not distribute:

- Original or pseudonymised patient-level datasets.
- Patient-level prediction exports or clinical histories.
- Trained model checkpoints, weights, or optimiser states.
- Credentials or access details for research data sources.

The methodology and aggregate results remain documented in the dissertation and available research code.

## Responsible use and limitations

This project is an **academic feasibility investigation**, not a medical device or operational clinical decision-support system. The reported findings should be interpreted in light of the original dataset, retrospective study design, potential reporting and selection biases, class imbalance, model calibration, and the need for independent and prospective validation.

A model-estimated probability must not be treated as a definitive statement about an individual patient's behaviour. In particular, predictions must not be used to justify seclusion, restraint, enhanced observation, or other restrictive practices.

Any future clinical application would require appropriate institutional approvals, privacy and fairness assessments, clinical safety evaluation, external validation, and ongoing monitoring.

## Acknowledgements

This project was conducted as part of the University of Portsmouth research programme in collaboration with St Andrew's Healthcare. Further acknowledgements and references appear in the dissertation.

## Citation

If referencing this work, please cite the dissertation:

Aldridge, C. (2025). *Investigating the Viability of Machine Learning Models for Risk Prediction with Datix & Supporting Data*. MSci Research Project, University of Portsmouth.

## Licence and permissions

No open-source licence is asserted here for confidential research data, trained model artefacts, institutional material, or third-party content. Reuse of repository code is subject to the licence, if any, separately added to the repository. Publication of the dissertation and derived research outputs remains subject to applicable institutional and research-data agreements.
