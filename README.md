# robot-cloth-manipulation
the maskrcnn forked from https://github.com/matterport/Mask_RCNN


server use python-socket to connect Fetch(Python2) and Mask R-CNN(Python3) 


## here is my advice:
### if you want to train your dataset:
1）you need build this structure file:
```shell
D:.
	├─cv2_mask
	├─json
	├─labelme_json
	└─pics
```

(here)["https://github.com/ZEUP330/Mask-R-CNN/tree/master/Tip"](on the Tip directory) are so bash file that help you move file or rename json

you can learn that using the labelme to mark your data in here;

and find the [train_corner.ipynb]("NetWork/samples/train_corner.ipynb") (refer to [here](Tip/README.md))