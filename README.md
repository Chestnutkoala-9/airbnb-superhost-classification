# Airbnb Superhost Classification Project

## Motivation

The Superhost program at Airbnb offers hosts increased visibility, earning potential, and exclusive rewards. To achieve Superhost status, hosts must meet certain requirements, including maintaining a 4.8+ overall rating, hosting a minimum number of stays, maintaining a low cancellation rate, and providing timely responses to guest inquiries. While these criteria aim to ensure a high-quality experience for guests, it is important to consider Airbnb's original mission of promoting diverse and authentic travel experiences.

As stated in Airbnb's 10K report, the platform aims to provide travelers with the opportunity to stay in local neighborhoods, have authentic experiences, and live like locals in cities around the world. However, the current Superhost criteria may inadvertently favor professional management teams who have the resources to meet the strict requirements, such as promptly responding to messages, managing multiple properties, and maintaining high levels of cleanliness and service. This emphasis on meeting strict criteria may hinder the growth of individual hosts who offer unique and personalized experiences.

This project aims to explore the implications of the Superhost program and understand its impact on the diversity and authenticity of listings on the Airbnb platform, based on various features such as listing descriptions, customer reviews, and additional host characteristics. The classification models used include Naive Bayes, Logistic Regression, and Random Forest.

## Project Structure

The [Airbnb_Superhost.ipynb](https://github.com/Chestnutkoala-9/airbnb-superhost-classification/blob/main/Airbnb_Superhost.ipynb) contains Jupyter notebooks used for data preprocessing, feature engineering, and model training.

## Dataset
The dataset used for this project includes the following files:
- listings-details.csv: Contains information about Airbnb listings, including listing descriptions and host characteristics.
- reviews.csv: Contains customer reviews for the listings.

They can be found in [InsideAirbnb](http://insideairbnb.com/).

## Text Preprocess models
- TD-IDF matrix 
- Word Embeddings: Word2Vec

The traditional TF-IDF only considers individual word tokens and may not capture the sentiment or meaning of multi-word expressions. For example, if the customer writes "not clean," TF-IDF matrix cannot distinguish this comment with "clean". Therefore, I tried Word2Vec, which can can learn to encode semantic relationships between words, including capturing the sentiment and meaning of multi-word expressions.

## Classification Results and Implications

Among the classifiers used, including Random Forest, Logistic Regression, Naive Bayes, and K-means Clustering, the top-performing model was Logistic Regression with an accuracy of 71.2% and an F1-score of 0.641. This suggests that the features we incorporated, such as textual descriptions, numerical attributes, and customer reviews, can provide valuable insights for distinguishing Superhost listings from others.

The classification results imply that the Superhost program may not be solely determined by textual and numerical factors, but rather by a combination of various aspects, including customer satisfaction, host responsiveness, and overall experience. It raises questions about the fairness and effectiveness of the Superhost program in accurately recognizing exceptional hosts.

Furthermore, the ranking of the classifiers based on their performance indicates the varying effectiveness of different models in capturing the underlying patterns and characteristics of Superhost listings. This highlights the importance of choosing an appropriate classifier based on the specific problem and dataset. It also emphasizes the need for further research and exploration to gain a deeper understanding of the factors influencing Superhost recognition and the implications for both hosts and guests on the Airbnb platform.

## Future Improvements

In order to further improve the classification accuracy, one potential avenue to explore is the use of n-grams. Currently, the classification models primarily rely on individual words for prediction. By incorporating n-grams, which are sequences of adjacent words, we can capture more contextual information and potentially enhance the model's understanding of the text. 
