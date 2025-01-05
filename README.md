## A Comparative Analysis of Deep Convolutional Networks for Traffic Sign Recognition

This project focuses on comparing the performance of various deep neural network architectures, including proposed CNN, VGG16, ResNet50 and EfficientNetB0, on the German Traffic Sign Recognition Benchmark (GTSRB) dataset. By leveraging state-of-the-art methods and rigorous evaluation, this study aims to contribute to advancements in traffic sign recognition for autonomous systems.

### Dataset
The German Traffic Sign Recognition Benchmark (GTSRB) dataset is a widely used dataset in the field of traffic sign recognition and computer vision. The images were captured under varying real-world conditions such as different lighting, weather, occlusions, and angles. The variety of image conditions make the GTSRB dataset challenging but reliable for developing robust traffic sign recognition systems.

<b>Overview of the Dataset:</b>

<ul>
<li>Single-image, multi-class classification problem</li>
<li>43 Classes</li>
<li>39,209 Training Images</li>
<li>12,630 Testing Images</li>
</ul>
<b>Image Format:</b>
<ul>
<li>The images contain one traffic sign each</li>
<li>Images are stored in PPM format (Portable Pixmap, P6)</li>
<li>Image sizes vary between 15x15 to 250x250 pixels</li>
</ul>

![class distribution](https://github.com/user-attachments/assets/afa1c2f2-5157-47c2-ae49-909dc68911bd)

### Data preprocessing

<ul>
<li><b>Resizing Images:</b> All the images were resized to 32*32*3 pixels.</li>
<li><b>Normalization:</b> Pixel values were scaled to [0, 1]</li>
<li><b>Dataset Splitting:</b> 80% of the dataset was used for training, and the rest 20% was used for validation.</li>
</ul>

### Models Trained
<ul>
<li>Proposed CNN</li>
<li>VGG16</li>
<li>ResNet50</li>
<li>EfficientNetB0</li>
</ul>

### Top layers:
The same top layers were employed for the pre-trained models.
<ul>
<li>BatchNormalization</li>
<li>Flatten</li>
<li>Dense layer with 512 units</li>
<li>Dense layer with 43 units</li>
</ul>

### Find optimal model:
<ul>
<li><b>Fine Tuning: </b> Different layer combinations of the pre-trained models were experimented to find the best model combination for GTSRB dataset.</li>
<li><b>Hyper-parameter Tuning: </b> Different learning rates and Batch sizes were experimented to find the optimal learning rate and batch size combination.</li>
</ul>

### Training Process:
<ul>
<li><b>Optimizer:</b> Adam</li>
<li><b>Loss function:</b> categorical cross-entropy for
multi-class classification).</li>
<li>Early Stopping to prevent overfitting</li>
<li><b>Evaluation Metrics:</b> accuracy / f1-score</li>
</ul>

### Best Model:
<ul>
<li>VGG16</li>
<li>Accuracy: <b>99.06%</b></li>
</ul>

### Files Details:
The files numbering from 1 to 4 are the experimented files where fine-tuning and hyperparameter tuning were applied to figure out the optimal model for the GTSRB dataset.
All the best models were trained for more epochs in the file numbering 5 with name "Final_Code_all_best_models_training.ipynb" where the actual accuracies are stored.

