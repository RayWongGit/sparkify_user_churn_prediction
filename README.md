## About Project
This is the Capstone Project of the Data Scientist Nano Degree Course from Udacity. In this project, we did churn anaysis for a music APP Sparkify. We found that features like gender, hour of day, day of week, page activity(i.e. downgrade) affected churn. Based on the identified features, we built a Random Forest Machine Learning model and got a F1_score of 0.934.

## Introduction 
### What is churn?
First thing first, what is churn? Customer churn is the loss of customers. It could be customers uninstall your APP or stop renewing the subscription.
### What is churn rate
Once we know what is churn, churn rate should be pretty intuitive. Churn rate is the metrics to measure customer churn, which is the proportion of contractual customers who leave during a given time period.
### Why Customer/User churn matters?
The cost to acquire a new customer is about 5–25 times that to retain an existing customer. The probability of selling to an existing customer is 60–70%, while it is only 5–20% for a new customer. What’s more, research also finds that reducing the churn rate by 5% could cause the profit increase by 25–90%. So customer is a big deal for SaaS or other subscription-based business.
### Business problem for this project
In this project we are going to explore churn for Sparkify. Sparkify is a pseudo popular digital music service similar to Spotify or Pandora. Millions of users listen to their favorite songs on Sparkify every day. They either use the free tier that place advertisements between the songs or use the premium subscription model, where they access music as free but pay a monthly flat rate. Users can upgrade, downgrade, or cancel their service at any time. If we can accurately identify the users at risk before they leave, the business can provide interventions like offering them discounts and incentives, which would potentially save the business millions in revenue.
However it should be noted that the stakeholders of this project is not only Sparkify or music streaming service providers, other business like mobile phone service, bank, internet services to whom churn rate matters a lot could also gain some insights from this project and apply them to their own business model.
## About Dataset
Every time a user interacts with the Sparkify service while they’re playing songs, logging out, like in a song with a thumbs up, hearing an ad, or downgrading their service, it generates data. The data we are using is right this user generated data.
The full dataset is 12GB, for this project, we will use a a tiny subset dataset which is 128M to explore the data and build a prediction model.

## Conclusions and Discussions
In this project, we tried to predict user churn with the Sparkify dataset. Since there were some missing values in the dataset, we first did some data wrangling on the dataset. After preliminary exploration, we created a couple new features (state, hour, weekday) to better understand the pattern of churn. From the visualization point of view, we found some variables that significantly related to churn. Based on this knowledge, we build a machine learning model to predict churn and got a F1 Score of 0.934 from the best model.
There are a couple limitations in this project:
There was no data description coming with this dataset, during exploration process we had to guess what each variable meant. This may result in some kind of misinterpretation
In model selection, we chose Logistic regression, SVM, Random Forest as a set to start with. XG Boost may perform better than Random Forest, although it is not available in Pyspark
We split the data once and fit the train and validation data to select the best model. However, the variance from train and validation data may also affect the result. To reduce this affect, we could do a statistical test on a couple iterations of different split.

## More
More about this project regarding background, analysis, result and discussion please refer to the Jupyter notebook file in the same fold as well as the blog [Make It Stick: Predicting Your Users’ Churn Before They Go](https://medium.com/@raywong.seattle/make-it-stick-predicting-your-users-churn-before-they-go-c974d7f8b81f)

## Reference

- [Wikipedia Customer attrition](https://en.wikipedia.org/wiki/Customer_attrition)
- [Wikipedia Churn Rate](https://en.wikipedia.org/wiki/Churn_rate)
- [Churn Rate: How to Define and Calculate Customer Churn](https://clevertap.com/blog/churn-rate/)
- [The Value of Keeping the Right Customers](https://hbr.org/2014/10/the-value-of-keeping-the-right-customers)
- [What Is Churn Rate?](https://blog.hubspot.com/service/what-is-churn-rate)
- [Cohort Analysis](https://clevertap.com/blog/cohort-analysis-user-retention/)
- [Why Users Uninstall Apps: 28% of People Feel Spammed [Survey]](https://clevertap.com/blog/uninstall-apps/)
- [Hands-on: Predict Customer Churn](https://towardsdatascience.com/hands-on-predict-customer-churn-5c2a42806266)
- [PySpark 2.0 The size or shape of a DataFrame](https://stackoverflow.com/questions/39652767/pyspark-2-0-the-size-or-shape-of-a-dataframe)
- [How to find count of Null and Nan values for each column in a PySpark dataframe efficiently?](https://stackoverflow.com/questions/44627386/how-to-find-count-of-null-and-nan-values-for-each-column-in-a-pyspark-dataframe)
- [check for duplicates in Pyspark Dataframe](https://stackoverflow.com/questions/50122955/check-for-duplicates-in-pyspark-dataframe)-[Customer Acquisition Vs.Retention Costs](https://www.invespcro.com/blog/customer-acquisition-retention/)

- [Filter Pyspark dataframe column with None value](https://stackoverflow.com/questions/37262762/filter-pyspark-dataframe-column-with-none-value/37262973)
- [How to calculate the counts of each distinct value in a pyspark dataframe?](https://stackoverflow.com/questions/42451189/how-to-calculate-the-counts-of-each-distinct-value-in-a-pyspark-dataframe)
- [How to use matplotlib to plot pyspark sql results](https://stackoverflow.com/questions/45003301/how-to-use-matplotlib-to-plot-pyspark-sql-results)
- [List of HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
- [how to change a Dataframe column from String type to Double type in pyspark
](https://stackoverflow.com/questions/32284620/how-to-change-a-dataframe-column-from-string-type-to-double-type-in-pyspark)
- [How to convert categorical data to numerical data in Pyspark](https://datascience.stackexchange.com/questions/6268/how-to-convert-categorical-data-to-numerical-data-in-pyspark/11363)
- [StringIndexer](https://spark.apache.org/docs/latest/ml-features.html#stringindexer)
- [How to delete columns in pyspark dataframe](https://stackoverflow.com/questions/29600673/how-to-delete-columns-in-pyspark-dataframe)
- [How to split columns into label and features in pyspark?
](https://stackoverflow.com/questions/54662701/how-to-split-columns-into-label-and-features-in-pyspark)
- [PySpark to PMML - “Field label does not exist” error](https://stackoverflow.com/questions/44779002/pyspark-to-pmml-field-label-does-not-exist-error)
- [RANDOM FOREST WITH PYTHON AND SPARK ML](https://www.silect.is/blog/2019/4/2/random-forest-in-spark-ml)

