# Forecasting-Springtime-Frost-Risk
The code aims to forecast frost events during spring, which typically occur at night when the soil becomes warmer than the sky and consequently loses heat. As a result, plants can suffer damage caused by frost. This model attempts to predict such events by using the most recent temperature and relative humidity values recorded before sunset.

The explanation of the code is written in Italian within the .ipynb file, so I will explain how it works here.

I added two CSV files (temperature and relative humidity), which are required for the code to run properly. In the first part of the code, I rename the columns as desired and then merge the two files.

Once merged, I account for the sunset time, which changes throughout the frost season (from February until the end of April). Sunset time depends on latitude and longitude; in my code, I account for possible locations within Italy.

After adjusting for the changing sunset times during the season, the class starts an iterative method that uses past temperature and relative humidity data. First, the class makes an initial estimate of the nighttime temperature. Then, this estimate is compared with the actual data, and depending on the difference, the parametric values a, b, and c are adjusted iteratively until the error between the estimated and the real values is minimized.
