# Stanford Machine Learning (Coursera) — Stanford University
### Course Instructor: Andrew Ng
#### Language: Octave / MATLAB
## Stanford Machine Learning (Coursera) — Stanford University
**Course Instructor:** Andrew Ng  
**Language:** Octave / MATLAB
Welcome to this repository containing the complete, verified solutions for the **Stanford Machine Learning Course** taught by **Andrew Ng** on Coursera. This course provides a comprehensive introduction to machine learning, datamining, and statistical pattern recognition.
This repository serves as a showcase of core machine learning algorithms implemented **from scratch** using Octave/MATLAB. Rather than using black-box libraries, every algorithm (from gradient descent to backpropagation and collaborative filtering) was coded from mathematical formulas to build a deep, first-principles understanding of the underlying theory.
---
## Repository Structure
The project is organized into 8 programming exercises, each targeting specific machine learning algorithms and real-world applications:
```bash
Machine-Learning-master/
├── Machine-Learning-master/
│   ├── ex1/     # Linear Regression
│   ├── ex2/     # Logistic Regression & Regularization
│   ├── ex3/     # Multi-class Classification & Neural Networks (Representation)
│   ├── ex4/     # Neural Network Learning (Backpropagation)
│   ├── ex5/     # Regularized Linear Regression & Bias vs. Variance Diagnostics
│   ├── ex6/     # Support Vector Machines (SVMs) & Spam Classifier
│   ├── ex7/     # K-Means Clustering & Principal Component Analysis (PCA)
│   ├── ex8/     # Anomaly Detection & Recommender Systems
│   └── octave.pdf # Reference documentation for Octave
└── README.md    # Repository Documentation (This file)
```
---
## Key Concepts & Skills Learned
Through this project, the following theoretical and practical machine learning concepts were mastered:
*   **Supervised Learning:**
    *   Cost functions, gradient descent optimization, and learning rate adjustment.
    *   Feature scaling, normalization, and normal equations.
    *   Classification using Sigmoid functions, decision boundaries, and regularization to prevent overfitting.
    *   Multi-class classification using the One-vs-All approach.
    *   Neural Network representation, forward propagation, and backpropagation for parameter learning.
*   **Model Diagnostics & Debugging:**
    *   Identifying Underfitting (High Bias) and Overfitting (High Variance).
    *   Plotting learning curves to evaluate model performance over training sizes.
    *   Using cross-validation sets to select optimal hyperparameters (e.g., regularization parameter $\lambda$, SVM parameters $C$ and $\sigma$).
*   **Unsupervised Learning:**
    *   Centroid assignment, optimization objective, and K-Means for vector quantization/image compression.
    *   Dimensionality reduction using Principal Component Analysis (PCA) to project high-dimensional data onto lower-dimensional subspaces while retaining variance.
*   **Specialized Applications:**
    *   Email text processing, stemming, feature extraction, and SVM training for Spam Classification.
    *   Anomaly detection using multivariate Gaussian distribution models.
    *   Recommender Systems using Collaborative Filtering and low-rank matrix factorization.
---
## Detailed Exercise & Project Breakdown
### Exercise 1: Linear Regression
*   **Real-world Problems Solved:**
    1.  **Food Truck Profit Prediction:** Predict profits for a franchise based on city population (univariate linear regression).
    2.  **Housing Price Prediction:** Predict house sale prices based on square footage and number of bedrooms (multivariate linear regression).
*   **Core Implementations:**
    *   [warmUpExercise.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/warmUpExercise.m) - Warm-up function returning an identity matrix.
    *   [plotData.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/plotData.m) - Visualization of 2D data.
    *   [computeCost.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/computeCost.m) & [computeCostMulti.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/computeCostMulti.m) - Calculated the cost function $J(\theta)$ for single and multiple variable regression.
    *   [gradientDescent.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/gradientDescent.m) & [gradientDescentMulti.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/gradientDescentMulti.m) - Parameter optimization via gradient descent.
    *   [featureNormalize.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/featureNormalize.m) - Normalized features to ensure equal convergence scale.
    *   [normalEqn.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex1/normalEqn.m) - Direct closed-form analytical solution of $\theta$.
