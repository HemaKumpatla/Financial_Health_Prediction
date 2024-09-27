# Financial-Health-Prediction-and-Feature-Importance-Analysis-for-Enterprises
# Bankruptcy Prediction
## Version 1:
1. Used all features of the data, i.e., 96.
2. Conducted data exploration, cleaning, and preprocessing.
3. Trained various classification models (Logistic Regression, Random Forest, Decision Tree, Gradient Boosting) with high accuracy but low precision and recall due to class imbalance.
4. Best model is Gradient Boosting classifier with accuracy 0.97 
## Version 2:
1. Addressed class imbalance using random oversampling (ROS).
2. Achieved better evaluation metrics.
3. Best model is still GBC with accuracy 0.97 but with improved precision and recall scores.

## Version 3:
1. Train a Random Forest Classifier (RFC).
2. Performed feature importance analysis and selected the top 20 important features (Feature Selection Method 1).
3. Re-trained models with the selected features and achieved good results.
4. GBC performed well with accuracy 0.96 and excellent precision and recall scores.
5. F1 scores for both the classes of tharget variable is 0.96
6. Then, we considered features with a correlation > 0.7 (Feature Selection Method 2).
7. This reduced the feature set to 51 features.
8. Trained models with this reduced feature set and achieved good results.

## Version 4:
1. Added data visualization using Matplotlib and Seaborn.
2. Conducted exploratory data analysis (EDA).
3. Analyzed the top 5 positively and negatively correlated features with the target variable(Bankrupt?).
4. Performed anomaly detection using IQR (interquartile range).
5. Trained models with the top 20 important features from Feature Importance Method 1
6. GBC worked best with 0.97 accuracy and 0.96 f1-score.
7. Saved and deployed GBC model using Streamlit.
8. Performed K-means clustering and trained models with it.
9. The Decision Tree Classifier (DTC) performed the best with 0.97 accuracy and 0.97 f1-score.
10. Saved and deployed DTC model using Streamlit.
11. Compared all the models based on their accuracies and f1-scores.

## Version 5:
1. Used Principal Component Analysis (PCA) to select the top 10 features.
2. We trained the models with these reduced features and achieved good results.
3. Decision tree classifier worked best with 0.98 accuracy and 0.98 f1-score.

## How to Use the Streamlit App

Running the Streamlit app locally is straightforward. Follow these steps:

1. **Clone this repository:**

          git clone https://github.com/HarithBangaru/Financial-Health-Prediction-and-Feature-Importance-Analysis-for-Enterprises.git
   
          cd Financial-Health-Prediction-and-Feature-Importance-Analysis-for-Enterprises

3. **Install the required Python packages:**
 
           pip install -r requirements.txt

4. **Run the Streamlit app:**

            streamlit run app.py

5. **Access the application:**

      Open your web browser and navigate to http://localhost:8501 to start using the application.

## Model Highlights

### Gradient Boosting Classifier

- **Algorithm Used**: Gradient Boosting Classifier

- **Model Accuracy**: Achieved high accuracy of 0.97 in Version 1.
  
- **Precision and Recall**: Initially faced challenges with low precision and recall due to class imbalance.
  
- **Class Imbalance Handling**: In Version 2, class imbalance was addressed using random oversampling (ROS).
  
- **Improved Metrics**: Achieved better evaluation metrics in Version 2, with improved precision and recall scores.
  
- **Feature Selection**: In Version 3 and Version 4, feature importance analysis was performed, and the top 20 important features were selected.
  
- **Top Features**: Notable features include 'Net worth/Assets,' 'Debt ratio %,' and 'Equity to Liability.'
  
- **Real-time Prediction**: The Gradient Boosting model was deployed using Streamlit for real-time financial health prediction through GBC.pkl file in Version 4.
  

### Decision Tree Classifier

- **Algorithm Used**: Decision Tree Classifier
  
- **Model Accuracy**: Achieved high accuracy of 0.97 in Version 4
  
- **Features**: Utilized features such as 'Net worth/Assets,' 'Persistent EPS in the Last Four Seasons,' and 'Debt ratio %.'
  
- **IQR Anomaly Detection**: Employed IQR (Interquartile Range) for anomaly detection in data preprocessing.
  
- **Precision and Recall**: Demonstrated strong precision and recall scores.

- **Real-time Prediction**: Deployed the Decision Tree model for real-time financial health prediction through DTC.pkl file in Version 4.

For more details on model performance, please refer to - [Version 4](Bankruptcy%20prediction%20version4.ipynb) in this README.


