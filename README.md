# credit-risk-classification

Logistic regression is a statistical method used for binary classification tasks, such as predicting whether an observation belongs to one of two categories. In the context of evaluating loan risk, logistic regression can be a valuable tool for predicting whether a loan is likely to be healthy or high-risk based on various features such as loan size, interest rate, debt-to-income ratio, borrower income, and total debt.

Logistic regression models the probability that a given input belongs to a particular category using the logistic function (also known as the sigmoid function). The logistic function maps any input value to a value between 0 and 1, which represents the probability of the input belonging to the positive class (in this case, high-risk loan). 

Steps taken to predict the loan classification:

1. **Data Preparation**:
   - The dataset was preprocessed, with features like loan size, interest rate, debt-to-income ratio, borrower income, and total debt extracted to form the feature matrix \( X \), and the target variable loan status was separated as \( y \).

2. **Train-Test Split**:
   - The dataset was split into training and testing sets using the `train_test_split` function. This allows the model to be trained on one subset of the data and evaluated on another subset to assess its generalization performance.

3. **Model Training**:
   - A logistic regression model was initialized and fitted to the training data. During this process, the model learns the optimal coefficients to predict the probability of loan default based on the input features.

4. **Model Evaluation**:
   - The trained model was used to predict loan statuses on the test data. These predictions were then compared to the actual loan statuses to generate a confusion matrix and a classification report.
   - The confusion matrix provides a breakdown of true positives, true negatives, false positives, and false negatives.
   - The classification report includes metrics such as accuracy, precision, recall, and F1-score for each class (healthy loan and high-risk loan).

5. **Model Performance**:
   - The reported accuracy of 99% on the test data indicates that the model performs very well overall in predicting loan statuses.
   - Precision, recall, and F1-score provide insights into the model's performance for each class. In this case, the model shows a precision of 1.00 , a recall of 0.99, and F1-score of 1.00 for healthy loans (class 0), indicating that it effectively identifies healthy loans. However, for high-risk loans (class 1), a precision of 0.85, a recall of 0.91, and an F1-score of 0.88 which is good, there is room for improvement in precision and F1-score.

Regarding whether this model can be recommended or not, here are some considerations:

- **High Accuracy**: The high accuracy of 99% on the test data suggests that the model performs well overall.
- **Class Imbalance**: It's important to consider the class distribution in the dataset. If there's a significant class imbalance (i.e., more healthy loans than high-risk loans), accuracy alone may not be the best metric for evaluating model performance. Other metrics like precision, recall, and F1-score provide a more comprehensive understanding, especially in the presence of class imbalance.
- **Continuous Monitoring**: Model performance should be continuously monitored and evaluated over time, especially if the underlying data distribution or business environment changes.

In summary, while the reported accuracy is impressive, further analysis and consideration of other metrics and factors are necessary to determine whether the model can be recommended for deployment in a real-world lending scenario.
