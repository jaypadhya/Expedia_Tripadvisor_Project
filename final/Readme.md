
# EXPEDIA TRIPADVISOR PROJECT

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/final_logo.png"></img>



In the hospitality domain, there are two of the most competing websites that look for maximum user bookings, the first one is Expedia and next is Tripadvisor. The scope of the project is to include Three most significant forms of analysis


# DATA STORING AND GATHERING:

There are three sources of Data in my project :-

1) EXPEDIA CSV DATASET

2) EXPEDIA JSON DATA from API KEY 

3) TRIPADVISOR Web scraped Data 


# DATA ANALYSIS :

# 1 : Exploratory Analysis:

- This includes using the Expedia CSV Datasets containing columns related to user's location and it's uniqueid, Hotel Country and it's unique id, hotel ratings, prices for hotel and marketing channels. I have performed exploratory analysis to find unique features from this dataset. 

# 2 : Sentimental and keyphrase Analysis

- This includes using Expedia's API key and Tripadvisor Web scraping using Selenium for fetching reviews across atleast 20+ webpages for 50+ hotels. The scripts and instructions for Web Scraping are mentioned in another file. The Data was then worked upon to combine reviews across both Datasets (Expedia and Tripadvisor) and then using NLTK and NLTK API's we calculate Sentimental Scores across comments from both TripAdvisor and Expedia. The final output is based on "LABEL" which signifies the overall feeling as - Positive, Neutral and Negative.

- Furthermore, I have then used Microsoft API calls for performing Sentimental analysis across every comment on Expedia and Microsoft API calls for performing Key Phrase Extraction for every Expedia comment and written to a CSV so that we can now use this CSV in combination with the exploratory dataset and provide the user various options to choose his destination. 

# 3 : Recommendation Analysis

- Combining the outputs of these two analysis, I have made a unique dataset that comprises using both the analysis and then recommending the user which hotel he should be booking. The user will now have a choice to select hotels based on many features like Sentimental scores, Key phrases, OSAT (Overall Recommendation Scores), Text reviews and aggregated Ratings 


-----------------------------------------------------------------------------------------------------------

# Analysis 1 - Exploratory Analysis

- We use the CSV datasheet and perform 6 different analysis to find conclusions across every six of them

We divide our analysis in following parts:

**A) Quarterly Analysis** : Count bookings, deals, browsing activities and find unique relationships.

**B) Monthly Analysis** : Count bookings, deals, browsing activities and find unique relationships

**C) Weekly Analysis** : Count bookings, deals, browsing activities and find unique relationships

**D) Effective marketing channel** : Finding the most effective marketing channel over Time period

**E) Loyal/Runaway Customer Booking Pattern** : Analysing relation between ratings and Booking price paid

**F) Hotel Pricing Segmentation** : Understanding the price ranges and dissecting hotels into groups

# A) Quarterly Analysis :

**Step 1 : Identifying the data **
- Reading through the CSV Datasets and understanding users booked vs Users not booked
- Using Pandas functionalities to get Quarter, Month, Day and Hour of the week when the customer booked the hotel.
- Drill down to get all data fro four quarters and perform various analysis like hotel booking counts. children and adult booking, ratings for hotels, revenues across each quarters, most effective marketing channel and deals booking.

In this step, I have performed following steps to get the result

- Looped the data and stored in dataframe and used pandas functionalities to make dataset have columns like Quarter, month, days of the week and hours of the day
- On analysing the counts, I came to conclude that booking was grouped by on whether they booked ("1") or they did not ("0") to understand how many users booked and how many did not. I concluded the following graph

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis1_userBrowsing_userBooking.png"></img>

# Conclusion:  Thus we have 50%-50% chances for converting one from browsing to booking. Let us now analyse the following points


# A) Quarterly Analysis :

**Step 2 : Further Drill down**
- User browsing/Booking per Quarter,  per Month and per Hour to analyse highly browsed /booked quarter with room searches, adult and children booking pattern

- User Booking on packages, bookings through mobile and most effective marketing channel per continent, per country to per city to understand trends

In this step, I have performed following steps to get the result
- I gathered only those columns needed for drilling down over Quarterly analysis and used Cufflinks, Matplotlib and Plotly offline to show the graphs. Using the finctionalities of these libraries in unique way, I could achieve a complete drill down analysis across every quarters 

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_hotel_booking_counts.png"></img>

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis1_2_quarterly_analysis.png"></img>

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis1_3_quarterly_analysis_zoom.png"></img>

** We can zoom in and check what the data looks like **

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_4_quarterly_analysis_zoom.png"></img>

