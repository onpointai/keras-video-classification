ANALYSTICS VIDHYA
SEE ALSO - https://www.analyticsvidhya.com/blog/2019/09/step-by-step-deep-learning-tutorial-video-classification-python/
Learn how you can use computer vision and deep learning techniques to work with video data
We will build our own video classification model in Python
This is a very hands-on tutorial for video classification – so get your Jupyter notebooks ready


ALSO:
Deep Learning Tutorial to Calculate the Screen Time of Actors in any Video (with Python codes)
https://www.analyticsvidhya.com/blog/2018/09/deep-learning-video-classification-python/
Tom and Jerry - Is Tom on the screen/Jeerry on the screen or netiher?


Other advanced methods:
Five video classification methods implemented in Keras and TensorFlow
https://blog.coast.ai/five-video-classification-methods-implemented-in-keras-and-tensorflow-99cad29cc0b5
=============================================================================================


PYIMAGE
https://www.pyimagesearch.com/2019/07/15/video-classification-with-keras-and-deep-learning/  17/7/2019

Dexters-MacBook:keras-video-classification dexterdsilva$ tree
.
├── Sports-Type-Classifier
│   ├── README.md
│   ├── data
│   ├── readme_images
│   │   ├── acc_sports.png
│   │   ├── cric.png
│   │   ├── heat_cric.png
│   │   ├── si_sports.png
│   │   ├── sports.png
│   │   ├── sports_confusion_matrix.png
│   │   └── sports_data_aug.png
│   └── sports_classifier.ipynb
├── VideoCLassificationwithKeras.pdf
├── example_clips
│   ├── lifting.mp4
│   ├── soccer.mp4
│   └── tennis.mp4
├── from_colab
│   ├── model
│   │   └── trained_model_22sports_50epochs.model
│   ├── output
│   │   ├── lifting_128frames_smoothed.avi
│   │   ├── lifting_1frame.avi
│   │   ├── lifting_22sp_50ep_11frs.avi
│   │   ├── lifting_22sp_50ep_128frs_smooth.avi
│   │   ├── soccer_128frames_smoothed.avi
│   │   ├── tennis_128frames_smoothed.avi
│   │   └── trained_model_22sports_50epochs.pickle
│   ├── predict_video.py
│   ├── pyimage-sports-video-classifier.ipynb-from-colab
│   └── readme.txt
├── model
│   ├── activity.model
│   └── lb.pickle
├── output
├── plot.png
├── predict_video.py
├── readme.txt
├── sports-video-classification.png
└── train.py

9 directories, 31 files


run this as python scripts and not a notebook - FAILED BECAUSE OF 
ValueError: Negative dimension size caused by subtracting 4 from 1 for 'average_pooling2d_1/AvgPool' (op: 'AvgPool') with input shapes: [?,1,1,512].
Don't know why because the python scripts should have just worked
No errors reported on pyimage

So I'll run this on colab - only work with a few sports
badminton
baseball
basketball
cricket
football
formula1
motogp
tennis
weight_lifting

The pyimage example predictions are on weight_lifting, football and tennis

$ python predict_video.py --model model/activity.model 
	--label-bin model/lb.pickle 
	--input example_clips/tennis.mp4 
	--output output/tennis_128frames_smoothened.avi 
	--size 128

ALSO - the fastai libraries work on colab - so worth running the notebook that created the Sports-Type-Classifier dataset

23/7/19 - 

get used to kwargs 

Video classification with Keras and Deep Learning
by Adrian Rosebrock on July 15, 2019 in Deep Learning, Keras, Tutorials
 Python File Icon Click here to download the source code to this post


In this tutorial, you will learn how to perform video classification using Keras, Python, and Deep Learning.

Specifically, you will learn:

The difference between video classification and standard image classification
How to train a Convolutional Neural Network using Keras for image classification
How to take that CNN and then use it for video classification
How to use rolling prediction averaging to reduce “flickering” in results
This tutorial will serve as an introduction to the concept of working with deep learning in a temporal nature, paving the way for when we discuss Long Short-term Memory networks (LSTMs) and eventually human activity recognition.

17/7/2019

