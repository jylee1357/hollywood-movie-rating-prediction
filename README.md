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

### ⌨️ Models
* Model Comparison 
  - Deep learning model's RMSE
    <img width="1040" alt="Screen Shot 2022-06-13 at 10 11 43 PM" src="https://user-images.githubusercontent.com/98932859/173361479-b682afb8-11ab-4e81-9b52-cdabe619b8ac.png">
    <img width="1028" alt="Screen Shot 2022-06-13 at 10 13 31 PM" src="https://user-images.githubusercontent.com/98932859/173361722-89449368-f598-4d7f-abc2-5d705319e0ac.png">  
    
   - Time series model's RMSE
    <img width="997" alt="Screen Shot 2022-06-13 at 10 17 13 PM" src="https://user-images.githubusercontent.com/98932859/173362374-c2c3510f-da8d-4365-8b4d-ebf1375be862.png">
    
### 📍 Takeaway
* In deep learning model, Random Forest Regressor scored the lowest RMSE
* In time series model, LSTM scored the lowest RMSE
