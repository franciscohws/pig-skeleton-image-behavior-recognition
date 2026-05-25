# Pig Behavior Recognition Using Skeleton and Image-Based Temporal Representations

This repository contains the code and documented notebooks used for pig behavior recognition using skeleton-based and image-based temporal representations.

The experiments compare pose/keypoint-based models and RGB video baselines, including YOLOv8n-Pose, DeGCN, KP-TCN, Random Forest, SlowFast, and ViTAM-SlowFast.

## Dataset

The dataset is deposited on Zenodo. The GitHub repository contains only code, notebooks, configuration examples, and documentation.

Zenodo DOI:

`TO_BE_ADDED_AFTER_ZENODO_PUBLICATION`

The Zenodo dataset includes:

- CVAT XML and CSV annotations for the 5,300-frame annotated dataset;
- YOLOv8n-Pose dataset for the 5,300 annotated frames organized into five temporal folds;
- out-of-fold YOLOv8n-Pose prediction outputs;
- skeleton windows for DeGCN and KP-TCN experiments;
- RGB image windows for SlowFast and ViTAM-SlowFast baselines;
- model outputs, metadata, class mapping, keypoint schema, and validation reports.

## Repository structure

```text
github_repository_v1/
├── notebooks/
│   ├── 01_degcn_yolov8npose_pipeline.ipynb
│   ├── 02_slowfast_baseline.ipynb
│   ├── 03_tcn_rf_inference_time_comparison.ipynb
│   └── 04_vitamslowfast_baseline.ipynb
├── configs/
│   └── paths_example.yaml
├── src/
│   ├── data/
│   ├── pose/
│   ├── models/
│   ├── evaluation/
│   └── utils/
├── docs/
├── results/
├── README.md
├── requirements.txt
├── environment.yml
├── .gitignore
└── LICENSE
```

## Notebooks

| Notebook | Purpose |
|---|---|
| `01_degcn_yolov8npose_pipeline.ipynb` | YOLOv8n-Pose and DeGCN pipeline using keypoint-based temporal representations. |
| `02_slowfast_baseline.ipynb` | SlowFast RGB video baseline. |
| `03_tcn_rf_inference_time_comparison.ipynb` | KP-TCN and Random Forest inference-time comparison. |
| `04_vitamslowfast_baseline.ipynb` | ViTAM-SlowFast RGB video baseline. |

## Installation

Create a Conda environment:

```bash
conda env create -f environment.yml
conda activate pig-skeleton-image-behavior
```

Or install dependencies using pip:

```bash
pip install -r requirements.txt
```

## Dataset setup

After downloading the Zenodo dataset, extract the ZIP files and update:

```text
configs/paths_example.yaml
```

Copy it to:

```text
configs/paths.yaml
```

and edit the paths according to your local machine.

## Reproducibility note

The notebooks were documented to preserve the original experimental flow. Some local paths may need to be adapted before execution.

## License

Code license: MIT License.

Dataset license: Creative Commons Attribution 4.0 International (CC BY 4.0), unless otherwise specified in the Zenodo record.