# Conclusion :
- We had seen from the dataframes that Quarter 2 has maximum Total Browsing activity and Quarter 4 has least. We will analyse the booking pattern across all 4 quarters.
- We see that Quarter 2 has maximum Adult booking rooms with highest bookins  and Quarter 4 has least bookings. 


**Insights** : Clearly we can understand that **less browsing is lesser booking** as Quarter 4 had least browsing

# Quarterly Analysis :

**Step 3 : Deeper : Drilling inside Quarters for more information**
- Drill down to find monthly representation of revenues and find month with highest revenues and lowest revenues
- Drill down to find week days with highest revenues and lowest revenues across all 4 quarters to find best day to book


In this step, I have performed following steps to get the result
- I fetched all the columns from Months and performed a Groupby on month to find the revenues across each month and obtained the following result


<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_9_monthly_analysis_1.png"></img>

# Quarterly Analysis :

**Step 4 : Deeper : Drilling inside months and Days to find highest revenue grossed**
- Drill down to find monthly representation of revenues and find month with highest revenues and lowest revenues
- Drill down to find week days with highest revenues and lowest revenues across all 4 quarters to find best day to book


In this step, I have performed following steps to get the result
- I drilled down to find more details about which would be the best day to book across all 4 quarters so we can be productive on that day for better results. These were the results  

**Quarter 1 - Best day of the week**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_10_quarterwise_q1_best_day_week.png"></img>

**Quarter 2 - Best day of the week**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_10_quarterwise_q2_best_day_week.png"></img>

**Quarter 3 - Best day of the week**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_10_quarterwise_q3_best_day_week.png"></img>

**Quarter 4 - Best day of the week**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_10_quarterwise_q4_best_day_week.png"></img>

- We can see that we can divide the Quarters to corresponding box plots to derive meaninful relationships between them

# B) Monthly Analysis :

**Steps :**
- Reading through the CSV Datasets and understanding users booked vs Users not booked
- Drill down to get all data fro four quarters and perform various analysis like hotel booking counts. children and adult booking, ratings for hotels, revenues across each quarters, most effective marketing channel and deals booking.

In this step, I did the following analysis
- I went across months and found out features that provide me quantitative picture about my data
- Using Cufflings, Matploblib inline and Iplots we can make an interactive plots offline and can zoom in, zoom out, select axis ,deselect axis and even scroll across a huge graph to get more indepth details  


```python

```

** Overall 12 month picture of bookings, children-adult counts, mobile deals used**

 <img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_11_monthly_analysis_1.png"></img>

** We can only use the features of cufflinks and see how the things look like.**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_11_monthly_analysis_2_features.png"></img>

- Monthly Unbooked Counts
<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_1_monthly_unbooked_pricepaid_histogram.png"></img>

# Conclusion : Thus we can conclude that March had most number of unbooked hotels with December as most booked ones 

# C) Hourly Analysis :

**Steps :**
- Drill down to get all data from four quarters and perform groupby on Hours to analyse like hotel booking counts. children and adult booking, ratings for hotels, revenues across each quarters, most effective marketing channel and deals booking.

In this step, I did the following analysis
- I went across hours and found out features that provide me quantitative picture about my data
- Using Cufflings, Matploblib inline and Iplots we can make an interactive plots offline and can zoom in, zoom out, select axis ,deselect axis and even scroll across a huge graph to get more indepth details  

** Overall 24 hours of bookings, children-adult counts, mobile deals used**

 <img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_11_hourly_analysis_1_hover.png"></img>

** We can only use the features of cufflinks and see how the things look like.**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_11_hourly_analysis_2_drilldown_11hours.png"></img>

# D) **Effective marketing channel** : Finding the most effective marketing channel over Time period


**Analysing Effectiveness of Mobile usage, Package deal booking and most effective marketing channels across continent, country, city and find out the best times for booking**

**Steps:**
- Analyse the best performing Marketing channel for booking and plotting the same
- Analyse which marketing channels worked best in which quarters
- Compare all four quarters 

In this step, Idid the following:
- I iterated over the dataset and found which marketing channel was most used and how many bookings it could get.
- I even drilled down to find the performance of marketing channels across each quarter  

** BECAUSE THE DATA SCALE WAS LARGE, WE NEEDED BOKEH LIBRARY SO WE CAN SCROLL THE LINE PLOTTTED AND FIND THE NUMBERS ** 

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_12_marketing_channels_bokeh_interactive.png"></img>

# Conclusion : Marketing channel 10 is most successful channel in all of the booking counts across the year and Channels 6,7,8 were highly ineffective as comparatively, the user bookings through these 3 channels were least


**Now we will drill down to understand marketing across 4 quarters and conclude on our observations**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_7_effective_marketing_q1_q2.png"></img>

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_8_effective_marketing_q3_q4.png"></img>

# Conclusion : Thus we compared Marketing channels across each quarters and understand their patterns

