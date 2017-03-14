# FSRCNN-TensorFlow
TensorFlow implementation of the Fast Super-Resolution Convolutional Neural Network (FSRCNN). This implements two models: FSRCNN which is more accurate but slower and FSRCNN-s which is faster but less accurate. Based on this [project](http://mmlab.ie.cuhk.edu.hk/projects/FSRCNN.html).

## Prerequisites
 * Python 2.7
 * TensorFlow
 * Scipy version > 0.18
 * h5py
 * PIL

## Usage
For training: `python main.py`
<br>
For testing: `python main.py --train False`

To use FSCRNN-s instead of FSCRNN: `python main.py --fast True`

Can specify epochs, learning rate, data directory, etc:
<br>
`python main.py --epochs 10 --learning_rate 0.0001 --data_dir Train`
<br>
Check `main.py` for all the possible flags

Also includes script `expand_data.py` which scales and rotates all the images in the specified training set to expand it

## Result

<br>
Original butterfly image:
<br>
![orig](https://github.com/drakelevy/FSRCNN-Tensorflow/blob/master/result/original.png?raw=true)<br>
Bicubic interpolated image:
<br>
![bicubic](https://github.com/drakelevy/FSRCNN-Tensorflow/blob/master/result/bicubic.png?raw=true)<br>
Super-resolved image:
<br>
![srcnn](https://github.com/drakelevy/FSRCNN-Tensorflow/blob/master/result/fsrcnn.png?raw=true)

## References
* [tegg89/SRCNN-Tensorflow](https://github.com/tegg89/SRCNN-Tensorflow)
<br>
* [liliumao/Tensorflow-srcnn](https://github.com/liliumao/Tensorflow-srcnn) 
<br>
* [carpedm20/DCGAN-tensorflow](https://github.com/carpedm20/DCGAN-tensorflow) 
