# ML for Business project from Practicum by Yandex
## Well_profitability_estimation_using_bootstrapping

### Goal

- Develop a linear regression model for the OilyGiant mining company that would analyze oil well parameters in each of the three selected regions and predict the volume of reserves in the new wells for each region;
- Based on these predictions, pick the region with the highest total profit and the lowest risk of losses.

### This project's repo includes the following files:

- The project's jupyter notebook (Well_profitability_estimation_using_bootstrapping.ipynb);
- A pdf format of the notebook (Well_profitability_estimation_using_bootstrapping.pdf);
- Input data (geo_data_0.csv, geo_data_1.csv, geo_data_2.csv);
- Project description from Practicum (ML_for_Busines_project_description.pdf).

### This project includes the following steps:

1. Descriptive statistics;
2. Model development for each region;
3. Profit calculations;
4. Risk assessment.

### Based on the analysis we have come to the following conclusions:

- **Model development**

Each of the 3 models' RMSE turned out to be lower than the respective baseline RMSE, so the models are better than the average estimate but not much better, except for the model in Region 1: it has an error of less than 1 thousand barrel. However, in this region the average predicted volume of reserves was much lower than in the other two regions.

Then we calculated the percentage by which the model is off compared to the average predicted volume of reserves. The error is quite high (over 40%) in regions 0 and 2 and very low (only 1%) in region 1. Overall, the actual and predicted volumes of reserves are very close in all 3 regions.

- **Profit calculations**

First, we calculated the volume of reserves sufficient for developing a new well without losses (a break-even point). The minimum volume of reserves per well in the new region must be 111.11 thousand barrels in order to break even.

Each of the 3 regions' average volume of predicted reserves is lower than this number. If we were to randomly take 200 wells in each region we would be at a loss, on average. To be able to make profit, let's select the most profitable wells in each region and see if the total reserves will cover the development cost.

Then we estimated the **profit distribution for the top 200 wells in each region**. The biggest part of the profit range for all 3 regions is above the break-even point. However, region 1 contains the most positive values. Based on that, we suggested that Region 1 should be selected for development of oil wells. 

- **Risk assessment**

The company's requirement for a new region is to have the risk of losses lower than 2.5%. First, we estimated the 95% confidence interval (CI) that the profit will fall into a particular range. Then we calculated the risk of losses for each region.

The risks of losses for regions 0 and 2 are much higher than the excepted 2.5%. Besides, with the 95% confidence we can expect the profit from Region 1 to be only positive, unlike for the two other regions.

These results confirmed our previous conclusion: 

**Region 1 is the best candidate for the future development of oil wells because it has the highest total profit and the lowest risk of losses**.

### The logbook of this project can be found [here](https://docs.google.com/spreadsheets/d/1SrGdReexaSEomJGS6yR6cRwJtHA_XqpprnLaE7B6Ayg/edit#gid=235288859) (ML for Business).
Total time spent on the project: 11.3 hours with a daily average of 1.88 hours working for 6 days.
