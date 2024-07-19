# Daegu Apartment Regression Model

### Business Understanding
---
[Daegu](https://en.wikipedia.org/wiki/Daegu) is South Korea's third-largest urban agglomeration after Seoul and Busan, the third-largest official metropolitan area in the country with over 2.5 million residents and the second-largest city in the Yeongnam region in the southeastern Korean Peninsula after Busan. However, the real estate market in Daegu faces significant challenges due to an increasing number of unsold apartment units

**1.1 Problem Statement**

[As of December 2023](https://koreajoongangdaily.joins.com/2023/02/07/business/industry/housing/20230207175620058.html), the number of unsold apartments nationwide reached 68,000 units, the highest in seven years since 2015. This increase in unsold units is more pronounced outside Seoul, where the unsold inventory rose by 19.8%​. In Daegu, the number of unsold apartments has surged, exacerbating concerns about market stability and economic impact. 

The real estate market in Daegu is experiencing an **oversupply of unsold apartment units, leading to market instability and financial challenges for property owners and developers.** This situation necessitates the development of an accurate apartment price prediction model to provide **realistic price expectations, stabilize the market, and ensure affordability** for potential buyers.

**1.2 Goal**

In this scenario, as startup focused on real estate technology consultant, I have the goal to develop a robust apartment price prediction model for Daegu using machine learning techniques. This model aims to:
- Provide realistic price estimates for apartment units.
- Ensure housing affordability for potential buyers.
- Support property owners in setting competitive prices that reflect current market conditions.
- Help stabilize the local real estate market by reducing the volume of unsold units.

**1.3 Project Stakeholder**

Project stakeholders are those with any interest in your project's outcome,

- **Property Owners and Developers**: to set competitive prices for new and existing apartment units.

- **Real Estate Agents**: to provide data-driven pricing advice to their clients, enhancing their service offerings and credibility.

- **Prospective Buyers**: to make informed purchasing decisions and ensure they are getting fair market value.

**1.5 Metric Evaluation**

To check the performance of our model, we will use Adjusted R², MAE, and RMSE.

- **Adjusted R²**: This metric measures the proportion of variance in the dependent variable that is explained by the model, adjusted for the number of predictors in the model. Unlike R², Adjusted R2 get a proper impact analysis of the feature on the model or the dependent feature. in multiple regression settings [(Adani)](https://www.aidtm.ac.in/en/blogs/why-r-square-need-to-adjust). A higher Adjusted R² indicates a better fit, taking into consideration the model complexity.



- **Root Mean Squared Error (RMSE):**
    RMSE measures the average magnitude of the errors between predicted and actual values, taking the square root of the mean squared errors. (after we do prediction there's no outliers in residual, means that RMSE is good to be used. In the context of housing prices, a lower RMSE is desirable because it means the model is more accurate in predicting the actual sale prices of houses ([Palupi, 2023](https://ejournal.kresnamediapublisher.com/index.php/jri/article/view/262))


### Data details
---
|             Attribute            | Data Type |                               Description                               |
|:--------------------------------:|:---------:|:-----------------------------------------------------------------------:|
| HallwayType                      | Object    | Types of apartment hallways                                             |
| TimeToSubway                     | Object    | Measure time takes from apartment to subway station                     |
| Subway Station                   | Object    | Name of subway station nearby apartment                                 |
| N_FacilitiesNearBy(ETC)          | Float     | number of other facilities such as hotels and special schools           |
| N_FacilitiesNearBy(PublicOffice) | Float     | Number of public offices nearby apartment                               |
| N_SchoolNearBy(University)       | Float     | Number of universities nearby apartment                                 |
| N_Parkinglot(Basement)           | Float     | Count number of parking spaces on basement                              |
| YearBuilt                        | Integer   | The year when the apartment was created                                 |
| N_FacilitiesInApt                | Integer   | Number of facilities for residents like swimming pool, gym, play ground |
| Size(sqf)                        | Integer   | Size of apartment in square feet                                        |
| SalePrice                        | Integer   | Apartment price in Korean Won (KRW)                                            |



### Data cleaning done :
---
- Change Data Type
- Handling Inconsistency
- Handling Anomaly
- Handling Missing Values
- Handling Duplicate
- Handling Outliers

### Model Chosen : Random Forest Initial

After evaluating the models' performance, **Random Forest Initial** was chosen over Stacking Regressor due to:
- **RMSE:** The Random Forest (Initial) achieved a competitive RMSE on the test set (41726.1743), which is close to that of the best performing model 
- **RMPE:** The RMSPE on the test set (23.407702) indicates that it has a reasonably low percentage error.
- **Adjusted R2:** The Adjusted R² Test value (0.839063) is also high, indicating that the model explains a significant proportion of the variance in the target variable.
- **Model Stability:** The difference between RMSE Train and RMSE Test for the Random Forest (Initial) is relatively small (221.4633), suggesting that the model generalizes well to unseen data and does not overfit.
- **Interpretability:** Random Forest model provides clear insights into feature significance, aiding in actionable decision-making.

---

Video presentation and powerpoint link : 
https://drive.google.com/drive/folders/1xEq6g5EL_r9eg8WkXHsGOxg3ZJ-jNAme?usp=sharing  
