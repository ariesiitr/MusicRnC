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

*   **Fourier Transform(feature extraction)**
    
    *   Apply Fourier Transform to convert the time-domain audio signal into the frequency domain.
        
    *   ```D  = librosa.stft(y)```
        
    *   D is the short-time Fourier transform of the audio signal.
        
*   **Mel-frequency Cepstral Coefficients (MFCC) Extraction**
    
    *   Extract MFCC features which are critical for audio analysis and classification.
        
    *   ```mfccs = librosa.feature.mfcc(y=y, sr=sr, n\_mfcc=13)```
        
    *   mfccs is a matrix containing the MFCC features.
        

Importance of Feature Extraction
--------------------------------

*   **Feature Extraction**
    
    *   Essential for converting raw audio data into a format that is suitable.
        
    *   Helps in capturing the relevant patterns and characteristics of the audio signal.
 
### Model Architecture
------------------

*   **Convolutional Layers**
    
    *   Use multiple Conv2D layers to capture spatial features from the audio spectrograms.
        
    *   Parameters include the number of filters, filter sizes, and strides.
        
    *   ```from tensorflow.keras.layers import Conv2Dmodel.add(Conv2D(filters=32, kernel\_size=(3, 3), strides=(1, 1), activation='relu', input\_shape=input\_shape))```
        
*   **Activation Functions**
    
    *   Primarily use ReLU (Rectified Linear Unit) for non-linearity.
        
    *   ```from tensorflow.keras.layers import Activationmodel.add(Activation('relu'))```
        
*   **Pooling Layers**
    
    *   Incorporate MaxPooling2D layers to downsample the feature maps.
        
    *   ```from tensorflow.keras.layers import MaxPooling2Dmodel.add(MaxPooling2D(pool\_size=(2, 2)))```
        
*   **Dropout Layers**
    
    *   Use Dropout layers to prevent overfitting by randomly setting a fraction of input units to 0.
        
    *   ```from tensorflow.keras.layers import Dropoutmodel.add(Dropout(rate=0.5))```
        
*   **Batch Normalization**
    
    *   Apply BatchNormalization to normalize the output of previous layers, accelerating training and improving performance.
        
    *   ```from tensorflow.keras.layers import BatchNormalizationmodel.add(BatchNormalization())```
        
*   **Flattening**
    
    *   Use Flatten to convert the 2D matrices into a 1D vector before passing to fully connected layers.
        
    *   ```from tensorflow.keras.layers import Flattenmodel.add(Flatten())```
        

Rationale and Design Philosophy
-------------------------------

*   **Parameter Selection**
    
    *   Careful selection of parameters like the number of filters, kernel sizes, and dropout rates to balance performance and complexity.
        
    *   ```Conv2D(filters=32, kernel\_size=(3, 3), strides=(1, 1))Dropout(rate=0.5)```
        
    *   Ensures that the model is both deep enough to capture complex patterns and regularized to prevent overfitting.
        

Made by:

Pranjal Vanjale

Siddhant Gupta

Vidhi Gupta

Yashovardhan Pandey

(Students of IIT Roorkee B.tech. First Year)


Mentored By:
Shreshth Mehrotra

Ashwarya Rao Maratha
