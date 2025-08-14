# Classification with Support Vector Machines (SVM) 🤖

This project implements the Support Vector Machine (SVM) algorithm, a powerful and versatile supervised learning model, for a binary classification task. Using the **Breast Cancer Wisconsin Dataset**, the goal is to build a classifier that accurately identifies tumors as malignant or benign.

The project focuses on understanding SVM's core concepts, including margin maximization, the kernel trick, and hyperparameter tuning.

---

## ## Project Workflow

1.  **Data Preparation**: The dataset was loaded and split into training and testing sets. A critical preprocessing step, **feature scaling** (`StandardScaler`), was applied, as SVMs are sensitive to the scale of input features.

2.  **Kernel Comparison**: To understand SVM's versatility, two models were trained and visualized on a 2D subset of the data:
    * A **linear SVM** (`kernel='linear'`), which creates a straight-line decision boundary.
    * A non-linear **RBF kernel SVM** (`kernel='rbf'`), which creates a complex, curved boundary.

3.  **Hyperparameter Tuning**: The `GridSearchCV` utility was used to systematically search for the best combination of the key hyperparameters `C` (regularization) and `gamma` (kernel coefficient) for the RBF kernel.

4.  **Cross-Validation**: `GridSearchCV` inherently uses **5-fold cross-validation** to ensure that the chosen hyperparameters produce a model with robust and reliable performance on unseen data.

5.  **Final Evaluation**: The best estimator found by the grid search was evaluated on the held-out test set to determine its final performance.

---

## ## Key Concepts Learned

* **Maximum Margin Classification**: The core principle of SVMs, which aims to find the hyperplane that creates the largest possible separation, or "margin," between classes. 
* **The Kernel Trick**: Understood how kernels (like RBF) allow SVMs to efficiently solve non-linear problems by mapping data to higher dimensions.
* **Hyperparameter Roles**: Learned the impact of the `C` parameter on the model's complexity and the `gamma` parameter on the flexibility of the decision boundary.
* **Grid Search with Cross-Validation**: Mastered the industry-standard technique for automated and robust hyperparameter tuning.

---

## ## Tools Used

* Python
* Scikit-learn
* NumPy
* Pandas
* Matplotlib
