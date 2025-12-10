# Statistical parking lot detection using YOLOv8 and clustering
This was prepared as part of a class project tuning various object detection models for detection of empty and occupied parking spots.  My approach was to look at the use of security camera data, where the camera angle is mostly fixed in space and taking images at regular intervals, and how that data could be aggregated to do automated statistical predictions of where parking paces are.

In some parking lots, parking spots are clearly marked with painted lines.  In others, such as the one used here, there are numerous unmarked spots that are used.  In various locations, there may be informal "habits" around parking behaviour that may be understood by considering longer-term observations of the same setting.



## Source datasets used:
  - [PKLot Dataset](https://www.kaggle.com/datasets/ammarnassanalhajali/pklot-dataset) on Kaggle

## Quick links to specific activities:

Most of the content here can be seen in the images and markdown text sections:

  - [YOLO Inference and Clustering](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/plot_bounding_boxes.ipynb) (Recommended), in which a selected camera angle is used to generate parking locations using a pre-trained YOLOv8 model and the [DBSCAN](https://en.wikipedia.org/wiki/DBSCAN) clustering algorithm, and the results visualized to illustrate the process
  
  - [SAM prompt generation](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/cluster_training_data.ipynb), in which the inferred parking spot locations were used as part of a fine-tuning and data-annotation pipeline, to generate training data for a [SAM](https://github.com/facebookresearch/segment-anything) model and to pre-generate bounding boxes for manual data annotation.
  - General data pipeline: 
    - [Loading](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/load_image_data.ipynb), 
    - [Simple EDA and YOLO usage](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/YOLO_sample.ipynb),
    - [Yolo Inference and Clustering](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/plot_bounding_boxes.ipynb),
    - [SAM prompt generation](https://github.com/JohnAllanE/parking-lot-yolo/blob/main/cluster_training_data.ipynb)