# E) **Loyal/Runaway Customer Booking Pattern** : Analysing relation between ratings and Booking price paid


- In this step, I iterated over the patterns across booking and non booking to classify customers as loyal (most booking) and runaway (not booking)
- I also made a CSV files having a list of loyal/runaway customers, marketing channles used, their respective countries and cities so we know their location and based on their marketing channels, effective action is possible

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_5_loyalty_customers.png"></img>

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis1_6_runaway_customers.png"></img>

# Conclusion : We can clearly see that if the ratings for the hotel was better, they did not hesistate to book. Runaway users did not book through Expedia meaning there are few slipaway that Expedia needs to understand. Also, users with negative ratings never booked. 

# F) **Hotel Pricing Segmentation and Rating segmentation** : Understanding the price ranges and dissecting hotels into groups 

** Steps **
- Read the data and analyse to find overall sum of ratings for each hotel 
- Read the data and analyse to find overall sum of prices for each hotel 
- Find the median, mode and mean to find a dissecting point and then classify a hotel based on the mid value

In this analysis, I found the mean, median and mode for pricing and then decided what will be the value based on which the hotel will be segmented as **"Economy" or "Luxury"**

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis1_13_pricepaid_histogram.png"></img>

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis1_13_2_pricepaid_kde.png"></img>

----------------------------------------------------------------------------------------------------------------------------



# Before Starting, I scraped the Tripadvisor webpages using Selenium so please install it on computer. I have provided the EXE file in folder
# Once you consider all settings, please ensure that you get an image below and your selenium is installed correctly - It will fetch 20+ pages if it finds for a particular hotel, else it will iterate over next set of hotels. Please refer to Web scraping Notebook page for knowing how I coded for fetching Tripadvisor Reviews

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/images_hitting_the_URL.png"></img>

----------------------------------------------------------------------------------------------------------------------------

# Analysis 2 : Sentimental and Text Analysis  


# Note : Please refer to Tripadvisor folder as it contains the scraped pages and data folder contains the JSON file  
We divide the analysis in Four Parts :-

A) Find the **Overall Satisfaction Score (OSAT = Average of all scores)** from all types of scores given by real time customer revwiews but keeping number of reviews in option.

B) Find **Hotel IDs** from **CSV** and collect reviews of hotels from **TripAdvisor API key call** and **Expedia web scraping.**(TripAdvisor does not provide API key for research purpose and one has to purchase for one year period So we scrape the data.)

C) Perform **Sentimental Analysis** using **NLTK and NLTK API** for both reviews on Tripadvisor and Expedia to understand what customers say on two of the most heavily used websites.

D)  Perform **Sentimental Analysis** using Microsoft Cognitive Sentimental API to have an overall setomental score and **Text Analysis** using Microsoft Cognitive KeyPhrase API to have top three key words used from Expedia API data across all Expedia hotels  

E) We store this data for analysis 3 - User based recommednation systems

# A) Overall Satisfaction Score (OSAT = Average of all scores)


# Step 1: 
In this step, I performed the following :

- After fetching the JSON data, I iterated to make a CSV file of the required fields. I mainly fetched User comments, Cleanliness, Hotel Condition and Room Comfort data

# Step 2:

- **Using the saved CSV data set we will load Hotel Review scores and find Overall Satsifaction score as single point of reference for a particular hotel**

- The OVERALL SATISFACTION SCORE (OSAT) WAS MADE ON THE SCALE OF 5 and the EXPEDIA data showed the following results:

<img src="https://github.com/jaypadhya/spring2017_Python/blob/master/final/analysis/ana_-1-5/outputs/plots/plots/analysis2_OSAT_Score_number_reviews.png"></img>

# B) Combining TripAdvisor and Expedia Reviews 

Find **Hotel IDs** from **CSV** and collect reviews of hotels from **Expedia API key call** and **TripAdvisor web scraping.** (TripAdvisor does not provide API key for research hence I chose to scrape the data.)

- This provides us with dataframe have Expedia's hotel Reviews,Cleanliness Scores,RoomComfort Score and HotelCondition Score for top hotels on basis of number of User comments. Then we will **combine reviews** from **Expedia** and **TripAdvisor** on **top 10** hotels and perform **Sentimental Analysis** for customers saying on both websites.


**Steps:**
- Iterate over the CSV file which was made from JSON datasets and then use the reviews, Cleanliness score, Room comfort score and Hotel Condition Score.
- Combine it in a single dataframe and use it for Expedia Dataframe set

- Iterate over the Folders in TripAdvisor containing all web pages and iterate towards all tags to fetch the reviews from the TripAdvisor User

