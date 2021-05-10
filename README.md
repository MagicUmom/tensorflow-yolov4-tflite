# Fork From [tensorflow-yolov4-tflite](https://github.com/hunglc007/tensorflow-yolov4-tflite) 2021/05/10
- For AIF 內部學員使用

# tensorflow-yolov4-tflite
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)

YOLOv4, YOLOv4-tiny Implemented in Tensorflow 2.0. 
Convert YOLO v4, YOLOv3, YOLO tiny .weights to .pb, .tflite and trt format for tensorflow, tensorflow lite, tensorRT.

Download yolov4.weights file: https://drive.google.com/open?id=1cewMfusmPjYWbrnuJRuKhPMwRe_b9PaT


# Quick Start

```bash
# 下載 yolov4.weights 權重
# 使用 gdown 下載，如果沒有此套件請使用 pip install gdown
gdown --id 1cewMfusmPjYWbrnuJRuKhPMwRe_b9PaT -O ./data/

# 將 darknet權重 轉換成 tf2的權重
python save_model.py --weights ./data/yolov4.weights --output ./checkpoints/yolov4-416 --input_size 416 --model yolov4

# 使用預測
python detect.py --weights ./checkpoints/yolov4-416 --size 416 --model yolov4 --image=./pred_data --output=./pred_result

```

### Prerequisites
* Tensorflow 2.3.0rc0
* OpenCV 4




### References

  * YOLOv4: Optimal Speed and Accuracy of Object Detection [YOLOv4](https://arxiv.org/abs/2004.10934).
  * [darknet](https://github.com/AlexeyAB/darknet)
  
   My project is inspired by these previous fantastic YOLOv3 implementations:
  * [Yolov3 tensorflow](https://github.com/YunYang1994/tensorflow-yolov3)
  * [Yolov3 tf2](https://github.com/zzh8829/yolov3-tf2)
