# MAGIC Gamma Telescope – Classification Project

### Overview
This project uses the **MAGIC Gamma Telescope** dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/159/magic+gamma+telescope) to classify high-energy particles detected by a Cherenkov telescope as either **gamma rays (signal)** or **hadrons (background)**.

The goal was to compare select **scikit-learn models** with a **TensorFlow neural network**, and determine which approach achieved the best accuracy and generalization.

---

### Objective
To model a machine learning model capable of accurately identifying gamma events using telescope data, while comparing multiple algorithms to find the most effective approach.

---

### Methods

1. **Data Preprocessing**
   - Loaded and scaled data using `StandardScaler`
   - Split data into **train**, **validation**, and **test** sets
   - Encoded class labels (gamma = 1, hadron = 0)

2. **Modeling Approaches**
   - **Scikit-learn models tested:**  
     - K-Nearest Neighbors (KNN)  
     - Logistical Regression
     - SVM  
   - **TensorFlow Neural Network:**
     - Input: 10 features  
     - Hidden layers with ReLU activation  
     - Dropout layers to prevent overfitting  
     - Output layer with sigmoid activation for binary classification  
     - Optimizer: Adam  
     - Loss: Binary Crossentropy  

3. **Hyperparameter Tuning**
   - Tuned parameters such as:
     - Number of hidden nodes  
     - Dropout probability  
     - Learning rate  
     - Batch size  
   - Selected model with lowest validation loss and highest accuracy.

---

 **Conclusion:**  
After testing multiple configurations, the **TensorFlow neural network** achieved the best overall performance, outperforming all other scikit-learn models in both validation accuracy and stability. For more information view the notebook.
