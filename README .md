
# Sales Forecasting using Machine Learning

-Decision Tree Classification
and Random Forest Models were used to forecast future Sales from the Superstore Sales Data provided.


## Acknowledgements
https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.OneHotEncoder.html
https://towardsdatascience.com/how-to-implement-and-evaluate-decision-tree-classifiers-from-scikit-learn-36ef7f037a78
https://www.datacamp.com/tutorial/decision-tree-classification-python
 - https://www.kaggle.com/code/andrespadillaucros/2-store-sales-random-forest-forecast
## Tech Stack

Jupyter Notebook



## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://katherineoelsner.com/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/)


## Lessons Learned

What did you learn while building this project? What challenges did you face and how did you overcome them?

Challenges:

I really struggled with Hot encoding, I could not convert the categorical data into numerical.

It is definitely a topic I will look further into and learn.
## TASKS COVERED IN THE ASSESSMENT

Jupyter Notebook for Data Analysis of Superstore Sales dataset using Pandas and Matplotlib.

Tasks covered in this Notebook are:
1.Identifying and importing essential libraries

2.Data loading and overview

3.Print attributes like count, mean, max, min, standard deviation, etc

4.Used the null function: df.isnull().sum() to find out if there were any null values in the data.

5.Calculated Sum of Sales and Profit from Orders sheet using: df['Sales'].sum() 

6.Visualized the data to perform data analysis. 
#Scatter plot sales vs profit
sns.regplot(x='Sales',y='Profit', data=df, scatter_kws={"color":"blue"}, line_kws={"color":"black"})

Reference: https://jakevdp.github.io/PythonDataScienceHandbook/04.02-simple-scatter-plots.html

7.Created a correlation matrix using the function:

correlation_matrix=df.corr(method='pearson')
sns.heatmap(correlation_matrix,annot=True)
plt.title('correlation matrix for numeric feautures')
plt.xlabel('Sales')
plt.ylabel('Profit')

Reference: https://www.geeksforgeeks.org/create-a-correlation-matrix-using-python/

8.#removing unnecessary column such as postal code

df = df.drop(['Postal Code'],axis=1)

9.I did a more analysis by a adding a seaborn pairplot.

Reference:https://seaborn.pydata.org/generated/seaborn.pairplot.html

10.Created a pie chart to calculate  #no of customers region wise

plt.figure(figsize=(8,8))
plt.title('Region')
plt.pie(df['Region'].value_counts(), labels=df['Region'].value_counts().index,autopct='%1.1f%%')
plt.show()

Reference: https://www.w3schools.com/python/matplotlib_pie_charts.asp


Before creating the Decision Tree, I calculated the minimum and maximum time stamp.

I then created a persistance moodel to see if it performs better than the random forest model.


Reference:
https://machinelearningmastery.com/persistence-time-series-forecasting-with-pyt
https://machinelearningmastery.com/random-forest-for-time-series-forecasting/
https://www.datacamp.com/tutorial/decision-tree-classification-python



I am still trying to make sense of the models as these are fairly new concepts, however I can conclude that the random forrest is a better model as more like to predict sales data more accuarately.
The test RSME for the persistance model is 1467.884.

The Random forest test score is 1039.837679880998.

