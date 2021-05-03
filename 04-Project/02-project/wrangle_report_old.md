This project was an enjoyable exploration into the task of wrangling data. Overall, the project was not difficult, although it was time consuming.

I began the project by importing all the data. The main data and the predictions data I simply imported, using pandas `read_csv()` function. 

I am not fan of social media and generally avoid using social media accounts, due to privacy concerns. I do not have a personal Twitter account. For this reason, I chose not to create a Twitter API account to download all the data for the given Tweet ID's in the table. I do understand the general concept of how this API would function, and if I choose to do this in the future, I have saved a copy of the suggested python code.

After importing the data, I assessed it. The most prominent data and quality issues I found are as follows:

### Quality

- Rating denom is 0 for row 313. Should be 13/10.
- Dog name 'such', 'a', 'quite','not', 'mad' found. The 'This is ...' str extractor didn't work properly
- Name column value is not accurate when the name value comes after lower case `this is [name]` in text
- RIP name not included
- Names followed by `name is ...` are not included
- Some tweets are RT's, as evidenced by first part of tweet
- When two dogs, Bentley/Millie, only first shows up
- Dropping unneeded columns
- Drop rows where df_tweets or df_predictions have no data for a tweet_id
- tweet_id is integer, should be string, in_reply_to... and retweeted_... are in float, should be string
- timestamp should be datetime, instead of object, timestamp column contains +0000 which looks redundant.
- In some of the columns there is None instead of NaN
- Some image predictions do not indicate dogs
- Get rid of extra content in source column
- Some `favorite_count` values are `0`, which seems unlikely.
- Drop any remaining rows that are retweets.
- Some `retweeted_status_id` values are actually garbled strings from the `text column`.
- Missing numerators
- Denominator in names
- Rows where `retweeted_status_timestamp` has values should all be removed as they are retweets

### Tidyness

- Columns have puppo, floofer, etc, and then None, and then the variable name
- Organize main dataframe, combine all into one

Some of these issues I found immediately, others I found during the course of the Cleaning stage.

I dropped all rows for which all three original datasets did not have at least some values. This resulted in a greatly reduced dataset, with only `1994` values, as opposed to the original `5000`.

If I had time to clean this dataset to perfection, there are many additional tasks I would complete. For example, I noticed towards the end of the project that some of the `text` column had been split into the `retweeted_status_id` column, and in these rows, the `rating_numerator` was empty and the appropriate value thereof was misplaced into the `rating_denominator` column, while the latter's value was misplaced into the `name` column. 