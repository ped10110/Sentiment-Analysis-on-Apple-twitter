<h1>Sentiments ON Apple In Tweeter </h1>
<h2>1. Introduction</h2>
Social media webweb sites like Twitter are essential stores for public perspectives and remarks withinside the virtual age. Improving product development, advertising and marketing plans, and client relationships for companies like Apple relies upon on their understanding of the way clients view their items on Twitter.

Understanding sentiment with the aid of using manually analyzing heaps of tweets, though, is a Herculean effort. Natural language processing (NLP) can automate this, letting businesses unexpectedly compare public opinion on a huge scale.

This mission objectives to create a NLP version that could robotically categorize a tweet`s sentiment as positive, negative, or neutral. This will allow Apple and different fascinated events to base their selections on public opinion, consequently guiding them. </br>

<h2>Business Understanding</h2>
Automating sentiment analysis on Twitter helps Apple and other interested parties to acquire insightful information without requiring great manual effort. Real-time tracking of public sentiment enables Apple to be more reactive to consumer input, maximize marketing strategies, and enhance product offers. In the end, this might result in more successful product launches and better consumer happiness.
<h2>Data Understanding</h2>
This project's dataset originates from CrowdFlower, through data.world. Over 3000 tweets manually rated for sentiment by human annotators make up the dataset. Every tweet is marked as either positive, negative, or neutral.

Source Summary: - Dataset: Apple Twitter Sentiment (CrowdFlower)
Source: data.world - Apple Twitter Sentiment
Given the task at hand, this dataset is quite useful since it directly addresses the need for an automated system to categorize public opinion on Twitter regarding Apple products. </br>

<h2>Data Preparation</h2>
Drop unnecessary columns
Goal: Remove unrelated columns used for analysis to make data records cleaner and more focused.
Reason:
Unrelated columns: These columns provide metadata or details that do not contribute to the mood analysis model. Delete data records and improve processing speed.
By removing columns like id, query, _unit_id, we focus only on important functions: tweet text and emotions. </br>

<h2>Exploratory Data Analysis (EDA)</h2>
<b>1. Which are the most dominating sentiments?</b>
<img src="https://github.com/BLACKSPI/Phase_4_project/blob/45745d0efe21023f899bd84617a19cdca72b2de1/Sentiment%20distribution.png", alt="sentiment distribution">

<p>This graph shows that most tweets are neutral about Apple. This indicates that the majority of users post factual or non-emotional content. Negative tweets are the second most common, highlighting a significant amount of criticism and complaints. Positive tweets are less common. This means that fewer users will express strong Apple approval. Very positive tweets are the least common and show that enthusiastic praise is relatively rare. Overall, the  distribution of mood suggests that  Apple receives a mix of opinions, but neutral arguments dominate more criticism than strong praise.</p>

<h2>Preprocessing</h2>
The objective here is to clean the text data to ensure it is in a format that can be processed by the machine learning model. This includes removing special characters, stop words, and unnecessary spaces.

<p>After preprocessing we wanted to see the most frequently used terms and the top positive and negative terms.</p>

<b>What are the most frequent terms?</b>
<p><img src="https://github.com/BLACKSPI/Phase_4_project/blob/762364260af5a88a99a2d665067cc714cd34e085/most%20used%20terms.png"></p>
<p>The diagram above shows the terms that are most frequent in our dataset.</p>

<b>What are the top Positive and Top Negative Words?<b/>
<p><img src="https://github.com/BLACKSPI/Phase_4_project/blob/6a39c7c8e84939df204568c3c90a243d3e63f907/positive%20vs%20negative.png", alt="image"></p>

<h1>Modelling</h1>
In this project we decided to use the following models:
<ol><li>Logistic Regression model (Baseline Model).
 Logistic regression is chosen for its simplicity and easy explanation. As the simplest model of the linear family classification, it acts as a good starting point.</li>
 <li>Random Forest Classifier. Random forest is known for its ability to manage more complex relationships and interactions between characteristics. It is also less excessive adjustment compared to personal decisions, making it a solid candidate to improve the performance of the model.</li>
 <li>Support Vector Machine (SVM). SVM is known for its ability to find optimal decisions in large data. Using linear nucleus, we hope SVM will grasp complex models in data, capable of improving random forest model.
 </li>
 <li>XGBoost. XGBOOST uses enhanced use, combining weak learners (shallow trees) to create a strong learner. It is known for its high performance, especially on unbalanced data sets and will further improve the accuracy of the classification compared to previous models.</li>
</ol> 

<h1>Model Evaluation</h1>

<p><img src="https://github.com/BLACKSPI/Phase_4_project/blob/806aad95bab81bcce671eefead0ba50c55957e79/ROC%20curve.png", alt ="img"></p>
<p>The performance of the <b></b>Random Forest</b> and <b></b>Logistic Regression</b> classifiers across several categories is shown by the multi-class ROC curve. With AUC scores varying from <b>0.77 to 0.88</b> across various classes, both models demonstrate a high degree of predictive power. In most categories, <b>Logistic Regression</b> performs marginally better than Random Forest, but its AUC scores are higher in class (3). Both models are effective at differentiating between classes, as evidenced by their overall significantly higher performance compared to random guessing (AUC = 0.5). To enhance performance on the less ideal categories, future actions might include investigating ensemble techniques or fine-tuning hyperparameters.</p>
<p>After comparing model performance, model chosen is Logistic Regression as the final model. This decision is based on:

Accuracy: Logistic Regression achieved an accuracy of 0.7378, the highest between all tested.
Class Imbalance Handling: Logistic Regression struggles with class 3 but performed well on the majority of classes, especially on class 1 (high recall of 94%).
Model Simplicity: Logistic Regression is a relatively simple model, making it easier to interpret and deploy in real-world applications.
Looking at performance across all classes, it is justified that Logistic regression was the best.</p>

<h1>Recommendations</h1> </br>
<ol><li>Improve Customer Support Response by monitoring and addressing common 
   complaints to reduce dissatisfaction and enhance Product Quality and Transparency.</li>
 </br>
 <li>Encouraging user engagement and Promoting positive reviews by Featuring 
   satisfied customer testimonials in marketing.</li>
</br>
<li>Improve data collection and sentiment monitoring by collectin feedback      from customers' reviews</li>
</br>
<li>Ensure Real-Time sentiment analysis by Deploying sentiment tracking to  
   detect emerging issues early and respond quickly.</li>
</br>
<li>Enhance AI-Driven Customer Insights to detect sentiment in customer service 
   chats and provide faster resolutions.</li></ol>



