<h1>Analysis and Prediction of Aquifer Levels Using Weather Conditions Data</h1>
<img width="1418" height="796" alt="image" src="https://github.com/user-attachments/assets/e43b4d01-9657-4e4a-a3d4-e0b863e73097" />

<h2>Introduction</h2>
PNJB is honored to participate in the 2023 Data Science Competition organized by the Analytics and Information Systems Club and the Kansas Data Science Consortium at the University of Kansas.
This analysis is the team’s attempt to predict aquifer level recorded by Viaanix at the Ryan and Eugene Goering Water Technology Farm mainly in R. A general method involves fitting different simple models before comparing them on a variety of criteria. There exist one limitations in data source although they do not deviate the suggest results from being optimal in this contex

<h2>Methods</h2>
The readers can expect a thorough process from deciding which data to collect, preparing and cleaning the data, performing exploratory data analysis, examining the data’s time series characteristics, and conducting a variety of model fittings to find the optimal solutions.
We carefully studied the data with graphical and technical examinations of the variables. Certain cleaning steps were applied to issues that were detected to improve data quality.
The analysis explores the possibility for linear regression and time series regression as the potential solutions. It also combines three other model engines to conduct a thorough comparison and error test.

<h2>Analysis</h2>

<b>Data Preparation</b> 
<br />
The proprietary data owned by Viaanix at the Ryan and Eugene Goering Water Technology Farm consists of three variables. Timestamp, later renamed as datetime and date, is the time index that keeps track of the observed data every few minutes from September 01 to December 22, 2022. Well Depth, later renamed as depth, is the distance (in feet) from the ground surface to the surface of the aquifer. An 80 feet well depth means the surface of the water is 80 feet below the earth surface. We convert this series to negative values to reflect the water surface being underground (below 0). ACI1_mA, later renamed as current, is the water current observed at the aquifer. rssi. later renamed as sensor, is the signal strength of the sensor at the observation site.
We performed a merge of the four data sets, renamed the variables, performed calculation on depth, and ensured all date and time variables are in consistent format. This data set does not have missing values but contains 5 duplicated values. We went ahead and removed those observations.
We added a period attribute to denote different stages of a day as night, morning, afternoon, and evening. The team hypothesized there may be a daily seasonal pattern in the data. We will perform a linear regression to testify this.
<br />
<br />
<img width="80%" height="70%" alt="image" src="https://github.com/user-attachments/assets/8362b3b3-caf5-498f-9733-f665655d096a" />

<img width="80%" height="70%" alt="image" src="https://github.com/user-attachments/assets/09f3d71f-974f-4256-bab1-4d29ea50b98e" />
<br />
<br />
The following visualizations depict variables depth and current over time. The two variables seem to share a strong correlation in movement. This is noted for later analysis. Apparently, well depth from September to mid-October of 2022 fluctuated more robustly than that after mid-October. The team is interested in learning why this phenomenon happened.

<br />


