# Emotion Analysis using K-Means


### Introduction
In this report, I will present the
methodology, results, and insights garnered
from exploring emotion recognition in K-Means clustering for
pattern discovery. Through hands-on
experimentation K-Means clustering, I aimed to grasp
the intricacies of these method in analyzing
and interpreting textual data. This endeavor
provided valuable insights into the
application of machine learning algorithms
for emotion analysis and enhanced my
proficiency in NLP techniques.

### Data Preparation
#### Data loading
Upon receiving the dataset, it was provided
in a compressed .gz format. After extraction,
I discovered that the dataset was structured
as .json files. To streamline the data for
analysis, I opted to convert these files into
.csv format. This process ensured that the
data was in a more accessible and
standardized form for further exploration
and preprocessing.

![Image1](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/26f6f99b-04cc-41f5-9c7e-49e25c69c111)

#### Preprocessing
During preprocessing, I tokenized the text to
individual words, converted it to lowercase
for consistency, removed stop words, and
eliminated special characters. I also
lemmatized the words to normalize them
and added a new column with preprocessed
text. These steps improved data quality for
subsequent analysis and modeling.

![Image2](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/3ef3e75e-b9bf-421a-a89b-22db401474bf)


#### Feature Transformation
Finally, I transformed the text into numerical
representations using TF-IDF. This method
calculates the importance of each word in a
document relative to a corpus, helping to
capture the significance of words in the
dataset. TF-IDF conversion enabled the text
data to be effectively utilized for machine
learning algorithm such as
K-Means clustering.

![Image3](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/243c493a-c5ee-43a3-92f8-a8f470ce1441)


### K-Means Clustering
#### Algorithm Implementation
In the implementation of K-Means
clustering, I created a separate Jupyter
notebook to streamline the process.
Combining all three dataframe files into one
facilitated easier implementation. I
initialized the KMeans algorithm with the
random number of clusters. Initially, when
attempting to determine the optimal number
of clusters using the elbow method, I
encountered challenges. As a solution, I
combined additional features with the
TF-IDF matrix to obtain a more informative
feature space. The combined features,
including the TF-IDF matrix and additional
metadata features, were used to fit the
KMeans model.

![Image4](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/43917b19-2ff3-4378-90cb-56b82c54eaba)


#### Optimal Clusters
To find the best number of clusters for
K-Means, I used two methods: the elbow
method and the silhouette method. The
elbow method looks for the point where the
rate of inertia decreases slows down,
suggesting an optimal cluster count. The
silhouette method computes scores
indicating how well each data point fits its
assigned cluster. Higher scores imply better
clustering. I found the optimal cluster count
to be 6 using both methods.


![Image 5](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/4d3e6ca2-0ab4-49b6-8655-55c84be14312)


![Image6](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/3eebc36d-14a5-436b-92c4-04adf1cfff8c)

### Model Insights
#### Performance Analysis

Upon analyzing the clusters formed by
K-Means, distinct patterns emerge regarding
emotions. Cluster 0 and Cluster 5 are
characterized by a predominant presence of
non-neutral emotions, while Clusters 1 and 3
primarily comprise neutral sentiments.
Cluster 2 exhibits a notable prevalence of
surprise, suggesting unexpected content in
the text samples. In contrast, Cluster 4
demonstrates a mix of emotions, with
neutrality being the most frequent.

![Image7](https://github.com/shivam-chavan-05/Emotion-Analysis-using-Kmeans/assets/144063863/2220a8bb-cde6-41ec-9306-e7e50a431731)


#### Comparative Analysis
SVM focuses on precise emotion
classification with predefined labels,
providing detailed performance metrics. In
contrast, K-Means explores the dataset's
structure without labels, revealing broader
patterns and clusters of emotional content.
SVM emphasizes classification accuracy,
while K-Means emphasizes data exploration
and pattern identification.

### Insights and Applications
Through SVM classification and K-Means
clustering, I gained insights into the
multifaceted nature of human emotions,
shedding light on their complexity within
textual data. These findings have significant
implications for fields such as psychology,
sociology, and communication studies,
emphasizing the need for nuanced
approaches in understanding human
emotions and communication dynamics.
The insights garnered from SVM
classification and K-Means clustering offer
practical applications across various
domains. In marketing, sentiment analysis
aids in crafting targeted campaigns, while in
customer service, emotion analysis enhances
feedback interpretation for improved
services. Moreover, in healthcare, emotion
monitoring supports mental health
interventions, and in content moderation, it
contributes to creating safer online
environments.
