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
Deployment Scenario
Ticketing Platform Integration
Integrating the model into a ticketing platform focuses on automatically tagging incoming tickets as they are created.
• Trigger: An email, chat message, or web form submission creates a new ticket.
• Process:
1. The model loads the saved vectorizer and model into memory.
2. Raw text is transformed into features using vectorizer.transform().
3. model.predict() returns the message's category (e.g., "Payment Issue").
• Action: The ticketing system automatically sets the category field on the new ticket, saving the agent time and ensuring it appears in the correct queue instantly.
---------------------------------------------------------------------------------------
The API provides external services (like chatbots) with real-time classification results.
• Setup: A web server loads the saved vectorizer and model once at startup.
• Request: A client sends the raw text message via an HTTP POST request.
• Processing: The server transforms the text using vectorizer.transform(), predicts the class using model.predict(), and converts the numerical result back to a readable category string using the LabelEncoder mapping .
• Response: The API sends back a JSON object containing the classified category and confidence score, enabling immediate action or routing by the client application.
--------------------------------------------------------------------------------------
Automated Routing to Departments
Automated routing uses the model's prediction to instantly direct customer messages, enhancing efficiency.
• Mapping: A configuration map links predicted categories to specific teams (e.g., "Delivery Issue").
• Routing Logic: The system uses this map to automatically assign the ticket or message to the correct team's queue immediately after prediction.
