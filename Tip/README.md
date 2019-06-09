## the frist cell is package
nothing change
## Second is file_path and init_model
nothing change
## Third is Model config

```python
# Number of classes (including background)
NUM_CLASSES = 1 + 4  # background + 4 shapes
```

you should change 4 to the number of your class
## four is Dataset(Reload)
### in load_shapes function:

```python
# Add classes,可通过这种方式扩展多个物体
self.add_class("shapes", 1, "head")
self.add_class("shapes", 2, "quilt")
self.add_class("shapes", 3, "corner")
```

### in load_mask function:

```python
for i in range(len(labels)):
    if labels[i].find("head") != -1:
        labels_form.append("head")
    elif labels[i].find("quilt") != -1:
        labels_form.append("quilt")
    elif labels[i].find("corner") != -1:
        labels_form.append("corner")
```

add the kind name one by one

## five cell:

```python
dataset_root_path=ROOT_DIR+"/new_data/"
img_floder = dataset_root_path + "pic"
# print(img_floder)
mask_floder = dataset_root_path + "cv2_mask"
# yaml_floder = dataset_root_path
imglist = os.listdir(img_floder)
```

dataset_root_path is you dataset path; 

## six and seven is visualization of data and label

check you dataset and label


## eight is load pretrain_model
nothing change

## nine is train:
nothing change
 