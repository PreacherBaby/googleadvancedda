# **Automatidata project**
**Course 2 - Get Started with Python**

Welcome to the Automatidata Project!

You have just started as a data professional in a fictional data analytics firm, Automatidata. Their client, the New York City Taxi and Limousine Commission (New York City TLC), has hired the Automatidata team for its reputation in helping their clients develop data-based solutions.

The team is still in the early stages of the project. Previously, you were asked to complete a project proposal by your supervisor, DeShawn Washington. You have received notice that your project proposal has been approved and that New York City TLC has given the Automatidata team access to their data. To get clear insights, New York TLC's data must be analyzed, key variables identified, and the dataset ensured it is ready for analysis.

A notebook was structured and prepared to help you in this project. Please complete the questions inside and prepare a summary for the data team.

# Course 2 End-of-course project: Inspect and analyze data

In this activity, you will examine data provided and prepare it for analysis.  
<br/>   

**The purpose** of this project is to investigate and understand the data provided.
  
**The goal** is to use a dataframe contructed within Python, perform a cursory inspection of the provided dataset, and inform team members of your findings. 
<br/>  
*This activity has three parts:*

**Part 1:** Understand the situation 
* How can you best prepare to understand and organize the provided taxi cab information?

**Part 2:** Understand the data

* Create a pandas dataframe for data learning, future exploratory data analysis (EDA), and statistical activities.

* Compile summary information about the data to inform next steps.

**Part 3:** Understand the variables

* Use insights from your examination of the summary data to guide deeper investigation into specific variables.


<br/> 
Follow the instructions and answer the following questions to complete the activity. Then, you will complete an Executive Summary using the questions listed on the PACE Strategy Document.

Be sure to complete this activity before moving on. The next course item will provide you with a completed exemplar to compare to your own work. 



# **Identify data types and relevant variables using Python**


### **Exercise Instructions:**


**Complete the following step-by-step instructions to inspect and analyze this NYC taxi dataset.**

This activity will help ensure the information is,

1.   Ready to answer questions and yield insights

2.   Ready for visualizations

3.   Ready for future hypothesis testing and statistical methods

**Follow the instructions and answer questions to complete this activity. Afterward,**

1.   Use the structured notebook provided to help you in this project. Please complete the questions inside and prepare a summary for the data team.

