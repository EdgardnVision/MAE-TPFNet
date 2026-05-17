
# MAE-TPFNet

Official repository for the manuscript:

MAE-TPFNet is a clip-level video recognition framework for pole-state recognition in distribution network construction surveillance videos. The task is formulated as a three-class risk-state recognition problem, including **Normal**, **Tilt**, and **Falling**, corresponding to safe, warning, and alarm states in distribution network construction scenarios.

## Overview

Surveillance videos during distribution network construction are often affected by persistent occlusion, strong linear background interference, camera shake, motion blur, and frame loss. These factors weaken pole-posture cues and increase the confusion among Normal, Tilt, and Falling states.



## Task Definition

The DG dataset is organized as a clip-level three-class recognition task. Each sample is a 10-second video clip.

| Class | Engineering response level | Description |
|---|---|---|
| Normal | Safe | The pole remains upright or nearly upright, and no obvious risk evolution is observed. |
| Tilt | Warning | The pole shows visible inclination but remains relatively stable without rapid instability or continuous falling. |
| Falling | Alarm | The pole undergoes continuous falling evolution, irreversible instability, near-collapse, or has already collapsed. |

The labels are determined according to visual posture, temporal evolution, and engineering risk level within the complete 10-second temporal window, rather than a single-frame angle threshold.

## Code Availability

This repository has been created to support the reproducibility of the manuscript.

Since the manuscript is currently under review, the full implementation has not been publicly released at this stage. Upon acceptance or publication, we will release:

- the implementation of MAE-TPFNet;
- the customized modules, including STPA, ST-CSA, and GAF-Head;
- training and testing configuration files;
- preprocessing scripts;
- evaluation scripts;
- documentation for reproducing the reported experiments.

The repository will be continuously updated.

## Dataset Availability

The DG dataset used in this study contains construction-site surveillance videos related to distribution network operations. Due to privacy, safety-management, and data-authorization restrictions, the raw monitoring videos cannot be directly released publicly.

To improve transparency and reproducibility, we will provide:

- the annotation file format;
- the preprocessing procedure;
- the train/validation/test split protocol;
- the video-level evaluation protocol;
- example directory structures and sample metadata when permitted.

Researchers interested in the dataset may contact the corresponding author for further information, subject to data-use restrictions.

## Planned Repository Structure

```text
MAE-TPFNet/
├── configs/              # Training and testing configuration files
├── datasets/             # Dataset loading and preprocessing scripts
├── models/               # MAE-TPFNet model implementation
│   ├── stpa/             
│   ├── st_csa/           
│   └── gaf_head/         # 
├── tools/                # Training, testing, and evaluation scripts
├── docs/                 # Documentation and reproducibility notes
├── README.md
└── LICENSE
