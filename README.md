# Las Vegas Airbnb EDA

## Table of Contents
* [Introduction](#introduction)
* [Data Review](#data-review)
* [Data Cleaning](#data-cleaning)
* [EDA](#eda)
* [Conclusion](#conclusion)

## Introduction

A popular way for people to find housing when visiting a different city than their own is by using Airbnb. Airbnb is a marketplace that allows users to rent housing accommodations from hosts on the platform. Airbnbs can be found in nearly every city, in this project we will be looking at the listings in Las Vegas and conducting an EDA on the dataset. The dataset for this project was sourced from [Kaggle](https://www.kaggle.com/datasets/kanchana1990/airbnb-las-vegas-listings)

## Data Review

The dataset contains information on hundreds of Airbnbs offered in the Las Vegas area, with 8 variables giving information about the Airbnbs offered.

| Variable      | Description           | 
| ------------- |:---------------------| 
| `roomType`     | The type of accomidation   |
| `stars`     | The average guest rating for the Airbnb   |   
| `address` | The address of the city the Airbnb is located in                             |
| `numberOfGuests`     | The number of guests allowed at the accomodation  |
| `primaryHost/smartName`     | The number of guests allowed at the accomodation  |
| `price`     | The listing price of the Airbnb    |   
| `firstReviewComments` | The comments left on the first review by a guest                           |
| `firstReviewRatings`     | The rating left on the first review by a guest  |

## Data Cleaning

The first step of our EDA process is to clean the data to prepare it for analysis. 

### Renaming Columns

The first step in our data cleaning process is to rename the columns to simpler terms for easier reference and readability.

| Original Variable      | Renamed Variable          | 
| ------------- |:---------------------| 
| `roomType`     | **Property** |
| `stars`     | **stars**   |   
| `address` | **Address**                            |
| `numberOfGuests`     | **Guest** |
| `primaryHost/smartName`     | **Host**  |
| `price`     | **price**  |   
| `firstReviewComments` | **Review**                  |
| `firstReviewRatings`     | **Rating**  |

### Removing unnecessary columns

The second step in our data-cleaning process was to remove any unnecessary columns. In this case, the price column was received as it was filled with null values.

### Standardizing values

The third step in the data-cleaning process was standardizing the values so duplicate values could be removed. As there were multiple addresses labelled as different when they were the same. To do so, trailing and white spaces were removed and the format was standardized by having the values all become lowercase.

### Interpolate

In case there were any missing values we just interpolated to fill in the data using the past information

## EDA

### Aggregated stars 

The graph shows the distribution of ratings for Airbnbs.

![image](https://github.com/jidafan/Las-Vegas-Airbnb-EDA/assets/141703009/d37efc65-f7ca-41fd-bbd1-12c3b91bae7b)

### Heatmap

The heatmap shows the correlation between three different columns, stars, ratings and guests.

![image](https://github.com/jidafan/Las-Vegas-Airbnb-EDA/assets/141703009/f47a3a04-0e4c-4ca4-b704-006add114989)

### Barplot of property type vs rating

The barplot shows the rating for property type vs rating

![image](https://github.com/jidafan/Las-Vegas-Airbnb-EDA/assets/141703009/52e744bb-68c9-4015-9484-40687117cb4d)

### Number of guests vs stars

The barplot shows the number of guests versus the number of stars for the Airbnb hosting
 
![image](https://github.com/jidafan/Las-Vegas-Airbnb-EDA/assets/141703009/41f764c3-71b7-4b87-948b-f151ab965501)

## Conclusion

