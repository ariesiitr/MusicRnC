# Music Recommendation and Classification

## Introduction
A project that utilizes Convolutional Neural Networks and feature selection techniques from audio data to create a music recommendation system and genre classification, providing a personalized and seamless listening experience.

## Presentation

[Explaination of our thinking](https://docs.google.com/presentation/d/1zzPMQsCPdOJwwZgkPYTzKr8t4RiqIoSack5H5CHUUow/edit?usp=sharing)

## Data Preprocessing 
Initial Steps
-------------

*   **Loading Audio Files**
    
    *   Utilize the librosa library to load audio files.
        
    *   ```import librosay, sr = librosa.load('path\_to\_audio\_file.wav')```
        
    *   y is the audio time series, and sr is the sampling rate.
        

Transformation Process
----------------------

*   **Fourier Transform**
    
    *   Apply Fourier Transform to convert the time-domain audio signal into the frequency domain.
        
    *   This process is essential for feature extraction.
        
    *   ```
         D  = librosa.stft(y)
        ```
        
    *   D is the short-time Fourier transform of the audio signal.
        
*   **Mel-frequency Cepstral Coefficients (MFCC) Extraction**
    
    *   Extract MFCC features which are critical for audio analysis and classification.
        
    *   ```mfccs = librosa.feature.mfcc(y=y, sr=sr, n\_mfcc=13)```
        
    *   mfccs is a matrix containing the MFCC features.
        

Importance of Feature Extraction
--------------------------------

*   **Feature Extraction**
    
    *   Essential for converting raw audio data into a format that is suitable .
        
    *   Helps in capturing the relevant patterns and characteristics of the audio signal.

Made by:

Pranjal Vanjale

Siddhant Gupta

Vidhi Gupta

Yashovardhan

(Students of IIT Roorkee B.tech. First Year)


Mentored By:
Shreshth Mehrotra

Ashwarya Rao Maratha