### Exercise 2: Logistic Regression & Regularization
*   **Real-world Problems Solved:**
    1.  **University Admission Predictor:** Estimate a student's admission probability based on two exam scores (linear decision boundary).
    2.  **Microchip Quality Assurance:** Classify fabricated microchips as pass or fail based on QA test results (non-linear circular decision boundary).
*   **Core Implementations:**
    *   [sigmoid.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex2/sigmoid.m) - Vectorized sigmoid activation function.
    *   [costFunction.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex2/costFunction.m) & [costFunctionReg.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex2/costFunctionReg.m) - Regularized cost and gradient calculations.
    *   [predict.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex2/predict.m) - Predict class labels (0 or 1) based on a threshold.
    *   [mapFeature.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex2/mapFeature.m) - Mapped features into polynomial terms up to the 6th degree to fit non-linear boundaries.
### Exercise 3: Multi-class Classification & Neural Network Representation
*   **Real-world Problems Solved:**
    *   **Handwritten Digit Recognition:** Classify image scans of digits (0 to 9) using two different models: (a) vectorized One-vs-All logistic regression, and (b) a pre-trained 3-layer Feedforward Neural Network.
*   **Core Implementations:**
    *   [lrCostFunction.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex3/lrCostFunction.m) - Vectorized logistic regression cost function.
    *   [oneVsAll.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex3/oneVsAll.m) - Trained multiple classifiers for the $K$-class classification problem.
    *   [predictOneVsAll.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex3/predictOneVsAll.m) - Predicted class labels using the trained One-vs-All model.
    *   [predict.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex3/predict.m) - Forward propagation algorithm for neural network classification.
### Exercise 4: Neural Network Learning
*   **Real-world Problems Solved:**
    *   **Neural Network Training from Scratch:** Train a neural network to recognize handwritten digits by writing the complete backpropagation algorithm.
*   **Core Implementations:**
    *   [sigmoidGradient.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex4/sigmoidGradient.m) - Computes the derivative of the sigmoid function.
    *   [randInitializeWeights.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex4/randInitializeWeights.m) - Randomly initializes weights to break symmetry.
    *   [nnCostFunction.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex4/nnCostFunction.m) - Implemented neural network cost function, forward propagation to compute activations, backpropagation to compute gradients, and parameter regularization.
    *   [checkNNGradients.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex4/checkNNGradients.m) & [computeNumericalGradient.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex4/computeNumericalGradient.m) - Gradient checking using numerical finite differences to verify correctness of the analytical backpropagation gradients.
### Exercise 5: Regularized Linear Regression & Bias vs. Variance
*   **Real-world Problems Solved:**
    *   **Water Dam Level Forecasting:** Diagnose bias/variance issues when training regularized linear regression to predict the volume of water flowing out of a dam based on the change in the water level.
*   **Core Implementations:**
    *   [linearRegCostFunction.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex5/linearRegCostFunction.m) - Regularized linear regression cost and gradient.
    *   [learningCurve.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex5/learningCurve.m) - Plotted training cost and cross-validation cost against training set size to diagnose model errors (high bias or variance).
    *   [polyFeatures.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex5/polyFeatures.m) - Mapped 1D inputs to higher-degree polynomials.
    *   [validationCurve.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex5/validationCurve.m) - Evaluated model performance across a range of regularization parameters ($\lambda$) on the cross-validation set to choose the best hyperparameter.
### Exercise 6: Support Vector Machines (SVMs) & Spam Classifier
*   **Real-world Problems Solved:**
    1.  **Gaussian SVM Boundary Plotter:** Solve highly complex non-linear boundaries using an SVM with a Radial Basis Function (RBF) kernel.
    2.  **Email Spam Filter:** Preprocess raw emails and train an SVM to classify them as spam or non-spam.
*   **Core Implementations:**
    *   [gaussianKernel.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex6/gaussianKernel.m) - Radial Basis Function kernel computation between two vectors.
    *   [dataset3Params.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex6/dataset3Params.m) - Grid search helper to select optimal values of cost $C$ and kernel bandwidth $\sigma$.
    *   [processEmail.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex6/processEmail.m) - Preprocesses email body text: lowercasing, HTML tag stripping, normalization of numbers/URLs/email addresses/dollar signs, word stemming using Porter Stemmer, and mapping to a vocabulary list.
    *   [emailFeatures.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex6/emailFeatures.m) - Converts preprocessed email indices into a binary feature vector indicating presence or absence of words in the vocabulary.
