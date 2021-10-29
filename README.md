# IRWA-2021-final-project-part-1

The workbook consists of the following:

1.- Imports cell -> All the libraries/modules used during the workbook are imported.  <br>

2.- A cell where we read the tweets dataset file using the json library and store its content in the "tweets" variable as a list of elements containing the information of each tweet.<br>

3.- A cell containing the functions that will be used during text processing, which are: <br>
&emsp;- remove_emoji(text):<br>
&emsp;  Given a string input the function removes any kind of emoji and returns the cleansed text.    

&emsp;- remove_symbols_and_links:<br>
&emsp;  Given a string input the function firstly removes from the text any link starting as https:// or http:// and then substitutes any character from the list ['&',':','.',',',';','…','-','!','?','¿'] for a blank space, because we don't want that to be processed as part of the keywords. Finally it returns the cleansed text.

&emsp;- build_terms:<br>
&emsp;  Given the content of a tweet as a text, this function firstly cleans the inputed text using the functions mentioned before, getting rid of emojis, links and symbols. Then it splits the cleansed text by every space character, obtaining that way a list of the words that appear in the tweet. Once we have that list, we remove from it all the stopwords that appear on the list given from the nltk library, such as articles, connectors... <br> After that, we stem each item of the wordlist, in order to obtain a keyword for each one. <br> Finally, we also separate from the list the hashtags contained in the tweet, creating a list specifically for them, which is appended at the end of the keyword list.<br>

4.- A cell where we execute the text processing over the tweets, by calling the build_terms function iteratively for every tweet, and save the results into a dictionary (tweets_keywords) containing the keywords of each one. <br>

5.- A last cell for printing some results as examples. <br>

For the code to work properly, the cells must be executed as they appear on the list above.
