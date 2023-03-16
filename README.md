# Wrangling and Analyzing WeRateDogs Data
## by Harnex Kakandelwa


## Dataset
This project involves gathering, assessing, cleaning and analyzing data about dog ratings from the popular Twitter account, [WeRateDogs](https://en.wikipedia.org/wiki/WeRateDogs). The original data used is from three separate datasets. The first dataset has archived tweets (with information such as the source, dog name, rating, and dog stage), the second dataset has predictions of dog breed based on the images while the third has information about the number of likes and retweets.

After assessing and cleaning the data, the analysis explores questions such as which dog stage or breed is popular in the WeRateDogs data?; what is the most common source of dog rating tweets?; which year had the highest number of dog rating retweets?; and so on.

Some of the changes made to the data or issues resolved in the cleaning process included the following:
* In the twitter archive dataframe, each dog stage was presented in a separate column, giving a total of four columns with information about one variable, dog stage. To make the data tidy, the four columns were collapse into one column for the dog stage variable
* The tweet counts and twitter archive dataframes were merged so that the `retweet_count` and `favorite_count` columns were part of the twitter archive dataframe
* Rows with retweets and replies were dropped since only original tweets were needed for the analysis
* The data type of the timestamp column was changed from string to datetime
* The rating denominator and numerator were extracted from the text in the `text` column
* Some of the predictions in the image predictions dataframe were not for dogs. So such rows were dropped from the dataframe

Details of the wrangling efforts for this project can be found in the **wrangle_report** file contained in the project repository.


## Summary of Findings
Using the assessed and cleaned WeRateDogs data, the following are some of the findings from the investigation:

1. What are the top five popular dog breeds based on the average favorite count?

  * Based on the average favorite count, the most popular breed is the black-and-tan_coonhound with an average of 33911 likes followed by the Bedlington_terrier with a mean of 33445 likes. The other three breeds making up the top five include Saluki (24060), French_bulldog (23118) and Afghan_hound (22451).



2. What is the most common source of dog rating?

  * The most common source of dog rating tweets is "Twitter for iPhone", with 1354 tweets followed by "Twitter Web Client" with 14 tweets.


3. On average, how has the number of dog rating retweets changed from 2015 to 2017?

  * Between 2015 and 2017, the number of dog rating retweets increased by over 300%, from about 1379 retweets in 2015 to about 6031 retweets in 2017.



4. Which dog stage has the highest median rating?

  * The popular dog stages based on the median rating are doggo and puppo with median ratings of 13 and 12 between them.


For a detailed report on the findings, please see the **findings_report** in the project repository.