# Implementing Linear Regression
# Darius Mahamedi
For this biweekly report, I focused my energy on trying to manually code and implement the least-mean-squared algorithm in Python. My goal was to implement the algorithm so I could feel like I understand it first, and then to use Scikit-learns built-in linear regression classes to compare my work. I also briefly played around with Scikit-learn seperately (which you can see in the file sklearnRegression.ipynb)
### Pandas
My first implementation of the algorithm attempted to store the datasets in a Pandas dataframe. I encountered several problems with Pandas, the big one being that the Pandas programs were extremely slow -- a large part of this was because of my own code, but overall I just felt like I should try using something other than a Pandas dataframe.
### Numpy
My second and main implementation of the algorithm used NumPy, which I felt was **much better** and more intuitive to use. The nice thing about NumPy is that -- according to its documentation -- it is built for matrix operations and linear algebra. That makes it more intuitive to use, and my final code ended up being **much** simpler.
### Why NumPy is the best
My implementation of the algorithms using NumPy is really simple now, but when I first tried to code everything with NumPy I was not as familiar with the built in functions. This resulted in for loops when I wanted to predict data, get the gradient, etc. It was made worse by the fact that the tasks relied on each other, so getting the gradient required I predicted the data, and so on. The result was that training the model over 1000 iterations took **forever**.
***However***, after I got more familiar with NumPy and built in functions like .dot(), I was able to simplify the code a great deal and remove most of the for loops. Now, training the model on a large dataset for **100,000** iterations takes * *less than a minute* * on my computer, which I think is really significant. My Pandas model took longer than just for 30 iterations.

### Datasets
The main dataset I used to test and build this program is Scikit-learns built-in California Housing (fetch_california_housing) dataset. It seems like a pretty big dataset, which might be why I didn't seem to have many problems with overfitting, even after 100,000 iterations.
The other dataset I used is OpenML's Wine Quality dataset.

# Results
I am really pleased with how numpyLinearRegression.ipynb came out. It is extremely fast, at least by comparison of earlier versions, and I am hoping to build off of it to write programs for ridge and lasso regression.

