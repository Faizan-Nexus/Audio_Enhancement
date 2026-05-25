# Audio Enhancement

Speech enhancement is critical in applications such as telecommunications, hearing aids, and voice recognition systems, where background noise and hum can degrade audio quality.

This project demonstrates and compares multiple classic speech enhancement techniques using Python and Jupyter Notebook. It is designed for researchers, engineers, and students seeking to learn about digital audio denoising methods.

## Main Motive

**The main goal of this project is to remove noise and hum sounds from audio recordings, thereby improving the intelligibility and clarity of speech.** The enhancement techniques employed help in making speech more distinct and usable in real-world applications.

## Techniques Implemented

1. **LMS Adaptive Filtering**  
   Uses the Least Mean Squares (LMS) algorithm as an adaptive filter to remove unwanted noise and hum from speech.

2. **Spectral Subtraction**  
   Estimates background noise and removes it from the noisy speech signal in the spectral domain—very effective at reducing stationary noise and hum.

3. **Wiener Filtering**  
   Applies Wiener filtering in the STFT (Short-Time Fourier Transform) domain, adaptively suppressing noise based on the power spectra.

4. **SNR (Signal-to-Noise Ratio) Evaluation**  
   Quantitatively compares input, enhanced, and clean signals using SNR metrics to measure noise reduction performance.

## Conclusion

- **Spectral Subtraction provides the highest improvement in SNR, making it the most effective for noise and hum removal in the provided examples.**
- Wiener Filtering offers good enhancement, and LMS also reduces noise, but not as much as Spectral Subtraction.

| Technique             | SNR (dB) | Rank  |
|-----------------------|----------|-------|
| LMS Adaptive Filter   | 13.41    | 3rd   |
| Spectral Subtraction  | 17.67    | 1st   |
| Wiener Filter         | 15.92    | 2nd   |

## Visualization & Tools

- **Plots**: Signal waveforms, SNR bar charts for each enhancement technique, and spectrograms for visual comparison of denoising results.
- **Audio Playback GUI**: Listen to clean, noisy, and enhanced speech directly within the notebook interface.

## Requirements

- Python 3.x
- `numpy`
- `scipy`
- `librosa`
- `soundfile`
- `matplotlib`
- Jupyter Notebook

Install requirements with:
```bash
pip install numpy scipy librosa soundfile matplotlib jupyter
```

## How to Use

1. Place your clean speech file (`harvard.wav` or similar) and a noise sample (`sample-1.wav`) in the project directory.
2. Open `Audio Enhancement.ipynb` in Jupyter Notebook.
3. Execute all cells to:
   - Load and mix audio
   - Apply LMS, Spectral Subtraction, and Wiener filtering
   - Compare results (plots, SNR, audio playback)
   - View SNR improvement for each method

> **Note**: You may use your own `.wav` files—just name them accordingly or update the paths in the notebook.

## Project Files

- `Audio Enhancement.ipynb`: Main notebook implementing the techniques, experiments, plots, and analysis.
- `DataSet/`: Place your audio files here or in the root.
- `README.md`: Overview and instructions.

## References
- Haykin, S. (2002). Adaptive Filter Theory
- Boll, S.F. (1979). Suppression of acoustic noise in speech using spectral subtraction
- Lim, J.S., & Oppenheim, A.V. (1979). Enhancement and bandwidth compression of noisy speech

---

Explore the notebook for source code, detailed explanations, and hands-on audio enhancement experiments.
