# PMLB — Pocket Machine Learning Benchmarking Application

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white"/>
  <img src="https://img.shields.io/badge/Runtime-TFLite%20%7C%20ONNX-FF6F00?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge"/>
</p>

**PMLB** is a free, open Android application for benchmarking TensorFlow Lite and ONNX models directly on-device. It measures inference latency, energy consumption, and memory usage, enabling reproducible comparisons of machine learning models across different Android hardware.

---

## Download

| Version | File | Notes |
|---------|------|-------|
| v1.0.0 | [PMLB-v1.0.0.apk](../../releases/latest) | Android 8.0+ (API 26+) |

> **Install tip:** Enable *Install from unknown sources* in Android Settings → Security before installing.

---

## Features

- **Simple Mode** — one-tap benchmark with sensible defaults (5 warm-up, 20 measured runs, trimmed mean)
- **Advanced Mode** — full control over warm-up runs, measured runs, trim %, threads, XNNPACK, backend (CPU / NNAPI / GPU), ONNX graph optimisation level, sustained performance mode, and input seed
- **Run Mode** — load any model and run real inference on a camera photo, gallery image, or typed text; auto-detects model type (classifier, detector, text/NLP, generic) and visualises output accordingly
- **Live Mode** — split-screen real-time inference: top half shows camera feed with detection overlays, bottom half shows model output continuously
- **Reproducible inputs** — seeded PRNG (default seed 42) ensures identical random input tensors across models and runs for fair comparison
- **Energy & power** — per-inference energy estimate (mJ) via BatteryManager / sysfs
- **Box-plot visualisation** — inference time distribution with IQR, median, mean, and outliers
- **Supports** TensorFlow Lite (`.tflite`) and ONNX (`.onnx`) models

---

## Supported Model Types (Run & Live Mode)

| Detected Type | Input | Output visualisation |
|--------------|-------|---------------------|
| Image Classifier | Image / Camera | Top-5 class confidence bars |
| Object Detector | Image / Camera | Bounding boxes drawn on image |
| Text / NLP | Text box | Sentiment score / class probabilities |
| Image-output (style transfer, depth, segmentation, super-resolution) | Image / Camera | Rendered bitmap (grayscale / RGB / segmentation colourmap) |
| Generic | Random tensor | Raw output values |

---

## Citation

If you use PMLB in your research or reference it in a publication, please cite:

```bibtex
@software{hassan2025pmlb,
  author    = {Hassan, Ali},
  title     = {{PMLB}: Pocket Machine Learning Benchmarking Application},
  year      = {2026},
  url       = {https://github.com/usmanialihassan92/PMLB},
  version   = {1.0.0},
  note      = {Android application for on-device benchmarking of TFLite and ONNX models}
}
```

Or in plain text:

> Hassan, A. (2025). *PMLB: Pocket Machine Learning Benchmarking Application* (Version 1.0.0) [Android application]. https://github.com/usmanialihassan92/PMLB

---

## Technical Details

| Component | Version |
|-----------|---------|
| TensorFlow Lite | 2.17.0 |
| ONNX Runtime | 1.21.0 |
| CameraX | 1.4.0 |
| Min Android SDK | 26 (Android 8.0) |
| Target Android SDK | 35 |

---

## Developer

**Ali Hassan**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ali-haxan/)
[![Google Scholar](https://img.shields.io/badge/Google%20Scholar-4285F4?style=flat&logo=google-scholar&logoColor=white)](https://scholar.google.com/citations?user=YMvX-2sAAAAJ&hl=en)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/usmanialihassan92)

---

## License

MIT License — see [LICENSE](LICENSE) for details.
