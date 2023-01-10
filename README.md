# Weratedog-Twitter-Archive-Analysis-Project

WeRateDogs is an online Twitter account which is devoted to humorously reviewing pictures of dogs doing adorable poses, often giving them scores above 10/10. It has acquired more than 7 million followers since its debut. 
The main goal of the analysis is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations.

## Data Wrangling Process
The data was collected from three different sources as stated below; 
❖	Enhanced Twitter Archive contains WeRateDogs basic tweet data for all 5000+ of their tweets, but not everything. The data is stored in a CSV file, which contains information such as each tweet text, dog rating, dog stage, dog name etc. 
 
❖	Image Predictions File contains information about every image in the 
WeRateDogs Twitter archive through a neural network that can classify breeds of dogs which results in a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images). 
 
 
❖	Additional Data via the Twitter API such as retweet count, and favorite count for individual tweets present in the enhanced Twitter archive are gathered through the Twitter API using the tweet id

The data collection process and sources were different for all the data used for the analysis; 
The dataset was collected, loaded and cleaned in python with the use of some libraries such as pandas, NumPy, tweepy, requests, JSON and regular expression. 
The enhanced Twitter was stored in CSV file which was load in into a python data frame using the pandas’ libraries with a total of 2356 observations and 17 features such as tweet id, tweet text, ratings etc.

The image file was downloaded programmatically from the Udacity server using the provided URL with the request library which was later written into a TSV(tab-seperated-values) file known as image prediction and loaded into a python data frame object using the panda’s library. The dataset contains 2074 rows of predicted dogs’ images. 
Additional data was mined from Twitter API using the tokens and keys from the Twitter developer account as the authentications. Each tweet information was extracted using the tweet id which was later stored in a text file. The text file was read into a python object using the panda’s package. Data Cleaning Process  
some data qualities and tidiness issues were discovered from the data and these are; 

Quality issue twitter_arch Table 
*	presence of null values in most of the columns 
*	outliers in the rating numerator column 
*	outliers in the rating denominator column 
*	URL embedded in the text 
*	timestamp column is object data type, not DateTime 
*	inconsistent dog name
Image table 
*	inappropriate feature naming 
*	presence of non-dog observations 

Tidiness issues 
*	image prediction variable spread over multiple columns 
*	Dog variable spread over multiple tables 
*	Dog stages spread over multiple columns 
These qualities and tidiness issues were cleaned and rectified using the panda’s library

## Data Analysis

The analysis set to answer the following questions; 
*	What dog breed has the highest number of ratings? 
*	What dog breed is the most rated? 
*	Is there relationship between retweet count, favorites count(likes0 and dog ratings? 
The data was collected from three different sources such as the Enhanced Twitter Archive, Image Predictions File, Additional Data via the Twitter API which was collected, cleaned and stored into a single table known as master_twitter archive, which later was use for further analysis. 

Question 1: what dog breed has the highest number of ratings? 
The most rated dog breed was determined by getting the count of individual dog breed that was rated by users  
 
   
It can be seen from the above graph that golden-retriever is the most rated dogs among the users follow by Pembroke and Labrador-retriever 

 

