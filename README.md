# CIRCLE EDSS REDCap Instrument

A REDCap instrument that automates the Clinical Instrument to Retrospectively Capture Levels of EDSS (CIRCLE) algorithm for standardized, retrospective scoring of the Expanded Disability Status Scale (EDSS) in multiple sclerosis.

## Overview

The EDSS is the gold standard for evaluating disability in patients with multiple sclerosis. However, manual EDSS scoring is time-consuming, requires significant expertise, and is prone to inter-rater variability. This REDCap instrument implements the CIRCLE algorithm with branching logic, ambulation constraints, and automated calculation of Functional System (FS) subscores and the final EDSS score.

Key features:

- **Branching logic**: Starts with the most severe disability in each functional system, skipping unnecessary questions to reduce completion time
- **Automated scoring**: FS subscores and final EDSS are calculated automatically based on CIRCLE rules
- **Ambulation constraints**: Wheelchair/bed-bound status triggers immediate EDSS calculation
- **Adjusted scores**: Bowel/bladder and visual system scores are adjusted per CIRCLE guidelines
- **Skip logic**: If no disability is present in a functional system, the scorer can skip directly to the next

## Installation

1. Download `CIRCLEEDSS_DataDictionary.csv`
2. In REDCap, navigate to **Project Setup** > **Data Dictionary** (or **Online Designer** > **Upload**)
3. Upload the CSV file as a new instrument or add it to an existing project

## Files

| File | Description |
|------|-------------|
| `CIRCLEEDSS_DataDictionary.csv` | REDCap data dictionary for the CIRCLE EDSS scoring instrument (170 variables) |
| `CIRCLEEDSSSurvey_DataDictionary.csv` | REDCap data dictionary for the accompanying user feedback survey |

## Functional Systems Covered

- Pyramidal
- Cerebellar
- Brainstem
- Sensory
- Bowel and Bladder
- Visual
- Cerebral
- Ambulation

## Citation

If you use this instrument in your research, please cite:

> Murillo F, Bilodeau PA, et al. Implementation of a Clinical Instrument to Retrospectively Capture Levels of EDSS (CIRCLE) REDCap Instrument to Automate Neurologic Disability Documentation in Multiple Sclerosis. *[Manuscript in preparation]*.

The CIRCLE algorithm was originally described in:

> Ciotti JR, Sanders N, Salter A, Berger JR, Cross AH, Chahin S. Clinical instrument to retrospectively capture levels of EDSS. *Multiple Sclerosis and Related Disorders*. 2020;39:101887.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
