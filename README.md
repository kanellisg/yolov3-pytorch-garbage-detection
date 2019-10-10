![Demo 2](https://github.com/maartensukel/yolov3-pytorch-garbage-detection/raw/master/demo/garb_demo_2.gif)

# Garbage detection using pytorch and YoloV3
## (Placeholder, work in progress)
PyTorch implementation of a garbage detection model. This repository contains all code for predicting/detecting and evaulating the model.

This repository is a combination of the following repositories:
* https://github.com/zhaoyanglijoey/yolov3
* https://github.com/ultralytics/yolov3

![Demo 1](https://github.com/maartensukel/yolov3-pytorch-garbage-detection/raw/master/demo/garb_demo_1.gif)

Test and prediction code for a garbage object detection

## Installations

To all libaries:
```
pip install -r requirements.txt
```

## Predictions
To run predictions, download the cfg and weights from https://drive.google.com/open?id=1DjeNxdaF7AW3Nu54_3oRw_1SeYJtOvNL and put them in the correct folders. 

Then for example run the following the make a prediction on a file using CPU:

```
python detector_garb.py -i samples/input5_frame281.jpg -o output
```

Or to realtime detect on your webcam using GPU: (CUDA must be installed)
```
python detector_garb.py -i 0 --webcam --video -o ./webcam_output/ --cuda
```


## Test

For testing download data from:
https://drive.google.com/open?id=1DjeNxdaF7AW3Nu54_3oRw_1SeYJtOvNL

To run test execute the following code:

```
python test.py
```

| Class           | Images | Targets | P     | R     | mAP   | F1    |
|-----------------|--------|---------|-------|-------|-------|-------|
| all             | 115    | 579     | 0.242 | 0.941 | 0.875 | 0.376 |
| container_small | 115    | 180     | 0.38  | 0.989 | 0.979 | 0.549 |
| garbage_bag     | 115    | 223     | 0.212 | 0.964 | 0.875 | 0.348 |
| cardboard       | 115    | 176     | 0.122 | 0.869 | 0.77  | 0.231 |



![test_example](https://github.com/maartensukel/yolov3-pytorch-garbage-detection/raw/master/test_batch0.jpg)

## Training
For training a new model look at:

https://github.com/maartensukel/yolov3-garbage-object-detection-training

## TODO:

* Make readme more clear.
* Add inference/prediction speed.
* Clean code. 
* Clean data from personal information. (License plates, faces)
* Collect feedback, code review.
* Make public.
* Write post
