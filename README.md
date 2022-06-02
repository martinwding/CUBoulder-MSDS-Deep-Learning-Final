# CUBoulder-MSDS-Deep-Learning-Final
## 1. Project Description
### 1.1 Project Objectives
This project has two main objectives:
1. Build an RNN model that predicts (classifies) whether a customer review about restaurants are positive or negative.
2. Build an unsupervised machine model that extracts key topics/themes from reviews.

<br>

### 1.2 Project Background
In order for a business to stay competitive, it needs to understand its customer feedbacks. What are customers saying about us? Are they happy with our products and services? Where do we need to improve upon? 

One important source of customer feedback is the reviews posted on specialized customer review platforms such as Google Reviews and Tripadvisor reviews. These review sites allow customers to post text reviews as well as a rating (usually 1-5 stars). Companies can take these reviews, segment them based on the rating or simply into postive and negative reviews. Companies can then analyze the negative reviews to understand their shortcomings and focus on the positive reviews to further enhance their competitive position.

However, with the advent of smart devices, more and more people are turning to social media to post their experiences with a brand. These social media posts are highly important (due to word of mouth), but much harder for the companies to efficiently analyze, because:
- there are no ratings (1-5)
- have to manually go through each post and sort them into positive/negative reviews, which is very resource intensive for companies

It would therefore be highly valuable, to train an automatic reviews classifier based on reviews that have a rating (e.g. data from specialized reviews platforms, such as Tripadvisor), and use the classifier to predict whether a social media post about a company (such as a Tweet) is positive or negative. In addition, it would be even more valuable to develop a model that can automatically extract keywords/themes from the reviews, as this will give human analysts even more efficient ways to understand and analyze the data.

<br>

### 1.3 Project Evaluation
Part 1 Classification:

Reviews data tend to have imbalanced data distributions:
- either many negative reviews and complaints vs. positive reviews, or
- an overwhelming proportion of positive reviews/high ratings vs. negative reviews

Therefore, accuracy will not be a suitable evaluation metric, as a naive strategy of always predicting the majority class will give us a (misleadingly) high accuracy.

The classification model results will be evaluated using the F1 score. The F1 score is the harmonic mean of precision and recall and it is calculated as:

$$F1 = 2 * \frac{precision\, * \,recall}{precision\, + \,recall}$$

Where

$$precision = \frac{True \, Positives}{True\, Positives \, + \, False \,Positives}$$

$$recall = \frac{True \,Positives}{True\, Positives \, + \, False \,Negatives}$$

Unlike accuracy, the F1 score does not suffer from class imbalance problems, however it is less interpretable than accuracy.

Part 2 Topic Modelling:

Unlike supervised methods, unsupervised methods don't have a "ground truth" to evaluate against. There are mathematical methods such as various distance metrics that can be use for evaluating topic models, but in this project, we feel that it is more important to apply human logic and judgement. Therefore the topic model will be evaluated on whether it provides meaningful and interpretable results.
