## City of Girls Film Predictions:
### Web-Scraping and Linear Regression Modeling

Predicting the Gross of the film adaptation of Elizabeth Gilbert’s book City of Girls and making recommendations to reach a worldwide total gross of $500 million USD

**Abstract**
The goal of this project is to use a linear regression model to predict the worldwide total gross revenue of an in-production film, an adaptaion of Elizabeth Gilbert's book City of Girls. If predicted revenue is less than $500 million USD, model feature coefficients will be used to make recommendations to the production team for ways that the target gross revenue can be reached. I scraped data from boxofficmojo.com for over 1,700 top-grossing films from 2010-2021 to create the linear regression model, relying on continuous numerical records (eg film budget) and categorical feature engineering (such as distribution company) to produce results.

**Design**
We at Metis are on the production team for the film adaptation of City of Girls, an instant New York Times bestseller from Elizabeth Gilbert, the author of Eat Pray Love. The film is in-production and the production company has hired us to predict the worldwide gross revenue of the film. Additionally, we will use our model to make recommendations on how the gross revenue can be brought to the production company’s target revenue of $500 million USD. 

**Data**
The dataset contains 1,739 films, selected from the top 15 grossing films by week since January, 2010. Data for each film was scraped from the website boxofficemojo.com and includes: worldwide gross revenue, budget, genres, number of theaters that showed the film, date of domestic release, distribution company, and rating.

**Algorithms**
**Data Preparation**
Films missing budget or revenue data were removed (which brought the operating sample size to 1018 films). 
Categorical data (such as distribution company and genre) were transformed into binary (“dummy”) variables. 
Data was split into training data (80%) and test data (20%) for model testing. The training data was further divided into another subset of training data (80% again) and validation data (20%) for validation before testing. This version of model validation was used because the large number of features (87) relative to the small number of rows (651 to train on) made other validation methods less stable.
Data was scaled via standard scale
A Linear Regression model was created and fit, relying on feature engineering to arrive at an adjusted R^2 value of 0.59 and validation score of 0.53.
Lasso (and Ridge) regularizations were performed. Optimal lambda for Lasso was 0.01 

More regularization and predictions need to be performed to arrive at desired results.
Tools used include: Scikit-learn, pandas, numpy, BeautifulSoup, and Matplotlib

Communication
Please see the accompanying presentation slides and code for this project.
