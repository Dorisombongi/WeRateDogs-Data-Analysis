# WeRateDogs-Data-Analysis
## Gathering Data
Data was gathered using three different methods and stored separately;
1. twitter archive enhanced dataframe was manually downloaded from the link given in the Udacity classrom and uploaded into the jupyter notebook. The dataframe was loaded directly from the link into the jupyter notebook.
2. image predictions dataframe was downloaded programmatically using the request library.
3. tweet json dataframe was downloade by querying Twitter API using Tweepy library and data was extracted programmatically from the json text file.
## Assessing Data
The datasets were assessed both programmatically and visually using pandas in jupyter notebook and using excel. Eight quality issues and three tidiness issues were found.
## Cleaning Data
The timestamp column data in the twitter archive enhanced dataframe was converted to datetime datatype.

The source column in the twitter archive enhanced dataframe has additional values which were dropped, For example from a href="http://twitter.com/download/iphone" rel="nofollow">Twitter for iPhone</a to Twitter for iPhone

The name column in the twitter archive enhanced dataframe has names which are incorrect; names which are lowercase like 'such','a', 'quite','an' and 'the'. The names with lowercase were renamed to None

Tweet ids with replies twitter archive enhanced dataframe were deleted as per the project requirements and the in_reply_to_status_id and in_reply_to_user_id columns were dropped.

Tweets with retweets twitter archive enhanced dataframe were also deleted as per the project requirements and the retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp columns were dropped.

Tweets with missing data in the expanded_urls column in the twitter archive enhanced dataframe were dropped.

The rating_numerator column in the twitter archive enhanced dataframe has unexpected values; values greater than 15 are unexpected and i dropped tweets with values greater than 15.

Remaining tweets twitter archive enhanced dataframe with rating_denominator values that are greater than or less than 10 were dropped and the rating denominator column remained with 10 in all tweets.

The doggo, floofer, pupper and puppo columns in the twitter archive enhanced dataframe were melted into one column named dog_stage and the four columns were dropped. Tweets with two dog stages were edited manually and i kept each first dog stage listed in them to avoiding messing our data and manually changing the second dog stage in the tweets to None.
