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

Change the data volume location by changing `$DATADIR` in `config_DGX1.sh`.



