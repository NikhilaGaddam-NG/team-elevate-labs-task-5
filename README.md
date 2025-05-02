
 Decision Trees and Random Forests - Heart Disease Prediction

 Objective
The objective of this project is to learn and apply tree-based models — Decision Trees and Random Forests — for classification tasks using the heart disease dataset.

 Dataset
The dataset used in this project is `heart.csv`, which contains various medical attributes and a target variable indicating the presence of heart disease.

Tools Used
- Python
- Scikit-learn
- Matplotlib, Seaborn
- Graphviz (for Decision Tree visualization)

 Project Steps

1. Train a Decision Tree Classifier
A Decision Tree classifier was trained using default parameters. The resulting tree was visualized using `matplotlib`.

 2. Analyze Overfitting and Control Tree Depth
To prevent overfitting, the tree depth was limited (`max_depth=4`). This significantly improved generalization on test data.

- Accuracy with max_depth=4: `0.84`

 3. Train a Random Forest and Compare Accuracy
A Random Forest classifier with 100 estimators was trained and compared with the Decision Tree.

- Random Forest Accuracy: `0.89`

 4. Feature Importances
Feature importances were calculated using the Random Forest model and plotted using a bar graph. The most important features contributing to the prediction included:
- `cp` (chest pain type)
- `thalach` (maximum heart rate)
- `exang` (exercise-induced angina)

 5. Cross-validation
5-fold cross-validation was used to evaluate the robustness of both models.

- Cross-validation Accuracy (Decision Tree, max_depth=4): `0.82`
- Cross-validation Accuracy (Random Forest): `0.87`



Classification Report (Random Forest)
              precision    recall  f1-score   support

           0       0.88      0.88      0.88        41
           1       0.90      0.90      0.90        50

    accuracy                           0.89        91
   macro avg       0.89      0.89      0.89        91
weighted avg       0.89      0.89      0.89        91
```



## Conclusion
- **Decision Trees** are easy to interpret and visualize but can overfit if not properly constrained.
- **Random Forests** provide better accuracy and robustness by averaging over many trees.
- Feature importance and cross-validation help in understanding and validating model performance.

---

## How to Run
1. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```

2. Run the Python script:
   ```bash
   python heart_disease_prediction.py
   ```

3. Ensure `heart.csv` is in the same directory as the script.

---
