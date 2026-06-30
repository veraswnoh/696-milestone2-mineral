# Québec Mineral Prospectivity Prediction

This repository contains the source code for our supervised learning, unsupervised learning, and data-preprocessing workflows for predicting anomalous concentrations of gold, silver, copper, cobalt, and nickel across Québec.

Because the complete raw and processed datasets are too large to include in the source-code submission, they are provided through Google Drive.

## Repository Structure

```text
project/
├── src/
│   ├── data_preprocessing/
│   ├── supervised/
│   └── unsupervised/
└── README.md
```

The original Google Drive workspace used the following structure:

```text
project/
├── src/
│   ├── data_preprocessing/
│   ├── supervised/
│   └── unsupervised/
├── data/
│   ├── raw/
│   └── processed/
└── report/
```

## Source-Code Folders

### `src/data_preprocessing`

Contains the scripts used to clean, transform, spatially join, and prepare the geochemical, geological, structural, and geophysical datasets for modelling.

### `src/supervised`

Contains the supervised-learning workflows, including the tabular baseline models and the multi-modal model combining tabular geological features with airborne-magnetic imagery.

### `src/unsupervised`

Contains the unsupervised-learning workflows used to identify geological phenotypes and evaluate whether phenotype membership improves anomaly prediction.

## Data Access

### Raw Geological Shapefiles

The geological and structural shapefiles can be accessed here:

https://drive.google.com/drive/folders/1Lya883OBvWRoMm6pGUXfln6diztZntyN?usp=drive_link

### Raw Geochemical Data

The raw tabular geochemical data can be accessed here:

https://drive.google.com/drive/folders/1JP07EHNgXTHKpJH9Rb5iF5Dr_rl0UA0C?usp=drive_link

### Raw Airborne-Magnetic Raster

The original GeoTIFF file used to generate the magnetic image tiles can be accessed here:

https://drive.google.com/file/d/1uHPvSyWHnhoL8XyJUtRGH-6fpy0bsimp/view?usp=drive_link

### Complete Data Directory

For reproducibility and convenience, the complete data directory—including both raw and processed data—is available here:

https://drive.google.com/drive/folders/1To1cYULGT8uPx_4v0iHTDXnsvJOGxtR3?usp=drive_link

The processed data are included for convenience but can also be regenerated using the scripts in `src/data_preprocessing`.

## Report

The accompanying project report provides the full methodology, experimental design, model results, interpretation, and discussion for the supervised and unsupervised components of the project.

## Reproducing the Project

To reproduce the original workspace:

1. Download the complete data directory from the link above.
2. Place the downloaded `data` folder beside the `src` folder.
3. Run the preprocessing scripts before running the supervised or unsupervised modelling workflows.

The expected structure is:

```text
project/
├── src/
│   ├── data_preprocessing/
│   ├── supervised/
│   └── unsupervised/
└── data/
    ├── raw/
    └── processed/
```

Some scripts may require file paths to be updated depending on where the project is stored locally.
