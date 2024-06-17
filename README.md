# Time-Series-Analysis

**Time Series Analysis and Anomaly Detection**

**Introduction**

This project aims to develop a solution for anomaly detection on time series sensor data using ARIMA models for forecasting. The input data consists of sensor readings collected at a granularity of 1 second. The project focuses on extracting and analyzing data related to Stand 13-18 region columns.

**Prerequisites**

-   Basic knowledge of Python programming
-   Understanding of time series analysis and ARIMA models
-   Familiarity with InfluxDB and Grafana (for data storage and visualization)
-   Access to a remote server for InfluxDB setup

**Project Overview**

The project involves the following steps:

1.  Setting up an InfluxDB remote server.
2.  Pushing input sensor data to the InfluxDB database.
3.  Applying ARIMA model for time series forecasting.
4.  Detecting anomalies in the time series data.
5.  Visualizing the sensor data, forecasted values, and detected anomalies using Grafana.

Introduction
------------

This project aims to develop a solution for anomaly detection on time series sensor data using ARIMA models for forecasting. The input data consists of sensor readings collected at a granularity of 1 second. The project focuses on extracting and analyzing data related to Stand 13-18 region columns.

Prerequisites
-------------

-   Basic knowledge of Python programming
-   Understanding of time series analysis and ARIMA models

Data Preprocessing
------------------

1.  Extract columns related to Stand 13-18 region from the regions_pickle file.
2.  Dropped the data points containing NAN and infinity values to remove the noise.
3.  Dropped the constant column

**Data Analysis**

1. Dataset is visualized using charts and plots.

2. ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image002.png)Dataset is checked for being stationary or not using rolling statistics and plotting the result.

|  |
|  | ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image005.png) |

**Time Series Forecasting Using ARIMA**

ARIMA Model is fitted on the dataset column by column

1. Firstly, the model is fitted on the very first column and the result is evaluated.

![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

**![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image013.png)**

2. The result for the first column is visualized

|  |  |  |  |  |  |  |  |
|  | ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png) |
|  |  | ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png) |
|  |
|  |
|  |  | ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png) |
|  |  |  | ![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image021.png) |
|  |

**3. **The same model is fitted for all the columns of the dataset**.**

**Anomaly Detection**

1. The residual is calculated for each of the columns fitted on ARIMA model.

2. A threshold value is defined for the anomaly detection

3. Anomaly detection is applied for the values higher than the defined threshold

![](file:///C:/Users/kumar/AppData/Local/Temp/msohtmlclip1/01/clip_image023.png)

**References**

[Jupyter Notebook](https://colab.research.google.com/drive/1eqmtHMkVo05vnOeiaAFpiBR_b9wEyRQ2?usp=sharing)

[Github Repository](https://github.com/kumarprakhar14/Time-Series-Analysis)