# NOTE: 
**Because the dataset goes beyond the capability of Git, we will perform iteration across top ten hotels from Expedia and find the same hotel name for Tripadvisor. Then merge both the comments in a single dataset. Once this is achieved, getting reviews from any number of hotels across both websites are possible. If git was not a challenge, I actually combined across all 50 hotels from Expedia and Tripadvisor**



--------------------------------------------------------------------------

** Now we merge both the dataframes and make a single dataset for Tripadvisor and Expedia**

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis2_comments_merged.PNG"></img>

# C) To Perform Sentimental Analysis for Top hotels across both the websites and find the sentiments for each of the reveiws

** STEPS **
- Using the above dataframes and passing the data to NLTK API for determining the scores and overall sentiments for top hotels.


**NOTE**:
- We would have to pass the data across each hotel from every row from Expedia and Tripadvisor as the comments are cumulative over a period of time. This means, the comments involve every single comment from Expedia and TripAdvisor from EVERY users to get a cumulative score for entire text 

**Thus we will get two dataframes from Expedia and Tripadvisor and we need to iterate over rows and SEND these to API call for NLTk. There is no KEY required as this is hitting the web URL and fetching the resposne**

**THE *ADVANTAGE* is it can run on any **HUGE TEXT** as it is in our case **

- Thus we will have two dataframes - One each for EXPEDIA AND TRIPADVISOR with their respective SENTIMENTAL SCORES and finalised labels

** The Image for the EXPEDIA sentimental Score looks like ** 

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis2_Exepdia_comments.PNG"></img>

** The Image for the TripAdvisor snetimental Score looks like ** 

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis2_TA_comments.PNG"></img>

# D) The Microsoft Cognitive API to fetch Sentimental Score and KeyWord extractions related to comments to understand the relationship  

** STEPS **
- We will use the EXPEDIA Datasets and perform Microsoft Cognitive services for keyword extraction and sentimental score. I have attached a sample code in my notebook and you can try any text, it works as it is open source as well
- After writing a function for fetching the data and getting over with it, we get the following output

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis2_microsoft_API_score.PNG"></img>

- I have attached a CSV file for the same("microsoft_combined_api.csv") which looks like :

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis2_microsoft_combined_score_important.PNG"></img>


---------------------------------------------------------------------------------------------------------------------------

# Analysis 3 : Recommendation Analysis

We will consider API Data and CSV Datasheet to evaluate the Overall Recommendation considering **both datasets**. Based on the **regions (Continent, country, city ), user preferences (family oriented, package deals, user source continent) from the CSV sheet and Sentimental scores (room cleanliness, Room Comfort,Hotel condition) from Expedia API data of Microsoft Cognitive APIs** - we will take user input and provide the best ten hotels in that regions.

**STEP 1**


- We combine the three CSV sheets - Sentimental score sheet, Word phrase sheet and the original CSV sheet to make a combined sheet for recommending a hotel to user based on all three factors.
- Loading all the three csv sheets and combine on hotelids
- Using many functions for getting user inputs based on his selection of city, country and recommending a centralised data for selection of the hotels. Such type of recommendations is called as collaborative filtering

- We combine both the Expedia User comments, Keywords extracted and sentimental score in single dataframe and looks like:

<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis3_microsoft_api_expedia_comments_combined.PNG"></img>

**STEP 2**
- Make a function for city, continent and country to allow a user to choose the destination based on his interests
- The first function for user city takes the city input from the user and then iterates through the dataframes to find which are best possible contries and continents where other users have been. The list for countries and continents is given to the user 
- The user will then select based on choices he gets from the system. 

**- The User gets the following screen to choose his city. The validation makes sure he inputs a number based in available dataset**
<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis3_selecting_city.PNG"></img>

**- The user gets the following screen as choices based on the CSV datasets and he can choose any option for based on options provided.**
<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis3_selecting_country_continent.PNG"></img>

** After iterating over the centralised Dataframe, the result is then provided with following information.**

** 1)Hotel Location, Hotel's Number of bookings (CSV Data)

**2) OSAT with Number of Expedia Reviews and User Comments(Expedia API Data), Cleanliness/Condition/Comfort Scores (Expedia API)  

**3) three most important Keywords and overall Sentimenal scores (Microsoft API)


<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis3_final_output.PNG"></img>

- I have created the CSV for the same choice and provided in the CSV files
<img src="https://github.com/jaypadhya/Expedia_Tripadvisor_Project/blob/master/final/analysis/ana_%5B1_3%5D/plots/analysis3_final_output_CSV.PNG"></img>

# This ensures that user has enough information before user books hotel 

Link for Dataset :https://drive.google.com/drive/u/1/folders/0B5LBxYvjN0ZwQW9Rb3BUSkItTjA

--------------------------------------------------------------------------------------------------------------------------------
