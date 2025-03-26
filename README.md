# Bird Density Estimation from Audio

## Overview
This project aims to estimate bird density in a forest environment using audio recordings. The model processes audio files, extracts spectrogram features, and employs a Convolutional Neural Network (CNN) to classify bird call occurrences. The results are further processed to estimate bird density in different recordings.

## Features
- **Audio Processing**: Converts raw audio recordings into spectrograms for feature extraction.
- **Machine Learning Model**: The CNN uses the spectrogram to extract relevant features and feeds it to the FC layers for prediction
- **Dataset Balancing**: Handles class imbalance by adjusting class weights (or) by random undersampling.
- **Evaluation & Visualization**: Displays training metrics (loss, precision, recall) through plots.
- **Batch Prediction**: Processes multiple audio files and exports results to a CSV file.

## Data Preprocessing

- Audio files are resampled to 16kHz.
- Spectrograms are generated using Short-Time Fourier Transform (STFT).

## Project Structure
```
📂 Project
├── 📁 Notebooks              
│   ├── Model_1.ipynb      # Contains The Model Implementation With Random Undersampling        
│   ├── Model_2.ipynb      # Contains The Model Implementation With Weighted Classes
├── 📁 Results              
│   ├── Actual.csv         # Contains The Actual No. Of Capuchin calls per file
│   ├── Predicted.csv      # Contains The Actual No. Of Capuchin calls per file
├── 📁 Saved Model               
│   ├── model_2.keras      # Saved Weights For Model 2
└── README.md                 
```

## Results
- Final predictions are exported to predictions.csv.
- The model's performance is evaluated by computing the total error between actual and predicted values.

## Future Improvements
- Experiment with different CNN architectures.
- Implement additional audio augmentation techniques.
- Fine-tune hyperparameters for better accuracy.

## Dataset
https://www.kaggle.com/datasets/kenjee/z-by-hp-unlocked-challenge-3-signal-processing

## Contributing
Contributions are welcome! Feel free to open issues or submit pull requests.
