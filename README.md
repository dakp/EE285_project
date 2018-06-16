# Distracted Driver Detection Based on CNN architectures

This is our solution for the Statefarm Distracted Driver Detection Kaggle competition. 
It takes a long time to train the network and extract images from Object detection and skin segmentation module for the full training set. Hence we are using a much smaller dataset having 250 images per class in the training set and 80 images per class in the test set

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 
The following steps will work after git cloning the repository.

### Prerequisites

No packages other than the ones used in class are required 

### Installing

There are three possible implementations:
1) Model trained on original dataset
2) Model trained on object detection extracted images and
3) Model trained on skin segmentation extracted images

To run the demo:
1) Run the setup.sh script to setup all files correctly.

```
chmod a+x setup.sh
./setup.sh
```
Run demo.ipynb for running the demo which takes <1 min. However note that since the training dataset is not large the accuracy will be poor. However we have saved the results of training on the whole dataset in the directory results/. The true results for the whole dataset can be extracted using plot.ipynb which has also been reported in our final report.

2) In case you want to see the output of skin segmentation on the input images run the iPython notebook Skin_seg.ipynb to generate the dataset for the skin segmented images. You need to change the directory according to your requirement.

3) Run the iPython notebook Darknet.ipynb to generate the dataset for the object detection images.

To use the above generated images we can run the iPython notebook demo.ipynb using output directories for the above datasets as mentioned above.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* The image Classification implementation is based on Transfer learning tutorial in pytorch (https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html).
* The object detection implementation is largely based on the tutorial series on how to implement YOLOv3 from Scratch in PyTorch (https://blog.paperspace.com/how-to-implement-a-yolo-object-detector-in-pytorch/)
* Skin segmentation implementation is based on the paper [Abouelnaga, Y., Eraqi, H.M. and Moustafa, M.N., 2017. Real-time Distracted Driver Posture Classification. arXiv preprint arXiv:1706.09498.]
