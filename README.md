# Bean Leaf Lesions Classification

- [Project Structure](#project-structure)
- [Dataset](#dataset)
- [Training](#training)
- [Tools](#tools)

This is a deep learning project where I used a pretrained GoogLeNet model to classify bean leaf diseases. The model is a 22 layer deep convolutional neural network that can tell apart three types of leaves: healthy ones, leaves with angular leaf spot, and leaves with bean rust.

## Project Structure

```
project/
├── Text_Classification_with_Pretrained_Model_of_Confusion_Matrix_or_Prediction.ipynb
├── README.md
└── archive(1)/
    ├── classname.txt
    ├── train.csv
    ├── val.csv
    ├── train/
    │   ├── angular_leaf_spot/
    │   ├── bean_rust/
    │   └── healthy/
    └── val/
        ├── angular_leaf_spot/
        ├── bean_rust/
        └── healthy/
```

## Dataset

I got the dataset from Kaggle, the Bean Leaf Lesions Classification dataset. It has about 1167 images split into training and validation sets.

## Training

For training I did it in two stages. First I froze all the backbone layers and only trained the final fully connected layer. Then I unfroze the last two inception blocks along with the FC layer and fine tuned everything together with a lower learning rate. The final test accuracy came out to around 95 percent.

## Tools

- Python 3.12
- PyTorch & torchvision
- scikit-learn
- Pandas
- Pillow (PIL)
- Matplotlib
- Jupyter Notebook
For training I did it in two stages. First I froze all the backbone layers and only trained the final fully connected layer. Then I unfroze the last two inception blocks along with the FC layer and fine tuned everything together with a lower learning rate. The final test accuracy came out to around 95 percent.

## Project Preview

![Project Preview](image/image.png)
