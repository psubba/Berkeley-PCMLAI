## Sentiment Analysis of Product Reviews

**Author**
Prateek Subba

### Executive summary
The capstone project focuses on sentiment analysis of product reviews using machine learning techniques to help differentiate between positive and negative reviews. This differentiation is crucial for product development and improvement. As part of this Capstone I am implementing and comparing various models, including Naive Bayes, Logistic Regression, Support Vector Machine (SVM), and Random Forest, with two feature extraction techniques (Bag of Words and TF-IDF), to identify the most effective model. Logistic Regression with Bag of Words emerged as the best-performing model, achieving the highest accuracy, precision, recall, and F1-score. This model's ability to effectively identify both positive and negative instances with minimal error provides valuable insights for product enhancement.


### Rationale
Understanding the sentiment behind product reviews is vital for businesses as it directly impacts product development, customer satisfaction, and overall market competitiveness. By accurately analyzing customer feedback, companies can identify strengths and areas for improvement, leading to better products and services that meet customer needs and expectations.

### Research Question
Which machine learning model and feature extraction technique best differentiate between positive and negative product reviews

### Data Source
The dataset available on Kaggle, "Consumer Reviews of Amazon Products" by Datafiniti, which includes over 34,000 consumer reviews for products like the Kindle and Fire TV Stick. The dataset can be accessed here(https://www.kaggle.com/datasets/datafiniti/consumer-reviews-of-amazon-products/data?select=Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv).

### Methodology
- Data Exploratiion and Preprocessing: Cleaning and preparing the review data.
- Feature Extraction: Implementing Bag of Words (BoW) and TF-IDF techniques to transform text data into numerical features.
- Model Implementation: Training four different machine learning models (Naive Bayes, Logistic Regression, SVM, and Random Forest) on the extracted features.
- Performance Evaluation: Comparing models based on accuracy, precision, recall, F1-score, processing time, and confusion matrices.

### Results
I found that Logistic Regression with Bag of Words features provided the best overall performance. It achieved the highest accuracy (0.95) and maintained excellent precision (0.96), recall (0.99), and F1-score (0.97). The model demonstrated a balanced ability to identify both positive and negative instances with minimal error. While Naive Bayes was the fastest in processing time, its performance, especially with TF-IDF, was less balanced. SVM and Random Forest, although accurate, were slower in processing times. Therefore, Logistic Regression with BoW is the most effective model for our dataset.

### Detailed Analysis of Results
The results provided compare the performance of different models using two feature extraction techniques: Bag of Words (BoW) and TF-IDF. Here is the detailed analysis:

#### Bag of Words (BoW):

*Naive Bayes:*
- Accuracy: 0.94
- Precision: 0.96
- Recall: 0.98
- F1-score: 0.97
- Processing Time: 0.01 secs
- Confusion Matrix: [[178, 283], [135, 6217]]

*Logistic Regression:*
- Accuracy: 0.95
- Precision: 0.96
- Recall: 0.99
- F1-score: 0.97
- Processing Time: 0.6 secs
- Confusion Matrix: [[178, 283], [81, 6271]]

*Support Vector Machine (SVM):*
- Accuracy: 0.94
- Precision: 0.94
- Recall: 1.00
- F1-score: 0.97
- Processing Time: 111.17 secs
- Confusion Matrix: [[70, 391], [13, 6339]]

*Random Forest:*
- Accuracy: 0.94
- Precision: 0.94
- Recall: 1.00
- F1-score: 0.97
- Processing Time: 47.11 secs
- Confusion Matrix: [[45, 416], [4, 6348]]


#### TF-IDF:

*Naive Bayes:*
- Accuracy: 0.93
- Precision: 0.93
- Recall: 1.00
- F1-score: 0.96
- Processing Time: 0.01 secs
- Confusion Matrix: [[0, 461], [0, 6352]]

*Logistic Regression:*
- Accuracy: 0.94
- Precision: 0.95
- Recall: 1.00
- F1-score: 0.97
- Processing Time: 0.28 secs
- Confusion Matrix: [[105, 356], [23, 6329]]

*Support Vector Machine (SVM):*
- Accuracy: 0.94
- Precision: 0.94
- Recall: 1.00
- F1-score: 0.97
- Processing Time: 106.74 secs
- Confusion Matrix: [[87, 374], [17, 6335]]

*Random Forest:*
- Accuracy: 0.94
- Precision: 0.94
- Recall: 1.00
- F1-score: 0.97
- Processing Time: 45.8 secs
- Confusion Matrix: [[35, 426], [5, 6347]]

#### Key Observations:

- Accuracy:
Most models achieve an accuracy of around 0.94-0.95. Logistic Regression with BoW features has the highest accuracy at 0.95.

- Precision, Recall, and F1-score:
    For BoW features, Logistic Regression achieves the highest recall (0.99) and F1-score (0.97), making it very effective in identifying positive instances.
    For TF-IDF features, all models have a recall of 1.00, indicating that they correctly identified all positive instances. However, precision and F1-score slightly vary, with Logistic Regression achieving the highest precision (0.95) and F1-score (0.97).

- Processing Time:
    Naive Bayes is the fastest model, with a processing time of 0.01 seconds for both BoW and TF-IDF.
    SVM is the slowest, taking over 100 seconds for both feature extraction methods.
    Logistic Regression and Random Forest have moderate processing times.

- Confusion Matrix:
    Naive Bayes with TF-IDF features fails to identify any negative instances correctly, leading to a very imbalanced confusion matrix.
    Logistic Regression with both BoW and TF-IDF features shows a better balance, though it still struggles with false negatives in some cases.
    SVM and Random Forest also show a good balance but have a few more false positives and false negatives compared to Logistic Regression.

#### Conclusion:
- Best Performing Model: Logistic Regression, especially with BoW features, seems to perform the best overall. It has the highest accuracy, and its precision, recall, and F1-score are very high, indicating it can effectively identify both positive and negative instances with minimal error.
- Feature Extraction Method: Both BoW and TF-IDF are effective, but BoW features slightly outperform TF-IDF features in this dataset, especially with Logistic Regression.
- Processing Time: Naive Bayes is the fastest, but its performance, especially with TF-IDF, is not as balanced as Logistic Regression. SVM and Random Forest take significantly longer to process.

Overall, Logistic Regression with Bag of Words features offers the best balance of accuracy, precision, recall, F1-score, and processing time for this dataset.


### Next steps
- Expand Dataset: Include more diverse product reviews to enhance model generalization.
- Fine-Tune Models: Optimize hyperparameters of the models to further improve performance.
- Aspect-Based Sentiment Analysis: Extend the analysis to identify sentiment towards specific product features, providing more granular insights for product development.
- Incorporate Deep Learning: Explore advanced deep learning techniques like Recurrent Neural Networks (RNN) or Transformers for potentially better performance.


### Jupyter Notebook

- [Sentiment Analysis of Consumer Reviews.ipynb](https://github.com/psubba/Berkeley-PCMLAI/blob/main/Capstone%20Project%2024.1/Sentiment%20Analysis%20of%20Consumer%20Reviews-Final.ipynb)


