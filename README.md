# CIRCLE EDSS REDCap Instrument

A REDCap instrument implementing the CIRCLE (Clinical Instrument to Retrospectively Capture Levels of EDSS) algorithm for retrospective EDSS scoring in multiple sclerosis research. Functional system subscores and the final EDSS are calculated automatically via REDCap calculated fields.

## Import into REDCap

### Add to an existing project (recommended)

1. Download [`CIRCLEEDSS_instrument.zip`](CIRCLEEDSS_instrument.zip)
2. In REDCap, open your project and go to **Online Designer**
3. Click **Upload instrument ZIP** (bottom of the instrument list)
4. Select `CIRCLEEDSS_instrument.zip`
5. The CIRCLE EDSS instrument will be added to your project alongside existing instruments

### Create a new standalone project

1. Download [`CIRCLEEDSS_DataDictionary.csv`](CIRCLEEDSS_DataDictionary.csv)
2. In REDCap, create a new project and go to **Project Setup**
3. Under **Data Dictionary**, click **Upload** and select the CSV file
4. This replaces the entire project data dictionary — use only for a fresh project

## Instrument design

Each functional system begins with a screening question asking whether any disability is present. A negative response advances the scorer directly to the next system, with a score of 0 assigned automatically. When disability is present, options are presented from highest to lowest severity, allowing early selection once the appropriate severity level is reached.

The instrument covers all eight CIRCLE functional systems:

| Functional System | Notes |
|---|---|
| Pyramidal | |
| Cerebellar | |
| Brainstem | |
| Sensory | |
| Bowel and Bladder | Score adjusted per CIRCLE guidelines |
| Visual | Acuity range extended below 20/200 (hand motion, finger counting, light perception, no light perception) |
| Cerebral | Fatigue collected but excluded from subscore to preserve original CIRCLE schema |
| Ambulation | EDSS floor of 2 for any gait difficulty; wheelchair/bed-bound status triggers immediate final score assignment |

Functional system subscores and the final EDSS are calculated automatically. Automated scoring was validated against 1,000 simulated functional system profiles before deployment; REDCap outputs achieved 100% concordance with the CIRCLE scoring rubric.

## Files

| File | Description |
|---|---|
| `CIRCLEEDSS_instrument.zip` | REDCap instrument ZIP — add to an existing project via Online Designer |
| `CIRCLEEDSS_DataDictionary.csv` | Full REDCap data dictionary — use to create a new standalone project |
| `CIRCLEEDSSSurvey_DataDictionary.csv` | Data dictionary for the accompanying usability survey |

## Citation

If you use this instrument, please cite the original CIRCLE algorithm:

> Ciotti JR, Sanders N, Salter A, Berger JR, Cross AH, Chahin S. Clinical instrument to retrospectively capture levels of EDSS. *Multiple Sclerosis and Related Disorders*. 2020;39:101887. doi:10.1016/j.msard.2019.101887

A citation for this REDCap implementation will be added upon publication.

Download [`CITATIONS.bib`](CITATIONS.bib) to import the reference into Zotero, Mendeley, or EndNote.

## License

MIT License. See [LICENSE](LICENSE) for details.
