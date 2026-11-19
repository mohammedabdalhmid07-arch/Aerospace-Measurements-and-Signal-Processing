# Aerospace Measurements & Signal Processing Lab (MATLAB)

A comprehensive suite of experimental data reduction, spectral analysis, and analog signal conditioning workflows developed in **MATLAB** for the Aerospace Engineering Measurements & Instrumentation Lab at Cairo University.

---

## Project Modules & Technical Scope

### 1. Wind Tunnel Aerodynamic Data Reduction
* **Coordinate Transformation:** Processed raw wind tunnel balance measurements from body-axis **Normal ($N$)** and **Axial ($A$)** force components into wind-axis **Lift ($L$)** and **Drag ($D$)** forces across varying Angles of Attack ($\alpha$):
  $$L = N \cos(\alpha) - A \sin(\alpha)$$
  $$D = N \sin(\alpha) + A \cos(\alpha)$$
* **Aerodynamic Polar Generation:** Evaluated force behavior across flow regimes and validated experimental trends.

### 2. Time-Domain & Frequency-Domain Analysis (FFT)
* **Signal Synthesis & Decomposition:** Constructed multi-component signals and transformed raw time-series measurements into the frequency domain using the **Fast Fourier Transform (FFT)**.
* **Spectral Visualization:** Analyzed single-sided amplitude spectra using linear and logarithmic (`semilogy` / `loglog`) scales to isolate dominant carrier frequencies from background harmonics.

### 3. Noise Modeling & Blind Signal Identification
* **Synthetic Noise Injection:** Generated and superimposed two distinct noise profiles (broadband random noise and high-frequency tonal interference) onto clean baseline signals.
* **Blind Signal Diagnostics:** Developed a systematic workflow to inspect unknown/external signal files, separate the fundamental **main signal** from noise components in both time and frequency domains, and extract filter design specifications.

### 4. Analog Filter Design, Implementation & Trade-off Evaluation
* **Filter Architecture Comparison:** Designed, simulated, and compared multiple analog filter families (including **Butterworth** and **Elliptic** filters) using MATLAB's *Analog Filter Designer* and Transfer Function (`tf`) modeling.
* **Parameter Sizing:** Determined required filter order ($n$), cutoff frequencies ($\omega_c$), passband ripple ($G_p$), and stopband attenuation ($G_s$) based on spectral separation requirements.
* **Performance & Distortion Metrics:**
  * Plotted intrinsic filter frequency responses (Magnitude $|H(j\omega)|$ and Phase Shift $\angle H(j\omega)$).
  * Evaluated post-filtering signal fidelity by comparing clean, noisy, and recovered signals in both domains, quantifying the trade-off between sharp roll-off attenuation and phase distortion.

---

## Key Visuals & Results
> *Tip: Export high-resolution plots from your MATLAB Live Scripts and place them in `/assets`.*

* **Time vs. Frequency Domain (Noisy vs. Clean):** `![FFT Analysis](assets/fft_comparison.png)`
* **Filter Magnitude & Phase Response:** `![Filter Response](assets/filter_bode.png)`
* **Recovered Signal Overlay:** `![Filtered Signal](assets/filtered_output.png)`

---

## Tools & Environment
* **MATLAB** (Live Scripts `.mlx`, Signal Processing Toolbox, Analog Filter Designer)
* **Documentation:** Exported technical reports (`.pdf`) included in each module directory.
