# Segmenting and Clustering Neighborhoods in Toronto

## Purpose
Explore, segment, and cluster the neighborhoods in the city of Toronto based on the postal code and borough information

## Data Collection
Toronto neighborhood data is not readily available on the internet as a dataset, thus **web scraping** would have to be implemented in order to assimilate the dataframes required for the analysis. For this purpose a Wikipedia page has been identified as the source that has all the information we need to explore and cluster the neighborhoods in Toronto.

## Data Cleaning
Upon wrangling the data, the following data cleaning procedures are to be performed on it before assembling it into a pandas dataframe that it is in a structured format, facilitating the analysis process:
- The dataframe will consist of three columns: PostalCode, Borough, and Neighborhood
- Only the cells that have an assigned borough are processed. Cells with a borough that is 'Not assigned' are ignored.
- More than one neighborhood can exist in one postal code area. For example, in the table on the Wikipedia page, you will notice that M5A is listed twice and has two neighborhoods: Harbourfront and Regent Park. These two rows will be combined into one row with the neighborhoods separated with a comma.
- If a cell has a borough but a 'Not assigned' neighborhood, then the neighborhood will be the same as the borough.
- In order to utilize the Foursquare location data, latitude and the longitude coordinates of each neighborhood are needed, for which the [Geocoder Python package](https://geocoder.readthedocs.io/index.html) would be used

## Data Analysis
Once the data is in a structured format, it is used to explore and cluster the neighborhoods in the city of Toronto. Maps are created to visualize your neighborhoods and how they cluster together. 
