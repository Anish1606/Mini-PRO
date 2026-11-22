# Convolutional Neural Networks for Automated Musical Instrument Classification

**10-Minute Conference Presentation Script**

## SLIDE 1 – INTRODUCTION

Good morning to the respected judges, faculty members and everyone present here.

We are here to present our research paper titled **"Convolutional Neural Networks for Automated Musical Instrument Classification."**

I am Antin Shanio A, along with my co-author Anish T, from the Department of Electrical and Electronics Engineering, St. Joseph's College of Engineering.

Our research focuses on developing an automated system that can identify different musical instruments from audio recordings using Convolutional Neural Networks.

The main idea behind this project is to combine audio signal processing and deep learning to make musical instrument recognition more automated, efficient and accessible.

## SLIDE 2 – RESEARCH CONTEXT AND PROBLEM STATEMENT

Musical instrument recognition is an important application of Music Information Retrieval.

Traditionally, identifying musical instruments in an audio recording requires a person to listen to the recording and manually identify the instruments.

However, this becomes challenging when multiple instruments are playing simultaneously.

For example, consider a musical recording containing guitar, piano, drums and violin. Their sounds may overlap, making it difficult to distinguish one instrument from another.

Additionally, variations in pitch, playing style, background noise and recording conditions make the identification process even more complicated.

Traditional signal-processing methods also have limitations because they mainly depend on manually designed features.

Therefore, our research aims to overcome these challenges by developing an automated instrument recognition system using deep learning.

## SLIDE 3 – OBJECTIVES

The primary objective of our project is to develop an AI-based system for automated musical instrument recognition from audio recordings.

Our specific objectives are:

First, to process different audio formats such as WAV, MP3, OGG and FLAC.

Second, to extract meaningful features from audio signals using audio-processing techniques.

Third, to implement a Convolutional Neural Network for multi-label classification of musical instruments.

Fourth, to generate confidence scores for the identified instruments.

Finally, to develop an interactive web application that provides waveform and spectrogram visualizations along with the classification results.

The overall aim is to make the instrument recognition process automated and user-friendly.

## SLIDE 4 – LITERATURE REVIEW

Before developing our system, we referred to several existing research works related to musical instrument recognition and audio classification.

The research work by Bosch and colleagues discusses sound segregation techniques for predominant instrument recognition.

McFee and colleagues introduced Librosa, which provides important functionalities for audio processing and music signal analysis.

Han and colleagues demonstrated the application of deep convolutional neural networks for predominant instrument recognition in polyphonic music.

Joder and colleagues highlighted the importance of temporal information in audio classification.

We also studied the OpenMIC dataset, which focuses on multiple-instrument recognition in real-world music recordings.

These research works helped us understand the existing approaches and select suitable techniques for our proposed system.

## SLIDE 5 – COMPARATIVE STUDY

When comparing our approach with existing methods, we considered manual identification, rule-based signal processing and traditional machine-learning techniques.

Manual identification is time-consuming and depends on human observation.

Rule-based approaches depend on predefined features and may not perform consistently when audio signals contain overlapping instruments or background noise.

Traditional machine-learning methods, such as Support Vector Machines and K-Nearest Neighbours, also depend heavily on the quality of manually extracted features.

In our proposed approach, we use CNNs to automatically learn useful patterns from audio features.

Additionally, our system supports multi-label classification and provides visual feedback through an interactive web application.

## SLIDE 6 – PROPOSED METHODOLOGY

Now coming to our proposed methodology.

Our system follows five major stages.

The first stage is audio input, where the user uploads an audio recording through the web application.

The second stage is preprocessing, where the audio is standardized using the Librosa library.

The third stage involves feature extraction, where meaningful time-frequency information is obtained from the audio signal.

The fourth stage is classification, where the extracted features are passed to the trained CNN model.

Finally, the system generates instrument predictions along with their confidence scores.

All these stages are integrated into a Streamlit-based web application.

## SLIDE 7 – AUDIO PREPROCESSING AND FEATURE EXTRACTION

Audio preprocessing is an important stage because different audio recordings may have different sampling rates and channel configurations.

Our system supports WAV, MP3, OGG and FLAC audio formats.

Using Librosa, the input audio is resampled to 22.05 kilohertz and converted into a mono-channel signal.

After preprocessing, we perform onset detection to identify important points in the audio, particularly the beginning of musical notes.

This helps us identify the musically active regions of the recording.

Short segments are then selected around these detected landmarks.

The selected audio segments are converted into Mel spectrogram representations.

In our implementation, we use 128 Mel frequency bands, and the resulting feature representation is resized to 128 by 130.

