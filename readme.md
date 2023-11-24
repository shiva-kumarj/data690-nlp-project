# Project
Problem statement: Analysis of sentiment disparity between various regions of the USA about Electric Vehicles.

## Project layout:
**dataset**: Contains the script(`news_extract.ipynb`) to read news articles from various sources and writes to them to the respective directories.
*news articles about states go into their respective directory.*

## Data dictionary:
- **title**: Title of the news article.
- **article**: article body.
- **date**: Date the article was published.
- **news_source**: name of the publishing agency.
- **state**: State the news publisher belongs to.

## How to get started:
simply run the `news_extract.ipynb` notebook. All the directories and the files will be written to the respective directories.


## DataFrame Structure

The primary dataset, represented by the DataFrame `df`, serves as the foundation for our project. Here's a quick overview of the key columns within the DataFrame:
DataFrame `df` combined the data from all the 3 regions.

1. **'title':**
   - Represents the title of the news article.

2. **'article':**
   - Contains the body or content of the news article.

3. **'news_source':**
   - Indicates the name of the publishing agency or news source.

4. **'region':**
   - Specifies the region to which the news article belongs ('east-coast', 'mid-west', 'west-coast').

5. **'article_cleaned':**
   - Contains the preprocessed and cleaned version of the article text.

6. **'converted_date':**
   - Represents the date of the article, potentially in a converted format.

7. **'year':**
   - Represents the year of the article.

8. **'entities':**
   - Contains information about entities extracted from the article. This could include named entities such as people, organizations, locations, etc.

## Output: Identified Topics in Different Regions (Topic Modelling)

The output of the topic modeling process includes a representation of topics identified in different regions. The structure of the output is as follows:

```python
{
    'east-coast': [
        (0, [('electric', 0.013918844), ('cars', 0.010919914), ...]),
        (1, [('energy', 0.019233901), ('heating', 0.014526396), ...]),
        ...
    ],
    'mid-west': [
        (0, [('electric', 0.018183071), ('vehicles', 0.014348478), ...]),
        (1, [('houston', 0.0070440886), ('energy', 0.0060703037), ...]),
        ...
    ],
    'west-coast': [
        (0, [('electric', 0.012310249), ('said', 0.0112518035), ...]),
        (1, [('california', 0.010265982), ('cars', 0.0069422796), ...]),
        ...
    ]
}


