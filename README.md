# Reconstruction of Degraded PPG Signals using UNet-TCN

This repository provides the dataset and model description associated with the paper:

**“Reconstruction and Denoising of Photoplethysmography Signals using Temporal Convolutional UNet”**

## Repository Contents

This repository includes:

- the degraded PPG dataset used in the experiments;
- information about the signal organization and corruption scenarios;
- the proposed UNet-TCN reconstruction framework.

## Dataset Description

The main dataset file is:

`ppg_degraded_dataset.xlsx`

The dataset contains multiple sheets corresponding to different PPG waveform types and degradation settings.

### Signal Categories

The dataset includes several PPG morphologies, such as:

- Normal
- Low Perfusion
- Stiff Arteries
- Strong Reflection
- Weak Reflection

### Data Content

Each sample contains:

- **Clean_PPG** — reference clean signal;
- **Corrupted_PPG** — degraded signal with additive noise and missing segments;
- **Mask** — binary indicator of valid and missing samples.

Depending on the sheet, the corrupted signals may include different:

- noise levels (SNR conditions),
- missing-data ratios,
- missing segment positions.

## Experimental Scenarios

The dataset was designed to evaluate the robustness of reconstruction models under different degradation conditions, including:

- multiple signal morphologies;
- several noise levels;
- different percentages of missing data;
- fixed-gap and multi-gap corruption patterns.


The model is trained to reconstruct clean PPG signals from degraded inputs while preserving signal morphology under noise and missing-data corruption.

