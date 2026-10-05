# Data availability and expected structure

The raw DJI M3M imagery is not included in this repository because of its size and ownership/transfer restrictions. Use only data that you are authorized to access.

The notebook expects the directory referenced by `LAND_DEGRADATION_DATA_DIR` to have this structure:

```text
research-workspace/
├── DJI_202605021610_001_Create-Area-Route2/  # Optional original acquisition directory
├── OUTPUT/
│   ├── Scene_0001/
│   │   ├── *_D.JPG
│   │   ├── *_MS_G.TIF
│   │   ├── *_MS_R.TIF
│   │   ├── *_MS_RE.TIF
│   │   └── *_MS_NIR.TIF
│   ├── Scene_0002/
│   └── ...
├── ANALYSIS_RESULTS/  # Generated vegetation/soil index arrays and figures
├── masks/             # Generated pseudo-label masks
├── dataset/           # Generated train/validation/test tiles
├── models/            # Generated U-Net and XGBoost models
└── reports/           # Generated evaluation tables and figures
```

The verified archive used in the study contains 437 scene directories. Each scene has one RGB JPEG and four single-band, unsigned 16-bit GeoTIFF files: green, red, red edge, and near infrared.

Do not commit raw imagery, generated tiles, model checkpoints, or personally identifying metadata unless publication rights have been confirmed.

