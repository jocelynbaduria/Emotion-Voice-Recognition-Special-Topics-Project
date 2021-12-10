# Emotion Voice Recognition 
## Speech to Text Application with WandB, Gradio and Vertex AI Implementation

1. [Video](https://drive.google.com/file/d/1KAxbi_Aawc2t_2clSeDiPbpuLn4VKABv/view?usp=sharing)
2. [Presentation Slide Deck](https://docs.google.com/presentation/d/1-oAgCE3lRnfluL5_81Fle0Ob5clA56obJb8_h8iBp6k/edit#slide=id.g103c86387bb_0_166)
3. [Project Final Report](https://docs.google.com/document/d/1q2SaXnbcIpTH_P9CYasodLvXIYnPD5wzxFNv73Lzajw/edit#)
4. [Data](https://drive.google.com/drive/folders/1A-hQey9c_l-zRqQeAXd79XCkUjwT5h5a?usp=sharing)

### Project Overview

(EVR) Emotion Voice Recognition is one of the latest topics in the AI space. Our project will focus on identifying the emotion of people's utterances (Fig.1) with the use of deep learning. The (ASR) Automatic Speech Recognition concept will be applied to emotion voice recognition. 

![Screen Shot 2021-12-09 at 4 18 55 PM](https://user-images.githubusercontent.com/62075076/145496360-e1662af5-2856-4ae4-b395-5a14b4142732.png)

       
               
The ASR approach will use an audio signal as an input and it will do the feature extraction of the speech, its text, pronunciation, and acoustic model (Fig.3). The extracted input signal will be passed to the decoder to convert the audio signal to text. The speech extracted data will be converted into an statistical parameter with a representation of graphical frequency. 

 ![Fig.3](https://user-images.githubusercontent.com/62075076/145496151-86934bdb-765d-4c74-9ec0-b3ac20fecbf7.png)

The most common used for this feature extraction is the (MFCCs) Mel-frequency cepstrum.  This feature extraction technique has a “frame shift and length usually between 20 and 32 ms, using 1024 frequency bins, 26 mel channels and between 10 and 40 cepstral coefficients with cepstral mean normalization”[2]. The MFCCs have a high accuracy of voice recognition but with low complexity. 

The main core deep learning model that we will apply in EVR is XLSR-Wav2Vec2 for Multi-Lingual ASR with Transformers of Facebook AI (Fig.5). The XLSR-Wav2Vec2 is fine-tuned using (CTC) Connectionist Temporal Classification, an algorithm used to train neural networks for sequence-to-sequence problems in Automatic Speech Recognition and Handwriting Recognition.

![Screen Shot 2021-12-09 at 4 20 52 PM](https://user-images.githubusercontent.com/62075076/145496224-24d208cc-42d0-4e74-8cde-8dac45b6cc33.png)

### Why Emotion Voice Recognition is Important?

The problem we want to solve is how to identify the emotion based on voice signal communication. This project is applicable to any form of voice signal communication and can be extended to study on voice lie detection tests, call centers services, audio voice interview and health care surveillance systems. This project will help government agencies in solving crimes, businesses in assisting technical and customer services, doctors and patients with needs on emotional support in health care services. The overall results of our project visualizations of emotion using the harmonics, waveplot, autocorrelation, RMSE metric score of audio files correspond to the degree of emotion thus it has a good detection of emotions in voice. This entails that the project will have a promising application in other fields of voice application in any industries.

### Experiments and Results

The team had explored various visualization techniques for this project and we were able to use some visualization techniques for audio input such as Harmonic, RMSE audio plotting using Librosa library, waveplot, and autocorrelation. The Emotion visualization corresponds to the waveplot and harmonic, the Happy emotion shows a wider range value compared to the Angry emotion.

We also captured some visualizations of training accuracy/loss/runtime, evaluation accuracy/loss/runtime and GPU memory usage deployment in Weights and Biases server. We had also added some visualizations of GCP cloud storage, Vertex AI performance training evaluation of our ESD audio dataset.  

The project was deployed in Gradio App using GCP Colaboratory. The results of audio file uploading in Gradio App was successfully predicted based on its emotions. The Happy audio input signal was recognized as Surprise based on the tone of the voice. 

1. Gradio App
![Screen Shot 2021-12-09 at 12 47 51 AM](https://user-images.githubusercontent.com/62075076/145441600-4fbc8fe3-b71b-416c-b835-e86624c07911.png)
2. Visualization: Happy Voice Emotion
   ![image](https://user-images.githubusercontent.com/46585696/145463773-5c920e8e-332a-4bfc-85ca-abc12943e270.png)

   
   Visualization: Angry Voice Emotion
   ![image](https://user-images.githubusercontent.com/46585696/145463974-feed81bf-9166-4736-93eb-a215591d8385.png)


3. WandB
![Screen Shot 2021-12-09 at 12 51 32 AM](https://user-images.githubusercontent.com/62075076/145441897-fb289221-5a49-4b9a-b6aa-184c71cb6c2d.png)
![Screen Shot 2021-12-09 at 12 53 06 AM](https://user-images.githubusercontent.com/62075076/145441923-75844263-7a09-42a7-b85b-de00ab26bd05.png)
![Screen Shot 2021-12-09 at 12 53 26 AM](https://user-images.githubusercontent.com/62075076/145441969-0246b3d7-b5d9-4fb2-a4c2-1e4b49259517.png)
4. Vertex AI 
   Training 
![Vertex Training](https://user-images.githubusercontent.com/62075076/145491796-d4ade55e-6c59-47f4-9400-336c1bc2deb6.jpeg)

   Audio Emotion Storage
![Audio Emotion Storage Overview](https://user-images.githubusercontent.com/62075076/145492028-683d8e07-86eb-4453-832a-dc70ab554faf.jpeg)

   Logging
 ![Logging](https://user-images.githubusercontent.com/62075076/145492091-34c2d6e9-acb1-4cfa-b202-6399e7f8ac5f.jpeg)

   Monitoring
 ![Monitoring](https://user-images.githubusercontent.com/62075076/145492119-16800c67-af59-4c4d-bbe4-9805d5a2e913.jpeg)