2.  Consider the questions presented  in the [Course 2 PACE strategy document](https://docs.google.com/document/d/1JM7h5MAQkD9uxoUhgpVBeT5R15y85LRaMo30I7bIFdk/template/preview).

3. Write a short Executive Summary using your findings.

4.   Compare your data insights with the provided exemplar to confirm of your approach and results.


Throughout these project notebooks, you'll see references to the problem-solving framework PACE. The following notebook components are labeled with the respective PACE stage: Plan, Analyze, Construct, and Execute.

# **PACE stages** 


<img src="images/Pace.png" width="100" height="100" align=left>

   *        [Plan](#scrollTo=psz51YkZVwtN&line=3&uniqifier=1)
   *        [Analyze](#scrollTo=mA7Mz_SnI8km&line=4&uniqifier=1)
   *        [Construct](#scrollTo=Lca9c8XON8lc&line=2&uniqifier=1)
   *        [Execute](#scrollTo=401PgchTPr4E&line=2&uniqifier=1)

<img src="images/Plan.png" width="100" height="100" align=left>


## PACE: **Plan**

Consider the questions in your PACE Strategy Document and those below to craft your response:

### **Task 1. Understand the situation**

*   How can you best prepare to understand and organize the provided taxi cab information? 

==> ENTER YOUR RESPONSE HERE

<img src="images/Analyze.png" width="100" height="100" align=left>

## PACE: **Analyze**

Consider the questions in your PACE Strategy Document to reflect on the Analyze stage.

### **Task 2a. Build dataframe**
















Create a pandas dataframe for data learning, exploratory data analysis (EDA), and statistical activities.

**Code the following,**

*   import pandas as pd               #library exercise for buidling dataframes

*   import numpy as np                #numpy is imported with pandas

*   df = pd.read_csv('2017_Yellow_Taxi_Trip_Data.csv')

**Note:** pair the data object name "df" with pandas functions to manipulate data, such as df.groupby().

**Note:** As shown in this cell, the dataset has been automatically loaded in for you. You do not need to download the .csv file, or provide more code, in order to access the dataset and proceed with this lab. Please continue with this activity by completing the following instructions.


```python
import pandas as pd

# RUN THIS CELL TO IMPORT YOUR DATA.
df = pd.read_csv('2017_Yellow_Taxi_Trip_Data.csv')
print("done")
```

    done


### **Task 2b. Understand the data - Inspect the data**

View and inspect summary information about the dataframe by coding the following:

1. df.head(10)
2. df.info()
3. df.describe()

Consider the following two questions:

**Question 1:** When reviewing the df.info() output, what do you notice about the different variables? Are there any null values? Are all of the variables numeric? Does anything else stand out?

**Question 2:** When reviewing the df.describe() output, what do you notice about the distributions of each variable? Are there any questionable values?

#==> ENTER YOUR RESPONSE TO QUESTIONS 1 & 2 HERE


```python
df.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>24870114</td>
      <td>2</td>
      <td>03/25/2017 8:55:43 AM</td>
      <td>03/25/2017 9:09:47 AM</td>
      <td>6</td>
      <td>3.34</td>
      <td>1</td>
      <td>N</td>
      <td>100</td>
      <td>231</td>
      <td>1</td>
      <td>13.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>2.76</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>16.56</td>
    </tr>
    <tr>
      <th>1</th>
      <td>35634249</td>
      <td>1</td>
      <td>04/11/2017 2:53:28 PM</td>
      <td>04/11/2017 3:19:58 PM</td>
      <td>1</td>
      <td>1.80</td>
      <td>1</td>
      <td>N</td>
      <td>186</td>
      <td>43</td>
      <td>1</td>
      <td>16.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>4.00</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>20.80</td>
    </tr>
    <tr>
      <th>2</th>
      <td>106203690</td>
      <td>1</td>
      <td>12/15/2017 7:26:56 AM</td>
      <td>12/15/2017 7:34:08 AM</td>
      <td>1</td>
      <td>1.00</td>
      <td>1</td>
      <td>N</td>
      <td>262</td>
      <td>236</td>
      <td>1</td>
      <td>6.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>1.45</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>8.75</td>
    </tr>
    <tr>
      <th>3</th>
      <td>38942136</td>
      <td>2</td>
      <td>05/07/2017 1:17:59 PM</td>
      <td>05/07/2017 1:48:14 PM</td>
      <td>1</td>
      <td>3.70</td>
      <td>1</td>
      <td>N</td>
      <td>188</td>
      <td>97</td>
      <td>1</td>
      <td>20.5</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>6.39</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>27.69</td>
    </tr>
    <tr>
      <th>4</th>
      <td>30841670</td>
      <td>2</td>
      <td>04/15/2017 11:32:20 PM</td>
      <td>04/15/2017 11:49:03 PM</td>
      <td>1</td>
      <td>4.37</td>
      <td>1</td>
      <td>N</td>
      <td>4</td>
      <td>112</td>
      <td>2</td>
      <td>16.5</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>17.80</td>
    </tr>
    <tr>
      <th>5</th>
      <td>23345809</td>
      <td>2</td>
      <td>03/25/2017 8:34:11 PM</td>
      <td>03/25/2017 8:42:11 PM</td>
      <td>6</td>
      <td>2.30</td>
      <td>1</td>
      <td>N</td>
      <td>161</td>
      <td>236</td>
      <td>1</td>
      <td>9.0</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>2.06</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>12.36</td>
    </tr>
    <tr>
      <th>6</th>
      <td>37660487</td>
      <td>2</td>
      <td>05/03/2017 7:04:09 PM</td>
      <td>05/03/2017 8:03:47 PM</td>
      <td>1</td>
      <td>12.83</td>
      <td>1</td>
      <td>N</td>
      <td>79</td>
      <td>241</td>
      <td>1</td>
      <td>47.5</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>9.86</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>59.16</td>
    </tr>
    <tr>
      <th>7</th>
      <td>69059411</td>
      <td>2</td>
      <td>08/15/2017 5:41:06 PM</td>
      <td>08/15/2017 6:03:05 PM</td>
      <td>1</td>
      <td>2.98</td>
      <td>1</td>
      <td>N</td>
      <td>237</td>
      <td>114</td>
      <td>1</td>
      <td>16.0</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>1.78</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>19.58</td>
    </tr>
    <tr>
      <th>8</th>
      <td>8433159</td>
      <td>2</td>
      <td>02/04/2017 4:17:07 PM</td>
      <td>02/04/2017 4:29:14 PM</td>
      <td>1</td>
      <td>1.20</td>
      <td>1</td>
      <td>N</td>
      <td>234</td>
      <td>249</td>
      <td>2</td>
      <td>9.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>9.80</td>
    </tr>
    <tr>
      <th>9</th>
      <td>95294817</td>
      <td>1</td>
      <td>11/10/2017 3:20:29 PM</td>
      <td>11/10/2017 3:40:55 PM</td>
      <td>1</td>
      <td>1.60</td>
      <td>1</td>
      <td>N</td>
      <td>239</td>
      <td>237</td>
      <td>1</td>
      <td>13.0</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>2.75</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>16.55</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 22699 entries, 0 to 22698
    Data columns (total 18 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   Unnamed: 0             22699 non-null  int64  
     1   VendorID               22699 non-null  int64  
     2   tpep_pickup_datetime   22699 non-null  object 
     3   tpep_dropoff_datetime  22699 non-null  object 
     4   passenger_count        22699 non-null  int64  
     5   trip_distance          22699 non-null  float64
     6   RatecodeID             22699 non-null  int64  
     7   store_and_fwd_flag     22699 non-null  object 
     8   PULocationID           22699 non-null  int64  
     9   DOLocationID           22699 non-null  int64  
     10  payment_type           22699 non-null  int64  
     11  fare_amount            22699 non-null  float64
     12  extra                  22699 non-null  float64
     13  mta_tax                22699 non-null  float64
     14  tip_amount             22699 non-null  float64
     15  tolls_amount           22699 non-null  float64
     16  improvement_surcharge  22699 non-null  float64
     17  total_amount           22699 non-null  float64
    dtypes: float64(8), int64(7), object(3)
    memory usage: 3.1+ MB


- The 'tpep_pickup_datetime' and 'tpep_dropoff_datetime' columns here are object-type data; They need to be converted to datetime in order to properly work with time series
- The 'Unnamed: 0' column is supposed to be called 'ID' 
- The 'store_and_fwd_flag' column values can be categorical instead of object to reduce the size of the file


```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>2.269900e+04</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
      <td>22699.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>5.675849e+07</td>
      <td>1.556236</td>
      <td>1.642319</td>
      <td>2.913313</td>
      <td>1.043394</td>
      <td>162.412353</td>
      <td>161.527997</td>
      <td>1.336887</td>
      <td>13.026629</td>
      <td>0.333275</td>
      <td>0.497445</td>
      <td>1.835781</td>
      <td>0.312542</td>
      <td>0.299551</td>
      <td>16.310502</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.274493e+07</td>
      <td>0.496838</td>
      <td>1.285231</td>
      <td>3.653171</td>
      <td>0.708391</td>
      <td>66.633373</td>
      <td>70.139691</td>
      <td>0.496211</td>
      <td>13.243791</td>
      <td>0.463097</td>
      <td>0.039465</td>
      <td>2.800626</td>
      <td>1.399212</td>
      <td>0.015673</td>
      <td>16.097295</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.212700e+04</td>
      <td>1.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>-120.000000</td>
      <td>-1.000000</td>
      <td>-0.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>-0.300000</td>
      <td>-120.300000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>2.852056e+07</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>0.990000</td>
      <td>1.000000</td>
      <td>114.000000</td>
      <td>112.000000</td>
      <td>1.000000</td>
      <td>6.500000</td>
      <td>0.000000</td>
      <td>0.500000</td>
      <td>0.000000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>8.750000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>5.673150e+07</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>1.610000</td>
      <td>1.000000</td>
      <td>162.000000</td>
      <td>162.000000</td>
      <td>1.000000</td>
      <td>9.500000</td>
      <td>0.000000</td>
      <td>0.500000</td>
      <td>1.350000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>11.800000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>8.537452e+07</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>3.060000</td>
      <td>1.000000</td>
      <td>233.000000</td>
      <td>233.000000</td>
      <td>2.000000</td>
      <td>14.500000</td>
      <td>0.500000</td>
      <td>0.500000</td>
      <td>2.450000</td>
      <td>0.000000</td>
      <td>0.300000</td>
      <td>17.800000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>1.134863e+08</td>
      <td>2.000000</td>
      <td>6.000000</td>
      <td>33.960000</td>
      <td>99.000000</td>
      <td>265.000000</td>
      <td>265.000000</td>
      <td>4.000000</td>
      <td>999.990000</td>
      <td>4.500000</td>
      <td>0.500000</td>
      <td>200.000000</td>
      <td>19.100000</td>
      <td>0.300000</td>
      <td>1200.290000</td>
    </tr>
  </tbody>
</table>
</div>



- the 'passenger_count' column has minimum amount of passengers as 0. The values are user-input (driver), so it is expected for them to forget about it.
- the same thing applies for the 'trip_distance' minimum value.
- minimum 'fare_amount' of -120 is a subject to investigate further.
- extreme values like max of the 'fare_amount" 999.

### **Task 2c. Understand the data - Investigate the variables**

Sort and interpret the data table for two variables:`trip_distance` and `total_amount`.

**Answer the following three questions:**

**Question 1:** Sort your first variable (`trip_distance`) from maximum to minimum value, do the values seem normal?

**Question 2:** Sort your by your second variable (`total_amount`), are any values unusual?

**Question 3:** Are the resulting rows similar for both sorts? Why or why not?

*#==> ENTER YOUR RESPONSES TO QUESTION 1-3 HERE


```python
# Sort the data by trip distance from maximum to minimum value

df.sort_values(['trip_distance'], ascending = False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9280</th>
      <td>51810714</td>
      <td>2</td>
      <td>06/18/2017 11:33:25 PM</td>
      <td>06/19/2017 12:12:38 AM</td>
      <td>2</td>
      <td>33.96</td>
      <td>5</td>
      <td>N</td>
      <td>132</td>
      <td>265</td>
      <td>2</td>
      <td>150.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>150.30</td>
    </tr>
    <tr>
      <th>13861</th>
      <td>40523668</td>
      <td>2</td>
      <td>05/19/2017 8:20:21 AM</td>
      <td>05/19/2017 9:20:30 AM</td>
      <td>1</td>
      <td>33.92</td>
      <td>5</td>
      <td>N</td>
      <td>229</td>
      <td>265</td>
      <td>1</td>
      <td>200.01</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>51.64</td>
      <td>5.76</td>
      <td>0.3</td>
      <td>258.21</td>
    </tr>
    <tr>
      <th>6064</th>
      <td>49894023</td>
      <td>2</td>
      <td>06/13/2017 12:30:22 PM</td>
      <td>06/13/2017 1:37:51 PM</td>
      <td>1</td>
      <td>32.72</td>
      <td>3</td>
      <td>N</td>
      <td>138</td>
      <td>1</td>
      <td>1</td>
      <td>107.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>55.50</td>
      <td>16.26</td>
      <td>0.3</td>
      <td>179.06</td>
    </tr>
    <tr>
      <th>10291</th>
      <td>76319330</td>
      <td>2</td>
      <td>09/11/2017 11:41:04 AM</td>
      <td>09/11/2017 12:18:58 PM</td>
      <td>1</td>
      <td>31.95</td>
      <td>4</td>
      <td>N</td>
      <td>138</td>
      <td>265</td>
      <td>2</td>
      <td>131.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>131.80</td>
    </tr>
    <tr>
      <th>29</th>
      <td>94052446</td>
      <td>2</td>
      <td>11/06/2017 8:30:50 PM</td>
      <td>11/07/2017 12:00:00 AM</td>
      <td>1</td>
      <td>30.83</td>
      <td>1</td>
      <td>N</td>
      <td>132</td>
      <td>23</td>
      <td>1</td>
      <td>80.00</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>18.56</td>
      <td>11.52</td>
      <td>0.3</td>
      <td>111.38</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2440</th>
      <td>63574825</td>
      <td>1</td>
      <td>07/26/2017 10:26:58 PM</td>
      <td>07/26/2017 10:26:58 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>162</td>
      <td>264</td>
      <td>2</td>
      <td>5.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>6.80</td>
    </tr>
    <tr>
      <th>15916</th>
      <td>47368116</td>
      <td>1</td>
      <td>06/29/2017 7:30:30 PM</td>
      <td>06/29/2017 7:43:29 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>79</td>
      <td>148</td>
      <td>3</td>
      <td>8.50</td>
      <td>1.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>10.30</td>
    </tr>
    <tr>
      <th>1350</th>
      <td>91619825</td>
      <td>2</td>
      <td>10/30/2017 8:20:29 AM</td>
      <td>10/30/2017 8:20:38 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>193</td>
      <td>193</td>
      <td>1</td>
      <td>2.50</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.66</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.96</td>
    </tr>
    <tr>
      <th>246</th>
      <td>78660848</td>
      <td>1</td>
      <td>09/18/2017 8:50:53 PM</td>
      <td>09/18/2017 8:51:03 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>145</td>
      <td>145</td>
      <td>2</td>
      <td>2.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.80</td>
    </tr>
    <tr>
      <th>17788</th>
      <td>58079289</td>
      <td>1</td>
      <td>07/08/2017 12:54:02 AM</td>
      <td>07/08/2017 12:55:03 AM</td>
      <td>2</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>158</td>
      <td>158</td>
      <td>3</td>
      <td>2.50</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>3.80</td>
    </tr>
  </tbody>
</table>
<p>22699 rows × 18 columns</p>
</div>




```python
# Sort the data by total amount and print the top 20 values

df.sort_values(['total_amount'], ascending = False).head(20)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>8476</th>
      <td>11157412</td>
      <td>1</td>
      <td>02/06/2017 5:50:10 AM</td>
      <td>02/06/2017 5:51:08 AM</td>
      <td>1</td>
      <td>2.60</td>
      <td>5</td>
      <td>N</td>
      <td>226</td>
      <td>226</td>
      <td>1</td>
      <td>999.99</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>200.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>1200.29</td>
    </tr>
    <tr>
      <th>20312</th>
      <td>107558404</td>
      <td>2</td>
      <td>12/19/2017 9:40:46 AM</td>
      <td>12/19/2017 9:40:55 AM</td>
      <td>2</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>265</td>
      <td>2</td>
      <td>450.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>450.30</td>
    </tr>
    <tr>
      <th>13861</th>
      <td>40523668</td>
      <td>2</td>
      <td>05/19/2017 8:20:21 AM</td>
      <td>05/19/2017 9:20:30 AM</td>
      <td>1</td>
      <td>33.92</td>
      <td>5</td>
      <td>N</td>
      <td>229</td>
      <td>265</td>
      <td>1</td>
      <td>200.01</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>51.64</td>
      <td>5.76</td>
      <td>0.3</td>
      <td>258.21</td>
    </tr>
    <tr>
      <th>12511</th>
      <td>107108848</td>
      <td>2</td>
      <td>12/17/2017 6:24:24 PM</td>
      <td>12/17/2017 6:24:42 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>265</td>
      <td>1</td>
      <td>175.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>46.69</td>
      <td>11.75</td>
      <td>0.3</td>
      <td>233.74</td>
    </tr>
    <tr>
      <th>15474</th>
      <td>55538852</td>
      <td>2</td>
      <td>06/06/2017 8:55:01 PM</td>
      <td>06/06/2017 8:55:06 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>265</td>
      <td>1</td>
      <td>200.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>11.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>211.80</td>
    </tr>
    <tr>
      <th>6064</th>
      <td>49894023</td>
      <td>2</td>
      <td>06/13/2017 12:30:22 PM</td>
      <td>06/13/2017 1:37:51 PM</td>
      <td>1</td>
      <td>32.72</td>
      <td>3</td>
      <td>N</td>
      <td>138</td>
      <td>1</td>
      <td>1</td>
      <td>107.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>55.50</td>
      <td>16.26</td>
      <td>0.3</td>
      <td>179.06</td>
    </tr>
    <tr>
      <th>16379</th>
      <td>101198443</td>
      <td>2</td>
      <td>11/30/2017 10:41:11 AM</td>
      <td>11/30/2017 11:31:45 AM</td>
      <td>1</td>
      <td>25.50</td>
      <td>5</td>
      <td>N</td>
      <td>132</td>
      <td>265</td>
      <td>2</td>
      <td>140.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>16.26</td>
      <td>0.3</td>
      <td>157.06</td>
    </tr>
    <tr>
      <th>3582</th>
      <td>111653084</td>
      <td>1</td>
      <td>01/01/2017 11:53:01 PM</td>
      <td>01/01/2017 11:53:42 PM</td>
      <td>1</td>
      <td>7.30</td>
      <td>5</td>
      <td>N</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>152.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>152.30</td>
    </tr>
    <tr>
      <th>11269</th>
      <td>51920669</td>
      <td>1</td>
      <td>06/19/2017 12:51:17 AM</td>
      <td>06/19/2017 12:52:12 AM</td>
      <td>2</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>265</td>
      <td>1</td>
      <td>120.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>20.00</td>
      <td>11.52</td>
      <td>0.3</td>
      <td>151.82</td>
    </tr>
    <tr>
      <th>9280</th>
      <td>51810714</td>
      <td>2</td>
      <td>06/18/2017 11:33:25 PM</td>
      <td>06/19/2017 12:12:38 AM</td>
      <td>2</td>
      <td>33.96</td>
      <td>5</td>
      <td>N</td>
      <td>132</td>
      <td>265</td>
      <td>2</td>
      <td>150.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>150.30</td>
    </tr>
    <tr>
      <th>1928</th>
      <td>51087145</td>
      <td>1</td>
      <td>06/16/2017 6:30:08 PM</td>
      <td>06/16/2017 7:18:50 PM</td>
      <td>2</td>
      <td>12.50</td>
      <td>5</td>
      <td>N</td>
      <td>211</td>
      <td>265</td>
      <td>1</td>
      <td>120.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>5.00</td>
      <td>12.50</td>
      <td>0.3</td>
      <td>137.80</td>
    </tr>
    <tr>
      <th>10291</th>
      <td>76319330</td>
      <td>2</td>
      <td>09/11/2017 11:41:04 AM</td>
      <td>09/11/2017 12:18:58 PM</td>
      <td>1</td>
      <td>31.95</td>
      <td>4</td>
      <td>N</td>
      <td>138</td>
      <td>265</td>
      <td>2</td>
      <td>131.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>131.80</td>
    </tr>
    <tr>
      <th>6708</th>
      <td>91660295</td>
      <td>2</td>
      <td>10/30/2017 11:23:46 AM</td>
      <td>10/30/2017 11:23:49 AM</td>
      <td>1</td>
      <td>0.32</td>
      <td>5</td>
      <td>N</td>
      <td>264</td>
      <td>83</td>
      <td>1</td>
      <td>100.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>25.20</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>126.00</td>
    </tr>
    <tr>
      <th>11608</th>
      <td>107690629</td>
      <td>2</td>
      <td>12/19/2017 5:00:56 PM</td>
      <td>12/19/2017 6:41:56 PM</td>
      <td>2</td>
      <td>23.00</td>
      <td>3</td>
      <td>N</td>
      <td>151</td>
      <td>1</td>
      <td>1</td>
      <td>99.50</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>10.00</td>
      <td>12.50</td>
      <td>0.3</td>
      <td>123.30</td>
    </tr>
    <tr>
      <th>908</th>
      <td>25075013</td>
      <td>2</td>
      <td>03/27/2017 1:01:38 PM</td>
      <td>03/27/2017 1:38:44 PM</td>
      <td>2</td>
      <td>26.12</td>
      <td>4</td>
      <td>N</td>
      <td>138</td>
      <td>265</td>
      <td>1</td>
      <td>100.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>15.00</td>
      <td>5.76</td>
      <td>0.3</td>
      <td>121.56</td>
    </tr>
    <tr>
      <th>7281</th>
      <td>111091850</td>
      <td>2</td>
      <td>01/01/2017 3:02:53 AM</td>
      <td>01/01/2017 3:03:02 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>265</td>
      <td>1</td>
      <td>100.00</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>20.16</td>
      <td>0.00</td>
      <td>0.3</td>
      <td>120.96</td>
    </tr>
    <tr>
      <th>18130</th>
      <td>90375786</td>
      <td>1</td>
      <td>10/26/2017 2:45:01 PM</td>
      <td>10/26/2017 4:12:49 PM</td>
      <td>1</td>
      <td>30.50</td>
      <td>1</td>
      <td>N</td>
      <td>132</td>
      <td>220</td>
      <td>1</td>
      <td>90.50</td>
      <td>0.0</td>
      <td>0.5</td>
      <td>19.85</td>
      <td>8.16</td>
      <td>0.3</td>
      <td>119.31</td>
    </tr>
    <tr>
      <th>13621</th>
      <td>93330154</td>
      <td>1</td>
      <td>11/04/2017 1:32:14 PM</td>
      <td>11/04/2017 2:18:50 PM</td>
      <td>2</td>
      <td>19.80</td>
      <td>5</td>
      <td>N</td>
      <td>265</td>
      <td>230</td>
      <td>1</td>
      <td>105.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>8.00</td>
      <td>2.64</td>
      <td>0.3</td>
      <td>115.94</td>
    </tr>
    <tr>
      <th>13359</th>
      <td>3055315</td>
      <td>1</td>
      <td>01/12/2017 7:19:36 AM</td>
      <td>01/12/2017 7:19:56 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>75.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>18.65</td>
      <td>18.00</td>
      <td>0.3</td>
      <td>111.95</td>
    </tr>
    <tr>
      <th>29</th>
      <td>94052446</td>
      <td>2</td>
      <td>11/06/2017 8:30:50 PM</td>
      <td>11/07/2017 12:00:00 AM</td>
      <td>1</td>
      <td>30.83</td>
      <td>1</td>
      <td>N</td>
      <td>132</td>
      <td>23</td>
      <td>1</td>
      <td>80.00</td>
      <td>0.5</td>
      <td>0.5</td>
      <td>18.56</td>
      <td>11.52</td>
      <td>0.3</td>
      <td>111.38</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Sort the data by total amount and print the bottom 20 values
df.sort_values(['total_amount'], ascending = False).tail(20)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>VendorID</th>
      <th>tpep_pickup_datetime</th>
      <th>tpep_dropoff_datetime</th>
      <th>passenger_count</th>
      <th>trip_distance</th>
      <th>RatecodeID</th>
      <th>store_and_fwd_flag</th>
      <th>PULocationID</th>
      <th>DOLocationID</th>
      <th>payment_type</th>
      <th>fare_amount</th>
      <th>extra</th>
      <th>mta_tax</th>
      <th>tip_amount</th>
      <th>tolls_amount</th>
      <th>improvement_surcharge</th>
      <th>total_amount</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>14283</th>
      <td>37675840</td>
      <td>1</td>
      <td>05/03/2017 7:44:28 PM</td>
      <td>05/03/2017 7:44:38 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>5</td>
      <td>N</td>
      <td>146</td>
      <td>146</td>
      <td>3</td>
      <td>0.01</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>0.31</td>
    </tr>
    <tr>
      <th>19067</th>
      <td>58713019</td>
      <td>1</td>
      <td>07/10/2017 2:40:09 PM</td>
      <td>07/10/2017 2:40:59 PM</td>
      <td>1</td>
      <td>0.10</td>
      <td>5</td>
      <td>N</td>
      <td>261</td>
      <td>13</td>
      <td>3</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.3</td>
      <td>0.30</td>
    </tr>
    <tr>
      <th>10506</th>
      <td>26005024</td>
      <td>2</td>
      <td>03/30/2017 3:14:26 AM</td>
      <td>03/30/2017 3:14:28 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>264</td>
      <td>193</td>
      <td>1</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>5722</th>
      <td>49670364</td>
      <td>2</td>
      <td>06/12/2017 12:08:55 PM</td>
      <td>06/12/2017 12:08:57 PM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>264</td>
      <td>193</td>
      <td>1</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>4402</th>
      <td>108016954</td>
      <td>2</td>
      <td>12/20/2017 4:06:53 PM</td>
      <td>12/20/2017 4:47:50 PM</td>
      <td>1</td>
      <td>7.06</td>
      <td>1</td>
      <td>N</td>
      <td>263</td>
      <td>169</td>
      <td>2</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>22566</th>
      <td>19022898</td>
      <td>2</td>
      <td>03/07/2017 2:24:47 AM</td>
      <td>03/07/2017 2:24:50 AM</td>
      <td>1</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>264</td>
      <td>193</td>
      <td>1</td>
      <td>0.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.00</td>
    </tr>
    <tr>
      <th>1646</th>
      <td>57337183</td>
      <td>2</td>
      <td>07/05/2017 11:02:23 AM</td>
      <td>07/05/2017 11:03:00 AM</td>
      <td>1</td>
      <td>0.04</td>
      <td>1</td>
      <td>N</td>
      <td>79</td>
      <td>79</td>
      <td>3</td>
      <td>-2.50</td>
      <td>0.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-3.30</td>
    </tr>
    <tr>
      <th>18565</th>
      <td>43859760</td>
      <td>2</td>
      <td>05/22/2017 3:51:20 PM</td>
      <td>05/22/2017 3:52:22 PM</td>
      <td>1</td>
      <td>0.10</td>
      <td>1</td>
      <td>N</td>
      <td>230</td>
      <td>163</td>
      <td>3</td>
      <td>-3.00</td>
      <td>0.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-3.80</td>
    </tr>
    <tr>
      <th>314</th>
      <td>105454287</td>
      <td>2</td>
      <td>12/13/2017 2:02:39 AM</td>
      <td>12/13/2017 2:03:08 AM</td>
      <td>6</td>
      <td>0.12</td>
      <td>1</td>
      <td>N</td>
      <td>161</td>
      <td>161</td>
      <td>3</td>
      <td>-2.50</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-3.80</td>
    </tr>
    <tr>
      <th>5758</th>
      <td>833948</td>
      <td>2</td>
      <td>01/03/2017 8:15:23 PM</td>
      <td>01/03/2017 8:15:39 PM</td>
      <td>1</td>
      <td>0.02</td>
      <td>1</td>
      <td>N</td>
      <td>170</td>
      <td>170</td>
      <td>3</td>
      <td>-2.50</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-3.80</td>
    </tr>
    <tr>
      <th>5448</th>
      <td>28459983</td>
      <td>2</td>
      <td>04/06/2017 12:50:26 PM</td>
      <td>04/06/2017 12:52:39 PM</td>
      <td>1</td>
      <td>0.25</td>
      <td>1</td>
      <td>N</td>
      <td>90</td>
      <td>68</td>
      <td>3</td>
      <td>-3.50</td>
      <td>0.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-4.30</td>
    </tr>
    <tr>
      <th>4423</th>
      <td>97329905</td>
      <td>2</td>
      <td>11/16/2017 8:13:30 PM</td>
      <td>11/16/2017 8:14:50 PM</td>
      <td>2</td>
      <td>0.06</td>
      <td>1</td>
      <td>N</td>
      <td>237</td>
      <td>237</td>
      <td>4</td>
      <td>-3.00</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-4.30</td>
    </tr>
    <tr>
      <th>10281</th>
      <td>55302347</td>
      <td>2</td>
      <td>06/05/2017 5:34:25 PM</td>
      <td>06/05/2017 5:36:29 PM</td>
      <td>2</td>
      <td>0.00</td>
      <td>1</td>
      <td>N</td>
      <td>238</td>
      <td>238</td>
      <td>4</td>
      <td>-2.50</td>
      <td>-1.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-4.30</td>
    </tr>
    <tr>
      <th>8204</th>
      <td>91187947</td>
      <td>2</td>
      <td>10/28/2017 8:39:36 PM</td>
      <td>10/28/2017 8:41:59 PM</td>
      <td>1</td>
      <td>0.41</td>
      <td>1</td>
      <td>N</td>
      <td>236</td>
      <td>237</td>
      <td>3</td>
      <td>-3.50</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-4.80</td>
    </tr>
    <tr>
      <th>20317</th>
      <td>75926915</td>
      <td>2</td>
      <td>09/09/2017 10:59:51 PM</td>
      <td>09/09/2017 11:02:06 PM</td>
      <td>1</td>
      <td>0.24</td>
      <td>1</td>
      <td>N</td>
      <td>116</td>
      <td>116</td>
      <td>4</td>
      <td>-3.50</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-4.80</td>
    </tr>
    <tr>
      <th>11204</th>
      <td>58395501</td>
      <td>2</td>
      <td>07/09/2017 7:20:59 AM</td>
      <td>07/09/2017 7:23:50 AM</td>
      <td>1</td>
      <td>0.64</td>
      <td>1</td>
      <td>N</td>
      <td>50</td>
      <td>48</td>
      <td>3</td>
      <td>-4.50</td>
      <td>0.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-5.30</td>
    </tr>
    <tr>
      <th>14714</th>
      <td>109276092</td>
      <td>2</td>
      <td>12/24/2017 10:37:58 PM</td>
      <td>12/24/2017 10:41:08 PM</td>
      <td>5</td>
      <td>0.40</td>
      <td>1</td>
      <td>N</td>
      <td>164</td>
      <td>161</td>
      <td>4</td>
      <td>-4.00</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-5.30</td>
    </tr>
    <tr>
      <th>17602</th>
      <td>24690146</td>
      <td>2</td>
      <td>03/24/2017 7:31:13 PM</td>
      <td>03/24/2017 7:34:49 PM</td>
      <td>1</td>
      <td>0.46</td>
      <td>1</td>
      <td>N</td>
      <td>87</td>
      <td>45</td>
      <td>4</td>
      <td>-4.00</td>
      <td>-1.0</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-5.80</td>
    </tr>
    <tr>
      <th>20698</th>
      <td>14668209</td>
      <td>2</td>
      <td>02/24/2017 12:38:17 AM</td>
      <td>02/24/2017 12:42:05 AM</td>
      <td>1</td>
      <td>0.70</td>
      <td>1</td>
      <td>N</td>
      <td>65</td>
      <td>25</td>
      <td>4</td>
      <td>-4.50</td>
      <td>-0.5</td>
      <td>-0.5</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-5.80</td>
    </tr>
    <tr>
      <th>12944</th>
      <td>29059760</td>
      <td>2</td>
      <td>04/08/2017 12:00:16 AM</td>
      <td>04/08/2017 11:15:57 PM</td>
      <td>1</td>
      <td>0.17</td>
      <td>5</td>
      <td>N</td>
      <td>138</td>
      <td>138</td>
      <td>4</td>
      <td>-120.00</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>0.0</td>
      <td>-0.3</td>
      <td>-120.30</td>
    </tr>
  </tbody>
</table>
</div>




```python
# How many of each payment type are represented in the data?
'''A numeric code signifying how the passenger paid for the trip.  

1= Credit card 

2= Cash 

3= No charge 

4= Dispute 

5= Unknown 

6= Voided trip'''


df['payment_type'].value_counts()
```




    1    15265
    2     7267
    3      121
    4       46
    Name: payment_type, dtype: int64




```python
# What is the average tip for trips paid for with credit card?

df[df['payment_type'] == 1]['tip_amount'].mean() # credit card
```




    2.7298001965279934




```python
# What is the average tip for trips paid for with cash?

df[df['payment_type'] == 2]['tip_amount'].mean() # cash
```




    0.0




```python
# checking if I did something wrong. Nope, no tips with cash
df[df['payment_type'] == 2]['tip_amount'].value_counts()
```




    0.0    7267
    Name: tip_amount, dtype: int64




```python
# How many times is each vendor ID represented in the data?

df['VendorID'].value_counts()
```




    2    12626
    1    10073
    Name: VendorID, dtype: int64




```python
# What is the mean total amount for each vendor?

df[df['VendorID'] == 1]['total_amount'].mean() #1st vendor
```




    16.298118733246966




```python
df[df['VendorID'] == 2]['total_amount'].mean() #2nd vendor
```




    16.32038175193886




```python
# Filter the data for credit card payments only
credit_card = df[df['payment_type'] == 1]

# Filter the data for passenger count only
credit_card['passenger_count'].value_counts()
```




    1    10977
    2     2168
    5      775
    3      600
    6      451
    4      267
    0       27
    Name: passenger_count, dtype: int64




```python
# Calculate the average tip amount for each passenger count (credit card payments only)

credit_card.groupby(['passenger_count']).mean(numeric_only=True)[['tip_amount']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tip_amount</th>
    </tr>
    <tr>
      <th>passenger_count</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2.610370</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2.714681</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2.829949</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2.726800</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2.607753</td>
    </tr>
    <tr>
      <th>5</th>
      <td>2.762645</td>
    </tr>
    <tr>
      <th>6</th>
      <td>2.643326</td>
    </tr>
  </tbody>
</table>
</div>



<img src="images/Execute.png" width="100" height="100" align=left>

## PACE: **Execute**

Consider the questions in your PACE Strategy Document and those below to craft your response:


### **Given your efforts, what can you summarize for DeShawn and the data team?**

*Note for Learners: Your answer should address Luana's request for a summary that covers the following points:* 

* A summary of the data types of each variable

* The number of null and non-null values

* Preliminary insights derived from the data, including:
    * Unusual or questionable values
    * How many of each payment type are represented in the data
    * Mean tip amount for each payment type
    * How many rides each vendor provided
    * Mean total amount for each vendor
    * Mean tip amount for each passenger count (only of those who paid by credit card)



==> ENTER YOUR RESPONSE HERE 

Based on an examination of the dataset, the variables that appear to have the strongest potential for use in developing a predictive model are total_amount and trip_distance. These variables are likely to be valuable due to the insight they provide into the characteristics of a taxi cab ride.
