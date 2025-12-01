# Client-Reviews-Classification-
The core goal of project is to create a predictive model that reads customer messages and accurately assigns each one to the correct subject category.

## The steps of the project:

- Data Preparation: cleaning and transforming the raw text data by tokenization and stop word removal.

- Feature Engineering: converting cleaned text into a numerical format using Term Frequency-Inverse Document Frequency (TF-IDF) vectorization.

- Model Training: Logistic Regression or Random Forest models are trained and compared to find the best predictor.

- Performance Evaluation: The models are tested using performance metrics like the confusion matrix, precision, recall, and F1-score to measure their reliability.


### Business Insight Extraction: 
Which model performs best?
Logistic Classification and Random Forest models were built. All 2 models performed equal well with accuracy = 1, what signal about model overfitting.
Why might one model outperform the others?
One model can outperform other because of different facts. Data size, outliers, noise can make one model perform better, and another model – worth.
Which class is hardest for the model?
In our case, model predicted very well all categories.
Which categories should the support team allocate more resources to?
According to categories distribution support team should allocate more resources to Return/Refund Requests category since this category contains the most amount of messages from clients.
What operational improvements can be made based on the trends?
There are no trends in our case since our data do not contain data series. Based on category distribution, next the most popular category (after General Inquiry is Delivery Issue. Consequently, we can conclude that company should improve delivery quality, reduce delays.
