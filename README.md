# Justin Doan

## Explanation of Solution
The solution I came up with uses a model that employs logistic regression to classify the mushrooms as either poisonous or edible. The solution was coded in Python in a Jupyter notebook, and uses the included Logistic Regression package in the sci-kit learn library to create a model that could be trained to predict the edibility of the mushrooms. I also used pandas to import the data to a dataframe as well as seaborn and matplotlib in order to display a confusion matrix which helped visualize how well the model was able to perform. 

## Design Process

### Research
In being transparent, I'll admit I had zero idea where to start in coding my solution for the challenge. I had never been exposed to such a task in my studies both through the university and independently, however, I was eager to learn what my options were for solving the challenge. After spending some time both on google and watching YouTube videos, I learned more about binary classification, specifically, defining the explanatory and target variables, splitting data into target and test sets, and using a classification algorithm to make our predictions.

Reading through [this article on learndatasci.com](https://www.learndatasci.com/glossary/binary-classification/), which served as my sort of foundation of binary classification, I found that the sklearn library had many different types of classification algorithms in it, such as Decision Trees, Random Forests, and Support Vector Machines to name a few. Ultimately though, I decided on using logisitic regression. Every time I watched a new video or clicked on a new article, the concept of logisitic regression was repeatedly mentioned, and I quickly learned that logisitic regression is one of the most widely used algorithms or methods to make predictions on a data set. Thus, it made sense for me to use this method for my first exposure into binary classification.

### Implementation
Once I decided to settle on using logistic regression as my algorithm of choice to solve the challenge, I outlined the steps of what I needed to do to apply logistic regression to the dataset. I'll have to admit that this article on [an application of logistic regression to the titanic data set](https://towardsdatascience.com/python-scikit-learn-logistic-regression-classification-eb9c8de8938d) served to be the most helpful throughout the implementation process I went through. Primarily, it guided me through the five steps of using logistic regression on a data set: load the data into the notebook, pre-process the data, split the data into training and testing splits, apply the logistic regression algorithm, and (I suppose optionally) visualize the results of the model, in this case by a confusion matrix. It was also extremely helpful in walking me through how to sort of "put the steps into code", and as I stated before I constantly referenced this article when I would get stuck.

The biggest obstacle I had to overcome was the encoding of categorical variables into a format usable for the logistic regression model. While researching how to implement logistic regression, a lot of the data that the examples were using would be for example sports statistics, such as points, rebounds, assists, all numbers. However in the case of the challenge, the data that was being analyzed was all categorical, such as color or shape. Eventually, I figured out that there are ways to encode these categorical variables, such as through one-hot or dummy encoding as [this article](https://towardsdatascience.com/encoding-categorical-variables-one-hot-vs-dummy-encoding-6d5b9c46e2db) discusses, in order to replace these string variables with numbers such that machine learning algorithms can work with them.

After encoding the data into a new dataframe, I then implemented the rest of the steps; I split the data into a training set and test set, applied the logistic regression algorithm, and plotted the results on a confusion matrix. 

### Potential Flaws/Future Implementation ideas
I think it's extremely important to mention the possible flaws in the method that I employed. I think the most significant to me was the near 100% accuracy in predicting the mushroom's edibility. While on paper it's amazing that such an algorithm could be this accurate in its predictions, the only reason I find it concerning is that all throughout my research in reading and watching about logisitc regression algorithms, most of the examples that I came across had around a 70-80 percent accuracy score. However, when going through similar concerns on [stats.stackexchange](https://stats.stackexchange.com/questions/461720/why-is-my-logistic-regression-returning-100-accuracy) and [stack overflow](https://stackoverflow.com/questions/59119041/why-am-i-getting-100-accuracy-for-my-logistic-regression-model), I don't believe I have any of the same issues that have previously been come across, so as a result, I will stand behind my final submission.

Additionally, the only pre-processing of the data I did was encoding the categorical variables. I did not get into feature selection, or reducing the number of input variables, selecting only the ones that are most correlated in determining the target variable. I came across some interesting documentation on using [pearson correlation](https://towardsdatascience.com/logistic-regression-for-binary-classification-56a2402e62e6) to determine which of the data had the highest correlation, however I decided against feature selecting here, as I felt that it's possible all the attributes could be influential in determining a mushroom's edibility. However, a future attempt at this challenge I would say would likely implement some sort of method to feature select,  and it would be interesting to see how this impact the results.

I think if I were to revisit this problem again, I would absolutely be interested in learning more about and impelementing some of the other classification algorithms and methods that are used, some of which I mentioned earlier. I'm especially curious about Random Forests, as I came across a lot of intresting information on both how it works and how well it is able to make predictions. I also think it would be very interesting to compare the performances off the different algorithms in order to see the benefits, drawbacks, and any other interesting observations.
### Learning Takeaways
To put it simply, I learned a lot, not just about binary classification, but just about programming in general.

Having come from absolutely zero knowledge on binary classification, I became aware of the process of applying a classification algorithm to a dataset in order to make predictions on a target variable. Additionally, I was exposed to the many different methods of classification and how we can make predictions using an existing data set. Furthermore, I was exposed to a ton of Python concepts I had never really worked with, such as importing data using pandas, using the sci-kit learn library to analyze the data, and working with matplotlib and seaborn to visualize my results. I also learned a ton about markdown and how it works in a jupyter notebook.

Additionally, I learned quite a bit about being a better programmer. I've only been exposed to code for a year and a half, starting with CS1336 in the fall of 2020, so for the most part I had never dug through library documentation to format a label or done research to figure out the best way to overcome a coding obstacle such as encoding categorical variables. In fact, even through submitting this challenge, I learned quite a bit about how github works and what it means to 'fork' and 'clone' a repo. The process of working through this coding challenge has truly allowed me to sort of experience the aspects of being a programmer that aren't taught in the walls of a university classroom.

### Final Thoughts
I suppose this entire wall of text explaining my design process wasn't part of the challenge requirements and is likely very unneccessary, so if you made it here, **thank you for taking the time to at the very least skim through some of the things I wrote**. I just thought it was important to "pull back the curtains" and provide some insight on how I worked through the coding challenge.

I'm very excited about both this semester's research topics and the opportunity to work on one of them. I'm looking forward to the next steps in this process!

## Documenation
(Note: Some helpful documentation has been discussed above, I'll include here additional sources I found helpful throughout the process)
#### Research
* (https://github.com/llSourcell/logistic_regression/blob/master/Sentiment%20analysis%20with%20Logistic%20Regression.ipynb)
* (https://learn.g2.com/logistic-regression)

#### Pandas Documentation
* (https://www.geeksforgeeks.org/how-to-print-an-entire-pandas-dataframe-in-python/)
* (https://www.geeksforgeeks.org/python-pandas-dataframe-corr/)
* (https://www.geeksforgeeks.org/display-the-pandas-dataframe-in-table-style/)


#### Sci-kit Learn Documentation
* (https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.train_test_split.html)
* (https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
* (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.recall_score.html)
* (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html)
* (https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html)
* (https://scikit-learn.org/stable/modules/preprocessing.html)

#### Markdown documenation
* (https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


