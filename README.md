# Drowsiness Detection App

Computer-vision prototype that estimates driver alertness from eye and face cues and can trigger a warning when drowsiness is detected.

## Pipeline

```mermaid
flowchart LR
    A[Camera frame] --> B[Face detection]
    B --> C[Eye-region detection]
    C --> D[Temporal alertness signal]
    D --> E[Driver warning]
```

## Engineering notes

- Uses OpenCV Haar-cascade assets for face and eye-region detection.
- Keeps the inference loop simple enough for an edge-oriented prototype.
- The project is a research/learning prototype; production deployment should add temporal calibration, precision/recall evaluation, low-light testing, and privacy controls.

## Run

Open `APP.ipynb` or `project.ipynb` after installing the notebook dependencies. The cascade XML files must remain beside the notebook or be referenced through a configurable path.
