# Active-Noise-Cancellation-in-Audio-Signal-Processing
Active Noise Cancellation (ANC) reduces unwanted noise by generating anti-noise signals. Using adaptive filters like LMS and RLS, it removes noise in real time, improving audio quality in systems like headphones.
Active Noise Cancellation (ANC) usingAdaptive Filters.

This project is a simple implementation of Active Noise Cancellation (ANC)using adaptive filtering techniques in Python. The main idea is to recover a cleansignal from a noisy input and compare how different adaptive algorithms performin doing so.

Overview
In practical audio systems, signals are often affected by unwanted noise. Thisproject simulates a feedforward ANC system, where:
• Aprimary input contains the original signal mixed with noise
• Areference input contains noise that is correlated with the primarynoise
• Anadaptive filter learns to estimate and remove this noiseThe final output is a cleaner version of the original signal.

Algorithms Implemented
The following adaptive algorithms are implemented and compared:
• Least Mean Square (LMS)
• Normalized Least Mean Square (NLMS)
• Recursive Least Square (RLS)
• Modified NLMS (sign-based variant)

How It Works
The noisy signal is modeled as:
d(n) = x(n) + n₂(n)
Where:
•x(n) → clean signal
• n₂(n)→ noise
A correlated noise reference
e(n) = d(n) - y(n)
Where:
•n₁(n) is passed through an adaptive filter:
y(n) → estimated noise
• e(n)→ final output (ideally close to the clean signal)
The adaptive algorithm continuously updates the filter to minimize this error.
Performance Metrics
To compare the algorithms, the following metrics are used:
• Mean Square Error (MSE) → measures how small the error is (lower
is better)
• Log Spectral Distance (LSD) → compares frequency content (lower is
better)
• Noise Reduction Ratio (NRR) → shows how much noise is removed
(higher is better)

Output
The program generates:
• Plots of clean and noisy signals
• Filtered outputs for each algorithm
• MSE convergence curves
• Comparison charts for LSD, NRR, and MSE

Requirements
Install the required libraries:
pip install numpy matplotlib
How to Run
python main.py

Key Observations
• LMS→ simple and easy to implement, but converges slowly
• NLMS→ improves stability and convergence compared to LMS
• RLS→ very fast convergence, but computationally expensive
•Modified NLMS→ offers a good balance between speed and complexity

Reference / Citation
This implementation is inspired by the following paper:
Atar Mon, Thiri Thandar Aung, Chit Htay Lwin"Active Noise Cancellation in Audio Signal Processing"International Research Journal of Engineering and Technology (IRJET), 2016

BibTeX
@article{mon2016anc,
title={Active Noise Cancellation in Audio Signal Processing},
author={Mon, Atar and Aung, Thiri Thandar and Lwin, Chit Htay},
journal={International Research Journal of Engineering and
Technology (IRJET)},
volume={3},
number={11},
year={2016}
}

Notes
• This is asimulation-based project(not real-time ANC)
• Noise used: Gaussian noise
• Signal used: sinusoidal waveform
Future Improvements
• Real-time ANC using microphone input
• Using speech signals instead of sine waves
• Implementation on embedded systems or DSP hardware

   Submitted From
  KUNCHUR KOTRESHA 
  241EC130 
  NATIONAL INSTITUTE OF TECNOLOGY KARNATAKA,SURATHKAL