These features provide the CNN with a structured representation of how frequency energy changes over time.

## SLIDE 8 – CNN MODEL AND MULTI-LABEL CLASSIFICATION

This slide explains the CNN architecture used in our project.

The extracted audio features are provided as input to the convolutional neural network.

The convolutional layers learn important patterns from the input features.

Batch normalization helps stabilize the training process, while pooling reduces the feature dimensions.

Dropout is used to reduce overfitting and improve the model's ability to generalize.

The extracted features are then passed through fully connected layers.

Finally, we use a sigmoid activation function to generate independent confidence scores for each instrument class.

One important point here is why we selected sigmoid instead of softmax.

In a musical recording, multiple instruments can be present simultaneously.

For example, a single recording may contain guitar, drums and piano.

Softmax generally makes the classes compete with one another, whereas sigmoid calculates an independent score for each class.

Therefore, sigmoid is suitable for our multi-label classification approach.

## SLIDE 9 – SYSTEM ARCHITECTURE

This slide illustrates the overall system architecture.

The frontend of our application is developed using Streamlit, which allows users to upload audio files and view the classification results.

Librosa is used for audio preprocessing and feature extraction.

PyTorch is used to implement and execute the CNN model.

After classification, Plotly is used to display the results through interactive visualizations.

Our application provides four important visual outputs.

They are the audio waveform, onset landmarks, Mel spectrogram, confidence bar chart and radar chart.

These visualizations help users understand not only the final prediction but also the different stages of audio analysis.

The application also maintains session-based analysis history.

## SLIDE 10 – EXPERIMENTAL PROCEDURE

For experimental evaluation, we used the IRMAS dataset as the training reference.

The experimental procedure begins with audio data preparation and preprocessing.

The audio recordings are standardized to a sampling rate of 22.05 kilohertz and converted into mono-channel format.

Next, onset detection is performed, followed by feature extraction and CNN-based classification.

We then evaluate the classification results using the available instrument labels.

We also tested the complete application workflow, including audio uploading, preprocessing, feature extraction, prediction and visualization.

This helped us verify the functioning of the complete system.

## SLIDE 11 – RESULTS AND OBSERVATIONS

Coming to the experimental results, our project report records an overall test accuracy of 84 percent.

The training performance graph illustrates the model's learning behaviour during the training process.

Our system successfully generates instrument predictions along with confidence scores.

One important observation is that performance on unseen audio recordings still requires improvement.

The project report also mentions a validation accuracy of approximately 54.7 percent.

This indicates that although the model learns useful patterns from the training data, its ability to generalize to different audio recordings remains a challenge.

Therefore, the results demonstrate the feasibility of CNN-based musical instrument recognition, while also highlighting the need for further improvement.

## SLIDE 12 – COMPARATIVE STUDY

Compared with conventional approaches, our system provides several additional capabilities.

It automatically processes audio, learns features using CNNs, supports multiple instrument predictions and provides individual confidence scores.

Another important advantage is the visual representation of the results.

Instead of displaying only the predicted instrument names, our application provides waveform and spectrogram visualizations along with confidence charts.

This makes the classification process easier to understand and more useful for educational and analytical applications.

## SLIDE 13 – LIMITATIONS AND FUTURE SCOPE

Although our implementation demonstrates the proposed approach, there are certain limitations.

The primary limitation is the size and diversity of the training dataset.

The available computational resources also restrict the training of larger and more complex models.

In future, we plan to explore larger datasets such as NSynth, implement data augmentation and investigate advanced architectures such as CNN-RNN hybrid models and transformer-based approaches.

We also plan to extend the system towards real-time microphone input, persistent storage and cloud-based deployment.

These improvements can help enhance the accuracy, generalization and practical usability of the system.

## SLIDE 14 – CONCLUSION AND FUNDING ACKNOWLEDGEMENT

To conclude, we have developed an automated musical instrument recognition system using Convolutional Neural Networks.

By combining audio preprocessing, feature extraction and deep learning-based classification, our system can identify musical instruments from uploaded audio recordings.

The project report records 84 percent test accuracy.

The Streamlit-based application further improves usability by providing visual representations of the audio signal and classification results.

Our work demonstrates how deep learning can be applied to music information retrieval and automated audio analysis.

Regarding funding, no external funding agency is identified in the supplied project documents.

We would also like to acknowledge our project guide, Ms. S. P. Vedavalli, for her valuable guidance and support throughout this project.

## SLIDE 15 – REFERENCES AND CLOSING

These are some of the important research papers and technical references that supported our work.

With that, we conclude our presentation.

Thank you for your valuable time and attention.

We are happy to answer your questions.
