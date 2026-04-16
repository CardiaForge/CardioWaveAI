# CardioWaveAI

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19476940.svg)](https://doi.org/10.5281/zenodo.19476940)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

A cloud-based cardiac monitoring platform that transforms raw heart rhythm data from wearable devices and medical-grade ECG systems into clinically actionable insights using wavelet-based signal analysis.

## Overview

CardioWaveAI applies multi-scale wavelet decomposition to RR interval time series extracted from ECG recordings, enabling Heart Rate Variability (HRV) analysis that goes beyond basic arrhythmia detection. The platform supports comparison across patients and time frames to identify clinically relevant cardiac patterns.

### Wavelet Transforms

| Transform | Description |
|---|---|
| **DWT** | Discrete Wavelet Transform — multi-resolution decomposition |
| **CWT** | Continuous Wavelet Transform — time-frequency analysis |
| **WPT** | Wavelet Packet Transform — full tree decomposition |
| **SWT** | Stationary Wavelet Transform — shift-invariant analysis |
| **WST** | Wavelet Scattering Transform — deformation-stable features |

### HRV Feature Extraction

- **Frequency bands:** VLF, LF, HF power spectral analysis
- **Nonlinear measures:** Sample entropy, Detrended Fluctuation Analysis (DFA)
- **Statistical features:** Energy, entropy, statistical moments per wavelet sub-band
- **Time-frequency features:** Scale-dependent energy distributions

### Data Sources

- Consumer wearable devices (RR interval exports)
- Medical-grade Holter monitors
- Clinical ECG systems (PhysioNet WFDB format supported)

## Architecture

CardioWaveAI is a polyglot microservices platform built with .NET 10 and Python 3.11, communicating over gRPC. See individual service repositories under the [CardiaForge](https://github.com/CardiaForge) organization.

## Validated Against

- PhysioNet MIT-BIH Arrhythmia Database
- PhysioNet MIT-BIH Normal Sinus Rhythm Database

## Citation

If you use CardioWaveAI in your research, please cite:

```bibtex
@software{popov_cardiowaveai_2026,
  author       = {Popov, Oleksandr},
  orcid        = {0009-0007-4864-5130},
  title        = {{CardioWaveAI: Wavelet-Based Cardiac Signal Analysis Platform}},
  year         = {2026},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.19476940},
  url          = {https://doi.org/10.5281/zenodo.19476940},
  license      = {Apache-2.0}
}
```

## License

This project is licensed under the Apache License 2.0 — see the [LICENSE](LICENSE) file for details.
