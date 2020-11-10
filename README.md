# Problem Statement

The Gardner Real Estate Company is looking into increase sales in the Ames, Iowa region. To increase market share the company has decided that an application where customers can input specific house details and receive a sale price would set them apart from the competition. The house price predicting model should be easy to understand and provide a reasonably accurate estimate of a home's sale price. 

# Dataset

The data analyzed was from the Ames Assessor's Office and was utilized in computing assessed values for individual residential properties sold in Ames, IA from 2006 to 2010. Data dictionary is shown [below](#Data-Dictionary)

# Executive Summary

There are 80 different features recorded for each house sold in Ames, IA. We looked at all 23 nominal, 23 ordinal, 14 discrete, and 20 continuous features to determine the features which were the most directly correlated to the house's sale price. We decided that while a more complex model might be slightly more precise at predicting sale price, a simpler model allows customers to easily determine what their own house might be worth.

There were 11 features which we found to have the largest impact on sale price while also being simple enough for all customers to understand.

<img src="./assets/neighborhood_sales_prices.png" alt="neighborhood" align="right" width="470">

|  |**Model Features**|  | 
| --- | :---: | --- | 
|  |**Numeric**|  | 
| Lot Area | Overall Quality | Garage Area | 
| Total Bathrooms | Total Square Feet | Remodel Year |
|  |  |  | 
|  |**Catagorical**|  | 
| MS SubClass | Neighborhood | Condition 1 | 
| Exterior Quality | Kitchen Quality |  |

Additionally as we modeled sale prices without using any interaction features customers can directly see how their own house's specifications affect their potential sale price. The following table shows how much a house's sale price would incraese if a certain feature was increased.

|  | **Lot Area** | **Overall Quality** | **Total Square Feet** |  **Garage Square Feet** |  **Remodel Year** |  **Total Bathrooms** |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
||||||||
| **Dollar increase** |2.0|10,700|32.4|23.9|248|10,900|

# Conclusions

* A model was created which takes in 11 features (6 numeric and 5 catagorical)
* The simple model correctly predicts the sale price of around 90% of the houses sold in Ames, IA between 2006 and 2010
* The average error in the predicted sale price is about 25,000 dollars

## Next Steps

* Look into creating more powerful model which could be used in combination with the simple model to more accurately predict a house's sale price for customers who want to know the exact price of their house
* Determine the functionality of this model in different regions of Iowa
* See if there are any other housing metrics which could be recorded and incorporated into the model to improve predictions


# Data Dictionary

