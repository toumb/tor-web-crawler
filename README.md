# Tor Network Web Crawler
<br>
<b>NOTE: This application was developed and presented for my Master's degree thesis.</b>
<br>
The application initially creates a list of <b>Tor network</b> URLs, stores them in an <b>SQL</b> database, while
checking their status, whether they are active or not.
<br>
Then the web crawler retrieves the HTML content from these webpages and stores it in the database.

Three retrieval options are given to the user:


<b>1. Random crawl</b>
   The user gives an initial url (seed) and a number of pages.
   The crawler creates a list of all the links found in first page and then chooses
   randomly which page to crawl next. This continues until the number of pages
   is reached.
  

<b>2. Serial crawl</b>
   The user gives an initial url (seed) and next page format (eg. =page2).
   The crawler searches for next pages until no more pages are found.
   This function is ideal when crawiling eg. forums and only a specific post needs
   to be collected.

  
<b>3. Breadth-first crawl</b>
   The user gives an initial url (seed) and the desired level to be reached.
   For every page, the crawler gets all of the links found and stores their content in
   the database. Then repeats the same procedure for each one of them, thus implementing
   a breadth-first search.
   
While collecting the content, the text found in these pages is extracted and stored seperately.
Finally, an unsupervised machine learing algorithm is used in order to classify it, based on the cyber-threat type it refers to.

The machine learning algorithm used is <b>K-Means</b>.

The database is implemented with <b>SQLite</b>.
