# ReaGeo

**ReaGeo: Reasoning-Enhanced End-to-End Geocoding with LLMs**

Official dataset for the ReaGeo paper

## About

ReaGeo is an end-to-end geocoding framework based on large language models, designed to overcome the limitations of traditional multi-stage approaches. The method converts geographic coordinates into geohash sequences, reformulating the coordinate prediction task as a text generation problem, and introduces a Chain-of-Thought (CoT) mechanism to enhance the model's reasoning over spatial relationships.

### Key Features

- **End-to-End Framework**: Eliminates workflow complexity and error propagation from traditional retrieval-based methods
- **Chain-of-Thought Reasoning**: Enhances spatial relationship reasoning through intermediate reasoning steps
- **Geohash Sequence Generation**: Converts coordinate prediction into text generation
- **Reinforcement Learning**: Uses distance-deviation-based reward (GRPO) to optimize generation accuracy
- **Versatile Geocoding**: Handles explicit address queries, vague relative location queries, and non-point geometric regions

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

### Dataset Description

The dataset includes both original location information and offset location information with directional descriptions. This design supports the Chain-of-Thought training approach, where the model learns spatial reasoning through relative positional relationships before generating geohash sequences. The dataset is suitable for:

- Single-point geocoding with explicit addresses
- Vague relative location query resolution
- Spatial reasoning and neighborhood knowledge learning
- End-to-end geocoding model training

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{cui2026reageo,
  title={ReaGeo: Reasoning-Enhanced End-to-End Geocoding with LLMs},
  author={Cui, Jian and Ren, Zhiyuan and Weng, Desheng and Zhao, Yongqi and Wenbin, Gong and Lei, Yu and Dong, Zhenning},
  journal={arXiv preprint},
  year={2026}
}
```
