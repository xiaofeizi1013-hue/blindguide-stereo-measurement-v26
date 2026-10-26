# BlindGuide v26 stereo measurement reproducibility

Numerical and image-cache reproduction materials for **Calibration and Tail Errors in Stereo Range Measurement** by Yifei Cheng, Yilin Zeng and Jiantong Sun.

This repository provides the frozen v26 numerical records, calibrated geometry, ROI masks, target-only image caches, implementation identity and reproducible figure sources. It supports eleven numerical table CSVs and ten manuscript/supplement figure PNGs. The full manuscript and original human photographs are not part of this public release.

## Download and run

Download `BlindGuide_v26_Public_Reproducibility_20261026.zip`, extract it, and open its `BlindGuide_v26_Public_Reproducibility` directory. Use Python 3.13 with the versions in `requirements-numerical.txt`.

```sh
python -m pip install -r requirements-numerical.txt
python reproduce.py --check --tables --figures --out reproduced
```

The portable entry point uses supplied CSVs and caches. It does not require CUDA, OpenCV or the original camera images. `REPRODUCIBILITY.md` maps each output to its inputs and scripts; `DATA_DICTIONARY.md` describes the fields.

The record set includes severe accepted errors, invalid metric conversions and contaminated calibration anchors. Full-image matching requires the retained original images and the documented Windows CUDA environment; it is separate from the portable numerical and cached-figure checks.

## Interpretation

Results use nominal board-distance labels. Frames at one distance are correlated. C0-to-C1 contributes one operator-documented physical transfer. The package does not establish population reset stability, texture causality or a traceable absolute-distance standard.

## Source and third-party software

The original numerical and plotting scripts and scientific inputs retain their frozen source bytes. The Windows libSGM wrapper and third-party Apache 2.0 license are supplied under `reproducibility/software/`; the portable checks do not execute that DLL. No new top-level license is assigned by this packaging operation.

Corresponding author: Yifei Cheng, xiaofeizi1013@gmail.com.

Repository: https://github.com/xiaofeizi1013-hue/blindguide-stereo-measurement-v26
