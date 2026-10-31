# CMSIS-STFT

A streaming Short-Time Fourier Transform (STFT) library for Arm Cortex-M microcontrollers, built on CMSIS-DSP. It supports F32, Q15 and Q31 precision and uses no dynamic memory allocation.

## Contents

| Folder | Description |
|---|---|
| `cmsis_stft_library/` | The library (`inc/` headers, `src/` source) |
| `examples/` | STM32F407 example firmware (STM32CubeIDE projects) |
| `pc_datalogger/` | PC application that receives, plots and logs the STFT output over USB |
| `matlab/` | Test-signal generator and verification script (reference: MATLAB `spectrogram`) |

## Requirements
- CMSIS-DSP 5.9.0 (not included)
- STM32CubeIDE, for the examples
- Python 3, for the datalogger
- MATLAB with the Signal Processing Toolbox, for verification

## Workflow
1. Generate the test signals with `matlab/Test_Signal_Generator.m`.
2. Build and flash an example from `examples/`.
3. Capture the output with `pc_datalogger/`. This saves an `.xlsx` file.
4. Compare it against MATLAB with `matlab/V3_MATLAB_Native_STFT_verify.m`.

Each folder has its own README.

