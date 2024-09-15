# GST_analytics

**If this notebook does not open then please try to contact me.**
my Mail id : dassaurav4534@gmail.com
my wp number : 8116615954


# Key methodology
**Data oriented approach <br>(recommended by CS professor of Stanford: Andrew Ng)**


<h2>1. Handling Imbalanced Data with SMOTE</h2>
<p>
   The dataset  had an imbalanced target variable (0 and 1). To prevent the classifier from being biased toward the majority class (0), 
   i used <strong>SMOTE (Synthetic Minority Over-sampling Technique)</strong>. SMOTE synthetically generates new instances of the minority class by 
   interpolating between existing minority class instances, helping balance the class distribution. This step was crucial to ensure that the model performs well on both classes.
</p>

<h2>2. Model Selection: MLPClassifier</h2>
<p>
   chose to implement a <strong>Multilayer Perceptron (MLP) Classifier</strong> from sklearn, a neural network-based model capable of learning complex patterns in data. MLP is a robust choice when the relationship between features and the target variable is non-linear.
</p>

<h3>MLP Architecture:</h3>
<ul>
   <li><strong>Hidden Layers:</strong> Two hidden layers with 100 and 50 units respectively, allowing the model to capture complex interactions in the data.</li>
   <li><strong>Activation Function:</strong> 'ReLU' (Rectified Linear Unit), introduces non-linearity and helps the model learn better from the data.</li>
   <li><strong>Solver:</strong> 'Adam', a gradient-based optimizer efficient for large datasets and sparse gradients.</li>
   <li><strong>Alpha:</strong> A small L2 regularization term of 0.0001, helping prevent overfitting by penalizing large weights.</li>
   <li><strong>Learning Rate:</strong> 'Adaptive', meaning the learning rate decreases as training progresses, stabilizing convergence and avoiding overshooting the optimal weights.</li>
</ul>

<h2>3. Training and Validation</h2>
<p>
   After preprocessing the data using SMOTE and configuring the MLPClassifier, you trained the model on the dataset. While training, you ignored potential 
   trade-offs related to training time, focusing purely on maximizing model performance.
</p>
<p>
   The validation was performed on an imbalanced dataset to observe the model's effectiveness in real-world scenarios, where class 0 is more frequent than class 1.
</p>

<h2>4. Evaluation Metrics</h2>
<p>The performance of model was assessed using several key metrics to provide a comprehensive evaluation:</p>
<ul>
   <li><strong>Accuracy:</strong> 0.9557 — The overall correct predictions made by the model.</li>
   <li><strong>Precision:</strong> 0.7251 and <strong>Recall:</strong> 0.8545 — Precision focuses on how many predicted positives were actually positive, while recall measures how many actual positives were correctly predicted.</li>
   <li><strong>F1 Score:</strong> 0.7845 — A balanced metric that combines precision and recall.</li>
   <li><strong>AUC-ROC:</strong> 0.9824 — This high value indicates excellent discrimination between classes.</li>
   <li><strong>Balanced Accuracy:</strong> 0.9104 — This adjusts for class imbalance, showing good performance across both classes.</li>
   <li><strong>Log Loss:</strong> 0.1043 — A low log loss indicates the model is confident in its predictions.</li>
</ul>

<h2>5. Confusion Matrix</h2>
<p>
   The confusion matrix provided a more granular view of your model's performance on the validation set:
</p>
<ul>
   <li><strong>True Negatives:</strong> 229039</li>
   <li><strong>False Positives:</strong> 7995</li>
   <li><strong>False Negatives:</strong> 3590</li>
   <li><strong>True Positives:</strong> 21088</li>
</ul>
<p>
   These values demonstrate that the model has been able to balance the trade-off between false positives and false negatives fairly well, especially given the class imbalance.
</p>

<h2>6. Conclusion</h2>
<p>
   By leveraging SMOTE for data balancing and MLPClassifier for model training, developed a model that effectively handles imbalanced data and delivers strong performance across several key metrics.
</p>
