# Body-Language-Detection

Body Language Decoder with MediaPipe, OpenCV and python in real time

## :memo:  Note
Before going forward with the project, create a new python environment and install all mediapipe and OpenCV

## :memo: Decription
In this project, I leveraged Mediapipe python library to estimate both facial and body landmarks using the holistic mediapipe solution. 
With that data I built a custom pose classification model that allows us to decode what a person might be conveying with their body language with acceptable accuracy.
The classes I selected for my body language detection are namely thumbs up,victory,happy,peace,thank you and live long.

Dataset creation and model building process: The dataset (landmark.csv) was created by extracting the facial and body landmark coordinates which were rendered
on the frames(images) captured by my VideoCapture device(webcam) in real time using OpenCV. 

Training process: Since the problem falls in the domain of Mutli-Class classification, after splitting the data into train and test, I used the Random Forest Classifier 
to train the model. After training the model, I dumped it into a pickle file. 
Finally, evaluated the model's performance by detecting the body language poses (the model was trained on), on real-time feed we receive from the webcam using OpenCV.


## :cloud: Algorithms and technologies used to build this model :-

1.  Mediapipe
2. OpenCV
3. Random Forest Classifier