### Exercise 7: K-Means Clustering & Principal Component Analysis (PCA)
*   **Real-world Problems Solved:**
    1.  **Image Compression:** Compress the colors of a 24-bit RGB image down to 16 colors by running K-Means clustering on the pixel RGB channels (color quantization).
    2.  **Eigenface Visualization & Compression:** Run PCA on a dataset of human face images, find the primary facial characteristics (eigenfaces), and compress/reconstruct the faces using a lower-dimensional projection.
*   **Core Implementations:**
    *   [findClosestCentroids.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/findClosestCentroids.m) - Assigned each training example to its nearest cluster centroid.
    *   [computeCentroids.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/computeCentroids.m) - Updated centroids by computing the mean of all points assigned to them.
    *   [kMeansInitCentroids.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/kMeansInitCentroids.m) - Initialized K-Means centroids randomly using data samples.
    *   [pca.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/pca.m) - Computes covariance matrix and runs Singular Value Decomposition (SVD) to find principal components.
    *   [projectData.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/projectData.m) & [recoverData.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex7/recoverData.m) - Projected data to lower dimension and reconstructed it back.
### Exercise 8: Anomaly Detection & Recommender Systems
*   **Real-world Problems Solved:**
    1.  **Server Health Monitor (Anomaly Detection):** Detect abnormal server behavior (throughput, latency) using a Gaussian distribution model to identify anomalies.
    2.  **Movie Recommendation Engine:** Predict ratings for unrated movies for a specific user and recommend the highest-scoring movies using collaborative filtering.
*   **Core Implementations:**
    *   [estimateGaussian.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex8/estimateGaussian.m) - Calculates the mean ($\mu$) and variance ($\sigma^2$) vectors of features.
    *   [selectThreshold.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex8/selectThreshold.m) - Uses cross-validation to select the optimal threshold $\epsilon$ for classification by maximizing the $F_1$ score.
    *   [cofiCostFunc.m](file:///c:/Users/Malvern/Desktop/Malvern/2026%20Pojects/Softwares/Machine-Learning-master/Machine-Learning-master/ex8/cofiCostFunc.m) - Implemented the Collaborative Filtering cost function and gradients, including regularization, for low-rank matrix factorization.
---
## Execution Instructions
### Prerequisites
You need to install either **GNU Octave** (recommended and free) or **MATLAB**.
*   **Octave Installation:**
    *   *Windows/macOS/Linux:* Download from the official website [GNU Octave Download](https://www.gnu.org/software/octave/download.html).
### Running an Exercise
1. Open Octave or MATLAB.
2. Set the working directory to the target exercise folder (e.g., `ex1`, `ex2`, etc.).
3. Run the primary script for that exercise in the command window.
   For example, to run Exercise 1:
   ```octave
   cd ex1
   ex1
   ```
4. This will run the linear regression pipeline step-by-step, plotting the dataset and printing cost values at each epoch.
### Testing/Submitting
Each exercise includes a `submit.m` script that originally submitted code blocks to the Coursera server for automated grading:
```octave
submit
```
---
## Learning Outcomes & Reflection
This course represents a significant milestone in engineering capabilities:
1.  **Mathematical Fluency:** Translating complex matrix equations, cost functions, gradients, and regularization factors directly into clean, vectorized, multi-dimensional array operations in Octave/MATLAB.
2.  **Feature Engineering:** Understood how to prepare raw data for machine learning models (e.g., mapping polynomial features, normalization, stemming and tokenizing natural text).
3.  **Model Diagnostics Mastery:** Developing the intuition to know how to fix a model when it fails to generalize (increasing regularization vs. adding features, tracking training/test curves).
4.  **No-Library Implementation:** Implementing algorithms manually forces one to master the math and logic behind modern ML libraries like Scikit-Learn, PyTorch, and TensorFlow, providing an invaluable foundation for senior ML engineering.