|<p align="center">Feature|<p align="center">Type|<p align="center">Description|
| --- | --- | --- |
|<p align="left">Observation Number|<p align="left">Discrite|<p align="left">Observation number of house sale|
|<p align="left">PID|<p align="left">Nominal|<p align="left">Parcel identification number - can be used with city web site for parcel review|
|<p align="left">MS SubClass|<p align="left">Nominal|<p align="left">Identifies the type of dwelling involved in the sale|
|<p align="left">MS Zoning|<p align="left">Nominal|<p align="left">Identifies the general zoning classification of the sale|
|<p align="left">Lot Frontage|<p align="left">Continuous|<p align="left">Linear feet of street connected to property|
|<p align="left">Lot Area|<p align="left">Continuous|<p align="left">Lot size in square feet|
|<p align="left">Street|<p align="left">Nominal|<p align="left">Type of road access to property|
|<p align="left">Alley|<p align="left">Nominal|<p align="left">Type of alley access to property|
|<p align="left">Lot Shape|<p align="left">Ordinal|<p align="left">General shape of property|
|<p align="left">Land Contour|<p align="left">Nominal|<p align="left">Flatness of the property|
|<p align="left">Utilities|<p align="left">Ordinal|<p align="left">Type of utilities available|
|<p align="left">Lot Config|<p align="left">Nominal|<p align="left">Lot configuration|
|<p align="left">Land Slope|<p align="left">Ordinal|<p align="left">Slope of property|
|<p align="left">Neighborhood|<p align="left">Nominal|<p align="left">Physical locations within Ames city limits|
|<p align="left">Condition 1|<p align="left">Nominal|<p align="left">Proximity to various conditions|
|<p align="left">Condition 2|<p align="left">Nominal|<p align="left">Proximity to various conditions (if more than one is present)|
|<p align="left">Bldg Type|<p align="left">Nominal|<p align="left">Type of dwelling|
|<p align="left">House Style|<p align="left">Nominal|<p align="left">Style of dwelling|
|<p align="left">Overall Qual|<p align="left">Ordinal|<p align="left">Rates the overall material and finish of the house|
|<p align="left">Overall Cond|<p align="left">Ordinal|<p align="left">Rates the overall condition of the house|
|<p align="left">Year Built|<p align="left">Discrete|<p align="left">Original construction date|
|<p align="left">Year Remod/Add|<p align="left">Discrete|<p align="left">Remodel date (same as construction date if no remodeling or additions)|
|<p align="left">Roof Style|<p align="left">Nominal|<p align="left">Type of roof|
|<p align="left">Roof Matl|<p align="left">Nominal|<p align="left">Roof material|
|<p align="left">Exterior 1|<p align="left">Nominal|<p align="left">Exterior covering on house|
|<p align="left">Exterior 2|<p align="left">Nominal|<p align="left">Exterior covering on house (if more than one material)|
|<p align="left">Mas Vnr Area|<p align="left">Continuous|<p align="left">Masonry veneer area in square feet|
|<p align="left">Exter Qual|<p align="left">Ordinal|<p align="left">Evaluates the quality of the material on the exterior|
|<p align="left">Exter Cond|<p align="left">Ordinal|<p align="left">Evaluates the present condition of the material on the exterior|
|<p align="left">Foundation|<p align="left">Nominal|<p align="left">Type of foundation|
|<p align="left">Bsmt Qual|<p align="left">Ordinal|<p align="left">Evaluates the height of the basement|
|<p align="left">Bsmt Cond|<p align="left">Ordinal|<p align="left">Evaluates the general condition of the basement|
|<p align="left">Bsmt Exposure|<p align="left">Ordinal|<p align="left">Refers to walkout or garden level walls|
|<p align="left">BsmtFin Type 1|<p align="left">Ordinal|<p align="left">Rating of basement finished area|
|<p align="left">BsmtFin SF 1|<p align="left">Continuous|<p align="left">Type 1 finished square feet|
|<p align="left">BsmtFinType 2|<p align="left">Ordinal|<p align="left">Rating of basement finished area (if multiple types)|
|<p align="left">BsmtFin SF 2|<p align="left">Continuous|<p align="left">Type 2 finished square feet|
|<p align="left">Bsmt Unf SF|<p align="left">Continuous|<p align="left">Unfinished square feet of basement area|
|<p align="left">Total Bsmt SF|<p align="left">Continuous|<p align="left">Total square feet of basement area|
|<p align="left">Heating|<p align="left">Nominal|<p align="left">Type of heating|
|<p align="left">HeatingQ|<p align="left">Ordinal|<p align="left">Heating quality and condition|
|<p align="left">Central Air|<p align="left">Nominal|<p align="left">Central air conditioning|
|<p align="left">Electrical|<p align="left">Ordinal|<p align="left">Electrical system|
|<p align="left">1st Flr SF|<p align="left">Continuous|<p align="left">First Floor square feet|
|<p align="left">2nd Flr SF|<p align="left">Continuous|<p align="left">Second floor square feet|
|<p align="left">Low Qual Fin SF|<p align="left">Continuous|<p align="left">Low quality finished square feet (all floors)|
|<p align="left">Gr Liv Area|<p align="left">Continuous|<p align="left">Above grade (ground) living area square feet|
|<p align="left">Bsmt Full Bath|<p align="left">Discrete|<p align="left">Basement full bathrooms|
|<p align="left">Bsmt Half Bath|<p align="left">Discrete|<p align="left">Basement half bathrooms|
|<p align="left">Full Bath|<p align="left">Discrete|<p align="left">Full bathrooms above grade|
|<p align="left">Half Bath|<p align="left">Discrete|<p align="left">Half bathrooms above grade|
|<p align="left">Bedroom|<p align="left">Discrete|<p align="left">Bedrooms above grade (does NOT include basement bedrooms)|
|<p align="left">Kitchen|<p align="left">Discrete|<p align="left">Kitchens above grade|
|<p align="left">KitchenQual|<p align="left">Ordinal|<p align="left">Kitchen quality|
|<p align="left">TotRmsAbvGrd|<p align="left">Discrete|<p align="left">Total rooms above grade (does not include bathrooms)|
|<p align="left">Functional|<p align="left">Ordinal|<p align="left">Home functionality (Assume typical unless deductions are warranted)|
|<p align="left">Fireplaces|<p align="left">Discrete|<p align="left">Number of fireplaces|
|<p align="left">FireplaceQu|<p align="left">Ordinal|<p align="left">Fireplace quality|
|<p align="left">Garage Type|<p align="left">Nominal|<p align="left">Garage location|
|<p align="left">Garage Yr Blt|<p align="left">Discrete|<p align="left">Year garage was built|
|<p align="left">Garage Finish|<p align="left">Ordinal|<p align="left">Interior finish of the garage|
|<p align="left">Garage Cars|<p align="left">Discrete|<p align="left">Size of garage in car capacity|
|<p align="left">Garage Area|<p align="left">Continuous|<p align="left">Size of garage in square feet|
|<p align="left">Garage Qual|<p align="left">Ordinal|<p align="left">Garage quality|
|<p align="left">Garage Cond|<p align="left">Ordinal|<p align="left">Garage condition|
|<p align="left">Paved Drive|<p align="left">Ordinal|<p align="left">Paved driveway|
|<p align="left">Wood Deck SF|<p align="left">Continuous|<p align="left">Wood deck area in square feet|
|<p align="left">Open Porch SF|<p align="left">Continuous|<p align="left">Open porch area in square feet|
|<p align="left">Enclosed Porch|<p align="left">Continuous|<p align="left">Enclosed porch area in square feet|
|<p align="left">3-Ssn Porch|<p align="left">Continuous|<p align="left">Three season porch area in square feet|
|<p align="left">Screen Porch|<p align="left">Continuous|<p align="left">Screen porch area in square feet|
|<p align="left">Pool Area|<p align="left">Continuous|<p align="left">Pool area in square feet|
|<p align="left">Pool QC|<p align="left">Ordinal|<p align="left">Pool quality|
|<p align="left">Fence|<p align="left">Ordinal|<p align="left">Fence quality|
|<p align="left">Misc Feature|<p align="left">Nominal|<p align="left">Miscellaneous feature not covered in other categories|
|<p align="left">Misc Val|<p align="left">Continuous|<p align="left">Dollar value of miscellaneous feature|
|<p align="left">Mo Sold|<p align="left">Discrete|<p align="left">Month Sold (MM)|
|<p align="left">Yr Sold|<p align="left">Discrete|<p align="left">Year Sold (YYYY)|
|<p align="left">Sale Type|<p align="left">Nominal|<p align="left">Type of sale|
|<p align="left">Sale Condition|<p align="left">Nominal|<p align="left">Condition of sale|
|<p align="left">SalePrice|<p align="left">Continuous|<p align="left">Sale price in dollars|

