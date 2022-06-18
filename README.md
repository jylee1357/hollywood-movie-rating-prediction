# Hollywood Movie Ratings Prediction

### 🙋‍♂️ Goals
- Through castings, I tried to create a model that predicts movie ratings and revenue
- Understand the influences and impacts of castings in Hollywood movies
- Made prediction using RNN,LSTM,GRU (based on Time Series)

### 𝌞 Data Collection & Preprocessing
* STEP 1
  - Used 2020-2021 IMDB Dataset (gathered information about movie title/runtime/ratings)
* STEP 2
  - Web crawled revenue data for each movie from Box Office Mojo website
* STEP 3
  - Gathered data about castings for each movie using IMDB 'title.principals' (since the data were extremely large, I used PySpark)
  - Mapped 'title.principals' with 'movie.id' to match castings with movies   
* STEP 4
  - Created 'past performance metrics' to display the ability of each casts
  - Data Features  
    <img width="564" alt="Screen Shot 2022-06-18 at 2 12 31 PM" src="https://user-images.githubusercontent.com/98932859/174423818-93860ad9-e9c1-4cb6-b970-327cf32c50e1.png">
* STEP 5
  - Merged 'past performance metric' that was calculated in step4 with basic movie infos
  - The final performance metric was calculated per movie by adding the 'past performance metric' of the entire casts within each movie.

### ⌨️ Models
* Lists of Models 
  - Linear & Logisitc Regression (with K-Fold Cross Validation)
  - Random Forest
  - Gradient Boostings
  - Support Vector Machine
* Prediction Result (Movie Ratings)
  <img width="996" alt="Screen Shot 2022-06-18 at 2 28 30 PM" src="https://user-images.githubusercontent.com/98932859/174424257-cee2525a-e26e-4c16-b777-ae8fa4f6834e.png">
* Prediction Result (Movie Revenue)
  <img width="996" alt="Screen Shot 2022-06-18 at 2 28 30 PM" src="https://user-images.githubusercontent.com/98932859/174424294-6bd4be41-b4af-4f08-a54e-6e169c73ec43.png">

### 📍 Takeaway
* In movie ratings prediction, Random Forest Classifier achieved the highest accuracy
* In movie revenue prediction, Linear Regression achieved the highest R-Squared
* In Lasso Regression, 'past movie rating' turned out to be the most important feature
* In Random Forest model, 'cast acting experience' turned out to be the most important feature
