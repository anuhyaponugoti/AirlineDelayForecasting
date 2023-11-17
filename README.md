# AirlineDelayForecasting

Link to data: https://drive.google.com/drive/folders/1YYkbN0tI-0kj5_r3lnqD2AEeyDqQGCqB?usp=sharing
Utilizing a Long-Short Term Memory Model to predict flight departure delay times.

## Contents
SRC folder - containing source code for our EDA and model.

FIGURES folder - containing figures/visualizations of our data.

LICENSE.md - MIT License.

README.md - The current file.

More details below.

## SRC
DS 4002 Dataset/EDA - Code files containing our initial EDA and visualizations.
Project3.ipynb - Jupyter Notebook for EDA with visuals and model training


### Installing/Building the model
Make sure you have the latest version of python installed, with a IDE capable of opening jupyter notebooks. VSCode/Google Colab both work. Make sure all necessary libraries are installed as well. Most should be automatically installed once our code is run. From there, copy the dataset from our drive link to the same location as Project3.ipynb. 

### Usage of the code
Each code block can be run in sequential order, and the model should work. Training time may vary depending on dataset size and number of epochs.

## DATA
Data (delta.csv, southwest.csv, spirit.csv) is stored in the in the Project3 folder in the [Google Drive link](https://drive.google.com/drive/folders/1YYkbN0tI-0kj5_r3lnqD2AEeyDqQGCqB).

| Column                       | Type   | Description                                                      |
|------------------------------|--------|------------------------------------------------------------------|
| Carrier Code                 | string | A short 2-letter code identifying the airline                    |
| Date                         | string | A string representing the date of the flight in month/day/year format |
| Destination Airport          | string | A 3-letter code that represents the flight’s destination airport  |
| Scheduled departure time     | string | The time that the flight was scheduled to depart in 24-hour format |
| Actual departure time         | string | The actual time the flight departed in 24-hour format              |
| Departure delay               | float  | The difference between scheduled departure time and actual departure time. The total number of minutes the flight was delayed |
| Delay Carrier                 | float  | The number of minutes that the flight was delayed due to the carrier |
| Delay Weather                 | float  | The number of minutes that the flight was delayed due to weather   |
| Delay National Aviation System | float | The number of minutes that the flight was delayed due to the National Aviation System (airport operations, air traffic control, etc) |
| Delay Security                | float  | The number of minutes that the flight was delayed due to security  |
| Delay Late Aircraft Arrival   | float  | The number of minutes that the flight was delayed due to the aircraft arriving late |


Data was split into a training set and testing set for a total of 27438 rows. The training set contained 19,206 rows and was used to train the model. The testing set contained 8232 rows and was used to test the results of the model.

## FIGURES
| **Figure**       | **Description**     | **Takeaways** |
|--------------|-----------|------------|
| Sampling of Traffic Sign Images | Display of some images from the data set | There are a multitude of sign types, which implies that our data is varied. There are also several varied environments on the road where traffic signs might not be readily apparent. The time of day in these images varies as well, but the lighting is generally bright enough to read the signs. The languages on each sign varies as well, so our model will be predicting road signs from all over the globe rather than locally, which could potentially lower accuracy due to increased class types. |
| Histogram of Image Height | Histogram displaying the distribution of image heights in the data set  |   A majority of pictures have a height around 2500px or 3000px, with a significant gap between those to bins. This is due to a lack of picture sizes that fit a height between 2500-3000px. |
| Histogram of Image Width | Histogram displaying the distribution of image widths in the data set   | Image widths are more closely grouped together from the 3000-5000px range. This not only shows that images are typically wider on average, by comaring the distributions to the image hieght graph, but it also reveals that images tend to fit a more normal distribution pattern in terms of width. |
| Training Accuracy of the Model | Graph of training accuracy of model as the number of epochs increases | The training accuracy increases from around 0.50 to around 0.75 as as the number of epochs increases from 0 to 45. |
| Training Loss of the Model | Graph of training loss of model as the number of epochs increases | The training loss decreases from around 2.4 to around 0.85 as the number of epochs increases from 0 to 45. |

## REFERENCES
[1] Bureau of Transportation Statistics, “Detailed Statistics Departures,” Bts.gov, 2017.
https://www.transtats.bts.gov/ONTIME/Departures.aspx

[2] “Flight delays, cancellations could continue for a decade amid airline workforce shortage- CBS News,” www.cbsnews.com, Jul. 25, 2023.https://www.cbsnews.com/news/the-future-of-flying-more delays-more-cancellations-more-chaos/

[3] S. Saxena, “What is LSTM? Introduction to Long Short-Term Memory,” Analytics Vidhya, Mar. 16, 2021. https://www.analyticsvidhya.com/blog/2021/03/introduction-to-long-short-term-memory-lstm/#:~:text=LSTM%20(Long%20Short%2DTerm%20Memory

[4] B. Or, “The Exploding and Vanishing Gradients Problem in Time Series,” Medium, Oct.22, 2020. https://towardsdatascience.com/the-exploding-and-vanishing-gradients-problem-in-time-series-6b87d558d22

[5]	“Flight delays, cancellations could continue for a decade amid airline workforce shortage - CBS News,” www.cbsnews.com, Jul. 25, 2023. https://www.cbsnews.com/news/the-future-of-flying-more-delays-more-cancellations-more-chaos/ 


### Acknowledgements
Professor Alonzi

Harsh Anand (TA)

Group12

### Previous Works
MI1: https://docs.google.com/document/d/1moaSiqyytJEJk_6fhaEO-GuXVGYF43t0tLwQ-K9HVQM/edit

MI2: https://docs.google.com/document/d/1bKP0BxPHBmJ3jrv7_dIAYwWdX-xw9997Z_yWi2381MM/edit

This project is licensed under the terms of the MIT license.
