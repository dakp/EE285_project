# Distracted Driver Detection Based on CNN architectures

This is our solution for the Statefarm Distracted Driver Detection Kaggle competition.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Give examples
```

### Installing

It takes a long time to train the network and extract images from Object detection and skin segmentation module. Hence the different models have already been trained and the weights are saved for running only inference.

There are three possible implementations:
1) Model trained on original dataset
2) Model trained on object detection extracted images and
3) Model trained on skin segmentation extracted images

To only run inference run the iPython notebook Main_inference.ipynb using different pickle files and datasets to load according to the above.


In case you want to run training as well, the following steps need to be performed (Note that generating dataset for training takes long time):
1) After installing various requirements, run the setup.sh script to setup all files correctly.

```
chmod a+x setup.sh
./setup.sh
```
2)
Run the iPython notebook Skin_seg.ipynb to generate the dataset for the skin segmented images.
Run the iPython notebook Darknet.ipynb to generate the dataset for the object detection images.

Run the iPython notebook Main_training.ipynb using different possible datasets as mentioned above.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* The image Classification implementation is based on Transfer learning tutorial in pytorch (https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html).
* The object detection implementation is largely based on the tutorial series on how to implement YOLOv3 from Scratch in PyTorch (https://blog.paperspace.com/how-to-implement-a-yolo-object-detector-in-pytorch/)
* Skin segmentation implementation is based on the paper [Abouelnaga, Y., Eraqi, H.M. and Moustafa, M.N., 2017. Real-time Distracted Driver Posture Classification. arXiv preprint arXiv:1706.09498.]
