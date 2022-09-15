## Project 3 - DATA VISUALIZATION  OF FORD GO-BIKE SYSTEM

### Introduction

This dataset provides information about individual rides made in a bike-sharing system in the San Francisco Bay Area. The dataset has 183412 rows and 16 columns.

The code to this project can be found  in this [here](https://github.com/Eben-Success/Udacity_Data_Analysis_Projects/tree/master/Project%203)

The project is divided into four stages:
- [Prelimary Investigations](#investigation)
- [Data Wrangling and Feature Engineering](#wrangling)
- [Univariate Data Analysis](#univariate)
- [Bivariate Data Analysis](#bivariate)
- [Multivariate Data Analysis](#multivariate)


### <a id="investigating">Prelimary Investigation</a>
In the prelimary process, I used the ```df.isnull().sum()``` to determine the number of missing values in the dataset. There were mssing values in  in start_station_id, start_station_name, member_birth_date, member_year, and member_gender.

Also, there were no duplicated values in the dataset.

### <a id="wrangling">Data Wrangling and Feature Engineering.</a> 
I replaced the missing values with the  mode of the dataset.
I converted the following :
```start_time```  and ```end_time``` into datetime.

```start_station_id```,```end_station``` and ```bike_id``` to strings.

 ```user_type```  and ```member_gender``` to category.

```duation_sec``` into ```duration_min```.

I also calculated the recent ages of the user by using the code: ```df['member_age'] = 2021 - df['member_birth_year']```

Finally, I separated the   ```start_time``` into ```start_hour```,```start_day```  and  ```start_month``` 



### <a id="univariate">Univariate Exploratory Data Analysis</a>

In the univariate process, I answer the following questions through visualizations of bar graph, histogram, boxplot and violinplot.

- Which age group rented the most bikes?
- Which day has the most trips?
- Which duration range occurs the most frequently?
- Who are the major users of the bikes? (Customers or Subscribers)

After careful investigation, I made the following deduction:
- The hours of 17, and 08 have the most bike rentals, with over 2000 trips.

- Most people rented bikes on the Thursday. The total amount of bikes rented on the Thursday was 35000. This is followed by Tuesday, which amount a total of over 31000 rentals. On Friday,  a total amout of approximately 29000 rentals were made. The least of the rentals were made on Sunday and Saturday.
- Majority of the users between the ages of 30 and 40 years.
- Most trips have duration less than 10 minutes
- The duration of trips take huge amount of values and is denser at the left. So, I looked at it in log transform and found that peak occurs at 600 seconds starting from 0 and then distribution starts to drop and does not regain any more peak value.

### <a id="bivariate">Bivariate Exploratory Data Analysis</a>
Similarly, in the bivariate process, I answer the following questions through visualizations of bar graph, histogram, boxplot and violinplot.

- Which day of the week has the most average trips duration?
- Which the trip duration of each age group?
- What isthe age range of different user types?
- What is the age range of different genders?

After careful investigation, I made the following deduction:
- Most people hire bikes on the weekends (Sunday and Saturday).
- Most the customers are between the ages of 30 and 39. While the age range of  majority of subscribers is 30 and 41 years. 
- The median ages of both male and females are identical. 


### <a id="multivariate">Multivariate Exploratory Data Analysis</a>

Likewise, with the multivariate analysis, I found answers to the following questions through visualizations of bar graph, histogram, boxplot violinplot:
- What is the relationship between Weekdays, Average Duration and User Gender?
- Which gender have the most average trip duration among weekdays?
- Were there features that strengthened each other?
- Which user_type and member_gender took the most trip?

After careful investigation of the relationship between the variables, I concluded the following:
* The  "other" gender have the largest median accross board.
* "Other" gender have the most average duration trip from Monday to Sunday. They have the highest duration on Sunday.
* From the chart, it confirms that the "other" user_type spend more duration_min on trips and they also occur majority of the users.

#### Summary
* Bike rentals is prominent among subscribers rather than customers. This implies, subscribers gets discounts or special rates.

* Both subscribers and customers often go a short trip. It seems to be common in the area. 

* The "Other" gender, after the multivariate data analysis seems to be more active in bike rentals than males and females.




