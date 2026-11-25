# SARShip-RPD

**SAR Ship Dataset with Region-wise Physical Descriptions**

SARShip-RPD v1.0 contains 3,731 Gaofen-3 synthetic aperture radar (SAR) ship image–text pairs across seven classes (S1–S7). Each ship chip is paired with a six-sentence English annotation covering the ship class, length, hull aspect ratio, and visually interpreted scattering characteristics of the bow, hull, and stern.

## Download

- File: `SARShip-RPD-v1.0.zip`
- Download: [Baidu Netdisk](https://pan.baidu.com/s/13PGPgwR9DKb8yHhEj9_voA?pwd=619y)
- Extraction code: `619y`

## Archive Contents

| Path | Contents |
| --- | --- |
| `data/S1/` through `data/S7/` | JPEG ship chips and matching English annotations (`*_en.txt`). |
| `splits/` | Six CSV manifests for zero-shot and generalized zero-shot evaluation. |
| `class_semantic_prototypes.json` | Nine class semantic prototypes covering the seven ship classes. |
| `README.md` | Archive documentation and data source information. |

## Evaluation Splits

| Setting | Unseen class combinations |
| --- | --- |
| Two unseen classes | S1/S5, S2/S6, and S5/S7 |
| Three unseen classes | S2/S6/S7, S2/S3/S4, and S1/S2/S5 |

Paths in the CSV manifests are relative to the extracted archive's `data/` directory. Use `seen_train` for training and `seen_val` for validation. Conventional zero-shot learning (ZSL) uses `unseen_test` for testing. Generalized zero-shot learning (GZSL) uses both `seen_test` and `unseen_test` for testing.

## Data Source and Citation

The ship chips were derived from Gaofen-3 SAR imagery described by Sun et al. in [Ship Recognition for Complex SAR Images via Dual-Branch Transformer Fusion Network](https://doi.org/10.1109/LGRS.2024.3398013), *IEEE Geoscience and Remote Sensing Letters*, 2024.

If you use this dataset, please cite **SARShip-RPD v1.0** and its accompanying paper.
