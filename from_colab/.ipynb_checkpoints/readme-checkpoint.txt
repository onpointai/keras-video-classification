Train model on colab and download model and pickle file
and use predict.py - works a charm! 29/7/2019


Having problems with 
from keras.models import model_from_json
model_arch='./output/model_architecture_5epochs.json'
model_weights='./output/trained_model_weights_5epochs.h5'
model_lb = './output/trained_model_5epochs.pickle'
new_model = './model/trained_model_5epochs.model'
with open(model_arch,'r') as f:
    loaded_model=model_from_json(f.read())

data_format issue because of keras/tensorflow version issue
NOTE: USED fro training on google colab
keras version  2.2.4
tensorflow version  1.14.0

so use the created .model file (500mb)

should be able to run the adrians predict_video.py script directly


cd /Users/dexterdsilva/Documents/Developer/MachineLearning/pyimage/keras-video-classification/from_colab
source activate dl1 

python predict_video.py --model model/trained_model_5epochs.model \
	--label-bin output/trained_model_5epochs.pickle \
	--input ../example_clips/lifting.mp4 \
	--output ./output/lifting_1frame.avi \
	--size 1

python predict_video.py --model model/trained_model_5epochs.model \
	--label-bin output/trained_model_5epochs.pickle \
	--input ../example_clips/lifting.mp4 \
	--output ./output/lifting_128frames_smoothed.avi \
	--size 128

python predict_video.py --model model/trained_model_22sports_50epochs.model \
--label-bin output/trained_model_22sports_50epochs.pickle \
--input ../example_clips/lifting.mp4 \
--output ./output/lifting_22sp_50ep_128frs_smooth.avi  \
--size 128

python predict_video.py --model model/trained_model_22sports_50epochs.model \
--label-bin output/trained_model_22sports_50epochs.pickle \
--input ../example_clips/lifting.mp4 \
--output ./output/lifting_22sp_50ep_1frame.avi  \
--size 11


Need to run this a python script 


Created a similar directory structure to colab

26/July/2019