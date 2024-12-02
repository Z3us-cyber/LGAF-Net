# LGAF-CNN for BCI Movement Classification

This repository will contain the implementation code for our paper "Are GAFs All You Need for BCIs?", which explores a novel approach to EEG-based Brain-Computer Interface movement classification using Learnable Gramian Angular Fields (LGAFs).

## Paper Overview

Brain-Computer Interfaces (BCIs) face several key challenges:
- Processing high-dimensional EEG data efficiently
- Managing signal-to-noise ratios
- Meeting real-time computation requirements

Our paper addresses these challenges by:
1. Introducing Learnable Gramian Angular Fields (LGAFs) for EEG signal processing
2. Demonstrating effective movement classification with minimal channels
3. Proposing an efficient CNN architecture for real-time applications

### Key Innovations

- **LGAF Transformation**: A learnable variant of GAFs that adaptively transforms time-series EEG data into 2D representations
- **Channel Optimization**: Achieved comparable performance using only three channels (CP2, C3, C4)
- **Efficient Architecture**: Integrated factorized convolutions and custom regularization techniques

### Experimental Results

Our preliminary study with four subjects showed:
- 93.06% classification accuracy across six hand movements
- Successful classification of forward, backward, left, right, up, and down movements
- Maintained performance (93.07% accuracy) with only three EEG channels
- F1-scores ranging from 0.89 to 0.96 across movement types

## Requirements

This implementation will require:
- Python 3.8+
- PyTorch
- NumPy
- SciPy
- MNE-Python
- Scikit-learn

## Model Architecture

The system consists of three main components:

1. **LGAF Transformation Layer**
   - Learnable parameters for signal transformation
   - Adaptive feature extraction
   - Efficient computation of angular fields

2. **CNN Architecture**
   - Factorized convolutional layers
   - Custom regularization techniques
   - Optimized for real-time processing

3. **Classification Layer**
   - Movement type prediction
   - Six-class output (corresponding to movement directions)

## Dataset

The experiments used EEG data recorded using an Enobio 8 system with:
- Four subjects
- Six distinct hand movements
- 500 Hz sampling rate
- 11-second trials
- Haptic feedback-enhanced virtual environment

Due to privacy considerations, the data is not included in this repository.

## Citation

If you find this work useful, please cite our paper:

```bibtex
@article{hernandez2024gafs,
  title={Are GAFs All You Need for BCIs?},
  author={Hernandez Gomez, A. and Nieto, N. and Podesta, M. O. and Felix, F. and Munoz, L. A.},
  journal={TBD},
  year={2024}
}
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

We thank Andrés Ayala and Mostla, Tecnologico de Monterrey for providing access to the Enobio8 system used in data collection.
