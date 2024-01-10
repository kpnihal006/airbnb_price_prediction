# Data Analysis of AirBnB listings in San Francisco
Data analysis of AirBnB listings of San Francisco and regression model to predict prices. The data source is from insideairbnb (link:  http://insideairbnb.com/san-francisco).
Datset contained 8055 entries and 16 columns, csv file converted to pandas dataframe. The models used to predict the prices were : Linear Regression, Decision Tree Regression, Random Forest Regression. Hyperparameter Tuning and Cross Validation were key processes in the modelling. Statistical analysis on the dataset was conducted as seen in the python notebook. A Tableau dashboard and story with data visualizations provides insights into the data and can be accessed through the files above. A PACE Strategy document and an executive document was formulated for the project.

## Plan
**Audience**: AirBNB property owners looking to improve business.
**Problem** Statement: Prediction of prices for properties based on relevant features.
**Solution**: Conduct data analysis of the dataset and build a regression model using machine learning.

## Outline of Process
- Objective
- Data collection
- Data preprocessing
- Explorative Data Analysis
- Feature Engineering
- Data Modelling
- Model Evaluation
- Interpretation
- Recommendations

## Libraries used
- pandas
- numpy
- seaborn
- matplotlib
- sklearn
- pickle

## Construct
### Data collection
The data was collected from the source and examined. The data dictionary from the source gave brief explanations regarding the features of the dataset.

### Data preprocessing
Outlier were identified and imputed through IQR and conditions. Duplicates were removed. Null values were dropped. The dataset was cleaned.

### Explorative Data Analysis
The dataset revealed average price of Downtown/Civic Center hotel rooms had high mean prices.
The mean number of reviews for Shared room in North Beach was very high with just 1 listing.
The Downtown/Civic Center has the lowest reviews and a considerably high average price. 
The financial district neighbourhood has higher No. of reviews and a fairly high average price with lower No. of listings.

### Feature Engineering
**Features**
- Days since last review = current date - date of last review
- Review Score = No. of reviews / Days since last review
- Minimum Amount Spent = Minimum Nights * Price
- No. of listings for each neighbourhood
- Average Price for each neighbourhood
- Average No. of nights for each neighbourhood
- Average No. of reviews for each neighbourhood
- Average availability through the year for each neighbourhood

### Modelling
Model was Evaluated on :
- R2 Score
- Mean Absolute Error
- Mean Squred Error
- Root Mean Squared Error

Categorical Encoding using pd.get_dummies() for neighbourhoods and room type was performed.
dataset was split into training, validation and test datasets.
Normalized the dataset values using StandardScaler fit and transform functions.
Built Linear Regression, Decision Tree Regression and Random Forest Regression Models.
Defined a dictionary for hyperparameters and scoring metrics.
Used GridSearchCV for Hyperparameter Tuning and Cross-Validation.

### Evaluation
<img width="1267" alt="image" src="https://github.com/kpnihal006/airbnb_price_prediction/assets/64321012/d72fe9cf-3983-49f5-b62f-a8e94cd99fe5">

### Interpretation and Recommendations
Feature Importance based on the model’s results
The most influential features is availability, neighbourhood, minimum number of nights and the frequency of reviews for a listing
<img width="629" alt="image" src="https://github.com/kpnihal006/airbnb_price_prediction/assets/64321012/2a007655-e317-4222-9f61-997add6353f8">
<img width="1079" alt="image" src="https://github.com/kpnihal006/airbnb_price_prediction/assets/64321012/f532b495-42a9-4233-a707-302ea28665b7">

An analysis of the data of San Francisco listings provided us with these key insights:
The neighbourhood of the listing affects the price significantly.
Listings with a higher minimum number of nights tend to have a higher price.
The frequency of reviews and updates contributes to a better rating.
The Financial District neighbourhood is a good place to list a property with high prices and reviews but a lower number of overall properties.
The Downtown/Civic Center has the highest number of listings with high average pricing but shows very few reviews.
There is a slight relation between the number of reviews over a year and the price. Keeping customer satisfaction high will promote good reviews constantly.
The number of reviews for a shared room in North Beach indicate a demand   for this particular rentals
Local factors should also be taken into consideration before listing a property.
