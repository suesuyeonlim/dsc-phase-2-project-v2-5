# Determining Factors for Housing Prices
## I. Overview and Business Understanding
A real estate website is the client for this project. The client wants to build a predictive model for housing prices in King's county in Washington, which can be potentially generalized to the whole nation. For this reason, the client wnts to know which factors are determinants for housing prices.

In this repository, I run Multiple Linear Regression to assess which predictor variables are useful in determining housing prices and how impactful they are.

## II. Data
The data used contains housing transactions in King's county for years 2021-2022. It has sale prices, as well as other characteristics (e.g., transaction date, the number of bedrooms, square feet of the living area, etc.).

## III. Methodology
Housing sale price is modeled using Multiple Linear Regression. It is log-transformed as the original distribution is right skewed, and the price is always positive.

<img width="856" alt="image" src="https://user-images.githubusercontent.com/19903898/235323742-a651a4f3-0051-45b4-9d22-2a9136b7a8aa.png">

Also, I transform some character variables into ordinal variables as shown below.
<img width="1132" alt="image" src="https://user-images.githubusercontent.com/19903898/235323893-4917a5ec-9912-4f88-a413-f4fefe57dc22.png">

## IV. Result
Finally, I run three different potential models to see which one performs the best. The first model uses the following variables as predictor variables:
- SQFT of Living Area 
- SQFT of Lot
- Transaction Year
- Home Condition
- Building Grade
- View
- Waterfront
- Greenbelt
- Nuisance

The second model uses dummy variables for counties as well as the predictor variables in the first model. The third model uses dummy variables for zipcodes instead of counties. Among them, I pick the third model as the R-squared is highest for both training and validation data, and AIC & BIC are the lowest.

First Model

<img width="652" alt="image" src="https://github.com/suesuyeonlim/dsc-phase-2-project-v2-5/assets/19903898/7d48dc0c-e9cc-4428-83dd-ca0d3d707d5e">

Second Model

<img width="778" alt="image" src="https://github.com/suesuyeonlim/dsc-phase-2-project-v2-5/assets/19903898/6c891b13-739e-4f09-a837-9e5599e2c193">

Third Model

<img width="778" alt="image" src="https://github.com/suesuyeonlim/dsc-phase-2-project-v2-5/assets/19903898/5e3149a7-ab4a-4346-afdf-cfb83ec77bca">

## V. Conclusion
Based on the result, it would be appropriate to use the following variables for the predictive model.
- SQFT of Living Area 
- SQFT of Lot
- Transaction Year
- Home Condition
- Building Grade
- View
- Waterfront
- Greenbelt
- Nuisance
- Zipcode

