# Deep-Fake-Detection-Project

🕵️‍♂️ Deepfake Image Detection using Xception.

This project detects whether an image is real or deepfake using a deep learning based binary classification approach.
I used transfer learning with the Xception model, which is effective for image forensics because its depthwise separable convolutions can capture subtle visual artifacts often present in deepfakes ⚙️.

The model leverages ImageNet pre-trained weights to reuse basic visual features like edges and textures. Initially, the Xception layers are frozen to keep learning stable and controlled, not random 🔒.

To reduce overfitting, data augmentation such as rotation, flipping, and zoom is applied, helping the model generalize better 🔄.

A custom classification head with Global Average Pooling, Dense layers, and Dropout is added for better feature learning and regularization 🧠.

The model is trained using binary cross-entropy loss and the Adam optimizer, with Early Stopping and learning rate reduction to maintain training stability 📉.

Finally, a sigmoid output provides a probability score, which is thresholded to classify images as Real or Deepfake ✅❌.
