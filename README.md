# ECG Arrhythmia Classifier 🫀

## Overview
A machine learning model that detects cardiac arrhythmias from ECG signals
using the MIT-BIH Arrhythmia Database from PhysioNet.

## Results
- 99% accuracy on 20,000 unseen test beats
- Classifies 5 beat types:

| Label | Beat Type |
|---|---|
| N | Normal |
| A | Atrial Premature |
| V | Premature Ventricular Contraction |
| L | Left Bundle Branch Block |
| R | Right Bundle Branch Block |

## Dataset
- MIT-BIH Arrhythmia Database (PhysioNet)
- 48 patients, 112,000+ labeled heartbeats
- Download: https://physionet.org/content/mitdb/1.0.0/

## Methods
1. Load ECG signals using `wfdb`
2. Bandpass filter (0.5–40 Hz) to remove noise
3. Segment into individual beats (360 samples per beat)
4. Train a Random Forest Classifier (100 trees)
5. Evaluate on 20% held-out test set

## Libraries
- `wfdb` — load PhysioNet ECG data
- `numpy` — array processing
- `matplotlib` — signal visualization
- `scipy` — bandpass filtering
- `scikit-learn` — Random Forest, evaluation metrics
