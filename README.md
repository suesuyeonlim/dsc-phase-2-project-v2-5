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
Finally, I run three different potential models to see which one performs the best. The first model uses zipcodes as dummy variables as well as other predictor variables, the second model uses counties instead. The third model does not use either zipcodes or counties. Among them, I pick the first model as the R-squared is highest and AIC & BIC are the lowest.

First Model

<img width="706" alt="image" src="https://user-images.githubusercontent.com/19903898/235324022-3804a3cd-211c-4fff-8b64-3df0d48fcd3e.png">

Second Model

<img width="765" alt="image" src="https://user-images.githubusercontent.com/19903898/235324054-b425abed-160c-429f-8d9d-6a78d483d174.png">

Third Model

<img width="765" alt="image" src="https://user-images.githubusercontent.com/19903898/235324077-9d235832-b3ce-4954-ae38-75ab05d6075c.png">

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

