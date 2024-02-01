# web-scraping-challenge

This new assignment consists of two technical products:
- Deliverable 1: Scrape titles and preview text from Mars news articles.
- Deliverable 2: Scrape and analyze Mars weather data.

### Deliverable 1: Scrape Titles and Preview Text from Mars News
1. I used Splinter to visit https://static.bc-edx.com/data/web/mars_news/index.html.
  
2. I created a Beautiful Soup object and used it to extract the text elements from the website.
  
3. I stored the article titles and preview texts of the news articles in a title-and-preview pair in a Python list of dictionaries, giving each dictionary two keys: `title` and `preview`.


  
### Deliverable 2: Scrape and Analyze Mars Weather Data**
1. I used Splinter to visit https://static.bc-edx.com/data/web/mars_facts/temperature.html.
2. I created a Beautiful Soup object and used it to extract the data in the HTML table.
3. I assembled the  data into a Pandas DataFrame, with the columns having the same headings as the table on the website.
  - These are the column headings:
    - `id`: the identification number of a single transmission from the Curiosity rover
    - `terrestrial_date`: the date on Earth
    - `sol`: the number of elapsed sols (Martian days) since Curiosity landed on Mars
    - `ls`: the solar longitude
    - `month`: the Martian month
    - `min_temp`: the minimum temperature, in Celsius, of a single Martian day (sol)
    - `pressure`: The atmospheric pressure at Curiosity's location
      
4. Next, I examined the data types that are currently associated with each column and casted `id`, `sol`, `ls`, and `month` to integer, `terrestial_date` to datetime, and `min_temp` and `pressure` columns to float.
5. Analyzed the dataset by using Pandas functions to answer the following questions:
   - How many months exist on Mars?
     - **A: 12 months**
   - How many Martian (and not Earth) days worth of data exist in the scraped dataset?
     - **A: 12 months**
   - What are the coldest and the warmest months on Mars (at the location of Curiosity)?
     - To answer this question:
       - Find the average the minimum daily temperature for all of the months.
       - Plot the results as a bar chart.
     - **A: On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest.**
   - Which months have the lowest and the highest atmospheric pressure on Mars?
     - To answer this question:
       - Find the average the daily atmospheric pressure of all the months.
       - Plot the results as a bar chart.
     - **A: Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.**
   - About how many terrestrial (Earth) days exist in a Martian year?
     - **A: The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.**
  


