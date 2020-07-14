# COVID19 Classification Prediction

The Kaggle dataset is provdided by Hospital Sírio-Libanês in Brazil. It contains patient vitals, blood results, demographics, etc.

My goal was to develop a model that can predict if a given patient will be admitted to the ICU, given the patient data and whether or not they were admitted.

I need to clean the data (a lot was missing), which I accomplished using scikit-learn's SimpleImputer with the mean strategy (filling missing values with the column mean).

For selecting features, I looked for weak or better linear correlations with the patient's ICU admission classification to select ~44 features from the total 231 columns.

Finally, I used fitted a Logistic Regression model on the data, which was then evaluated with a train test split. During evaluation, I also tried using SMOTE to synthesize more positive results to get a more balanced model. The "final" model had an overall accuracy of 87%, Weight F1 score average of 87%, and 75% recall of positive ICU Admission cases.

Further evaluation metrics, as well as visualizations for evaluation and exploratory analysis are also in the notebook.
