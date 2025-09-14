# water_potablity_monitoring_model
1. Data Loading & Preprocessing

The dataset water_potability.csv is loaded with pandas.

Features (X) are separated from the target label (y = Potability).

Missing values are handled using SimpleImputer (most frequent strategy).

Feature scaling is performed using StandardScaler for normalization.

2. Machine Learning Models

Several models are trained and compared:

Logistic Regression – A baseline classification model.

Decision Tree Classifier – Used with entropy and limited depth.

Random Forest Classifier – Achieves the best accuracy (~70%).

The feature importance from the Random Forest is extracted to identify significant parameters (like pH, Sulfate, Hardness, and Solids).

3. Prediction on Custom Input

The trained Random Forest model is used to predict potability of custom water samples (with given pH, Hardness, Solids, Sulfate values).

Output: "Water is Potable" or "Water is not Potable".

4. Principal Component Analysis (PCA)

PCA is applied for dimensionality reduction.

Top contributing features are identified (e.g., Turbidity, Solids, Conductivity).

ML models are re-run on reduced features but accuracy drops.

5. Neural Network (Deep Learning)

A simple feed-forward Keras Sequential Model is built:

Input Layer → Dense(64, ReLU) → Dense(32, ReLU) → Dense(1, Sigmoid).

Trained with Adam optimizer, binary crossentropy loss.

Achieves a competitive accuracy (~similar to Random Forest).

6. Best Model

Random Forest with full feature set performs best with ~70% accuracy.
