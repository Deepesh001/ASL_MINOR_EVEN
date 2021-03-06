# Sign Language Alphabet Recognition In Real-Time


This project is a sign language alphabet recognizer using Python, openCV and tensorflow for training InceptionV3 model, a convolutional neural network model for classification.

## Requirements

This project uses python 3.6 and the PIP following packages:
* opencv
* tensorflow
* matplotlib
* numpy

### Install using PIP
```
pip3 install -r requirements.txt
```
## Training

To train the model, use the following command (see framework github link for more command options):
```
python3 train.py \
  --bottleneck_dir=logs/bottlenecks \
  --how_many_training_steps=2000 \
  --model_dir=inception \
  --summaries_dir=logs/training_summaries/basic \
  --output_graph=logs/trained_graph.pb \
  --output_labels=logs/trained_labels.txt \
  --image_dir=./dataset
```
  It may take up to four hours to train.

## Classifying

To test classification, use the following command:
```
python3 classify.py path/to/image.jpg
```

## Using webcam (demo)

To use webcam, use the following command:
```
python3 classify_webcam.py
```
Your hand must be inside the rectangle. Keep position to write word, see demo for deletions.
