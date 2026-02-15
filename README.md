# Frequency Domain Image Processing: Blurring and Sharpening

## Overview

This project demonstrates frequency domain image processing techniques for blurring and sharpening images using the Fourier Transform. It provides a comprehensive exploration of how images can be manipulated by transforming them from the spatial domain to the frequency domain, applying various filters, and transforming back to produce enhanced or modified images.

## Key Features

- **Discrete Fourier Transform (DFT)**: Implementation of 2D DFT and Inverse DFT for image transformation
- **Low-Pass Filters** (for blurring):
  - Ideal Low-Pass Filter (ILPF)
  - Butterworth Low-Pass Filter (BLPF)
  - Gaussian Low-Pass Filter (GLPF)
- **High-Pass Filters** (for sharpening):
  - Ideal High-Pass Filter (IHPF)
  - Butterworth High-Pass Filter (BHPF)
  - Gaussian High-Pass Filter (GHPF)
- **Comprehensive comparison** of filter characteristics and visual outcomes
- **Educational content** covering theoretical foundations and practical applications

## Project Structure

```
├── project.ipynb          # Main Jupyter notebook with all implementations
├── README.md             # This file
└── images/               # Directory for test images
```

## Prerequisites

- Python 3.x
- OpenCV (`cv2`)
- NumPy
- Matplotlib

Install dependencies:

```bash
pip install opencv-python numpy matplotlib
```

## Usage

### Running Locally

1. Ensure your image file is placed in the `images/` directory
2. Update the image path in the notebook:
   ```python
   image_path = 'images/your_image.tiff'
   ```
3. Run the notebook cells in order:
   - Cell 1: Image loading and setup
   - Cell 2: Core DFT functions demonstration
   - Cell 3: Low-pass filter implementation and demonstration
   - Cell 4: High-pass filter implementation and demonstration
   - Cell 5: Complete filtering comparison

### Running on Google Colab

The notebook includes Google Colab compatibility. Click the "Open in Colab" badge at the top of the notebook to run it directly in Colab (ensure your image is accessible via Google Drive).

## Theoretical Background

The notebook covers:

- **2D Continuous Fourier Transform (CFT)**: Mathematical foundation and equations
- **2D Discrete Fourier Transform (DFT)**: For digital image processing
- **Frequency Components**: Understanding low and high frequencies in images
- **Convolution Theorem**: Relationship between spatial and frequency domain filtering
- **Filter Design Principles**: How different filter types work and their trade-offs

## Results and Discussion

### Low-Pass Filters (Blurring)

- **Ideal LPF**: Sharp blurring but introduces ringing artifacts
- **Butterworth LPF**: Smooth blurring with reduced artifacts; tunable via order parameter
- **Gaussian LPF**: Smoothest blurring effect with minimal artifacts

### High-Pass Filters (Sharpening)

- **Ideal HPF**: Strong edge enhancement but significant artificial ringing
- **Butterworth HPF**: Balanced sharpening with controlled artifacts
- **Gaussian HPF**: Natural-looking sharpening without ringing effects

## Real-World Applications

- **Medical Imaging**: Noise reduction and feature enhancement
- **Satellite/Aerial Imaging**: Atmospheric haze removal and feature enhancement
- **Computer Vision**: Preprocessing for object detection and segmentation
- **Forensic Analysis**: Detail enhancement in forensic images
- **Security & Surveillance**: Quality enhancement and privacy protection
- **Astronomy**: Noise cleaning and celestial object enhancement

## Key Functions

### Core DFT Functions

- `dft2d(img_gray)`: Performs 2D Discrete Fourier Transform
- `shift_dft(dft_result)`: Shifts zero-frequency component to center
- `idft2d(shifted_dft_result)`: Performs Inverse 2D DFT

### Low-Pass Filter Functions

- `create_ideal_lowpass_filter(rows, cols, D0)`
- `create_butterworth_lowpass_filter(rows, cols, D0, n)`
- `create_gaussian_lowpass_filter(rows, cols, D0)`

### High-Pass Filter Functions

- `create_ideal_highpass_filter(rows, cols, D0)`
- `create_butterworth_highpass_filter(rows, cols, D0, n)`
- `create_gaussian_highpass_filter(rows, cols, D0)`

### Utility Functions

- `apply_filter(shifted_dft, filter_mask)`: Applies filter mask and performs IDFT

## Parameters

- **D0**: Cutoff frequency (controls the transition point between low and high frequencies)
  - For low-pass: Smaller D0 = more blurring
  - For high-pass: Larger D0 = more sharpening
- **n**: Butterworth filter order (controls the sharpness of transition)
  - Higher n = sharper transition, more artifacts
  - Lower n = smoother transition, fewer artifacts

## Conclusions

Through this project, we demonstrated that:

1. **Gaussian filters** provide the most visually pleasing results with smooth transitions and minimal artifacts
2. **Butterworth filters** offer flexibility with tunable parameters for balancing effect and quality
3. **Ideal filters** are conceptually simple but introduce problematic ringing artifacts
4. **Filter selection** should be based on specific application requirements and desired trade-offs
5. **Frequency domain processing** provides powerful tools for image enhancement across numerous fields

## Future Enhancements

- Adaptive filtering techniques based on image characteristics
- Comparison with spatial domain filtering methods
- Extension to color images (per-channel processing)
- Automated parameter selection methods
- Real-time filtering implementations
- Integration with machine learning pipelines

## References

- 2D Fourier Transform properties and applications
- Digital Image Processing principles
- Filter design methodologies
- OpenCV and NumPy documentation

## Group List

| No. | Student Name         | Student ID |
| --- | -------------------- | ---------- |
| 1   |                      |            |
| 2   | Eugene Baidoo        | 11310591   |
| 3   | Bernard Mensah Afful | 11253585   |
| 4   | Addo Gabriel         | 11118661   |
| 5   | Oswald Amoah         | 11046928   |
| 6   | Nyanyo Edem larry K  | 11052329   |
| 7   |                      |            |
| 8   |                      |            |
| 9   |                      |            |
