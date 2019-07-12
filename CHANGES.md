# Changes required to make NVIDIA mask-rcnn run

Change file locations in `download_dataset.sh`

```
#wget https://s3-us-west-2.amazonaws.com/detectron/coco/coco_annotations_minival.tgz
wget https://dl.fbaipublicfiles.com/detectron/coco/coco_annotations_minival.tgz
```

Also change file locations in `download_weights.sh`.

```
#wget https://s3-us-west-2.amazonaws.com/detectron/ImageNetPretrained/MSRA/R-50.pkl
wget https://dl.fbaipublicfiles.com/detectron/ImageNetPretrained/MSRA/R-50.pkl
```

### Data volume

The instruction `./caffe2/extract_dataset.sh` refers to a script that doesn't exist.

Trying training with the standard COCO layout we use in github.com/armandmcqueen/tensorpack-mask-rcnn.

Plus putting `R50.pkl` that we downloaded into a `models/` folder 

```
~/data/
    train2017/
    val2017/
    annotations/
    models/
```


Plus putting `R50.pkl` that we downloaded into a `models/` folder 


