# ReaGeo

Open-source dataset for ReaGeo paper

## Dataset

This repository contains the Singapore geocoding dataset used in the ReaGeo paper.

### Data Files

- `singapore_train.json` - Training set (60,000 samples)
- `singapore_test.json` - Test set (6,669 samples)

### Data Format

Each sample contains the following fields:

```json
{
  "address": "Original address text",
  "lat": Original latitude,
  "lon": Original longitude,
  "geohash": "Original Geohash code",
  "direction": "Direction (e.g., west, south, etc.)",
  "new_address": "New address with offset description",
  "new_lat": New latitude after offset,
  "new_lon": New longitude after offset,
  "new_geohash": "New Geohash code after offset"
}
```

### Description

The dataset includes both original location information and offset location information with directional descriptions, suitable for geocoding tasks that require spatial reasoning.

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{reageo2026,
  title={ReaGeo: [Paper Title]},
  author={[Authors]},
  journal={[Journal/Conference Name]},
  year={2026}
}
```

Please replace the placeholder information with the actual paper details.
