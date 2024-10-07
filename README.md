# Data-512 Homework 1: Wikipedia Pageviews for Rare Disease Articles

## Project Overview
This project aims to collect, analyze, and visualize pageview data for a set of rare disease-related articles on English Wikipedia. The dataset spans from July 1, 2015, to September 30, 2024, and was obtained using the Wikimedia Analytics Pageviews API. The goal of the project is to understand the visibility of these articles over time by examining traffic trends and patterns.

## Data Description and Provenance

### Data Source
The dataset of rare diseases was provided by the professor in the CSV file `rare-disease_cleaned.AUG.2024.csv`. This list of pages was collected using a database of rare diseases maintained by the National Organization for Rare Diseases (NORD) ([NORD Database](https://rarediseases.org)), and matching them to Wikipedia articles either about rare diseases or containing sections related to rare diseases.

- **NORD Database**: [National Organization for Rare Diseases](https://rarediseases.org)
- **Wikimedia Pageviews API**: Data on article views for these diseases was collected using the [Wikimedia Analytics Pageviews API](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews).
- **Attribution**: The data is licensed under [CC-BY](https://foundation.wikimedia.org/wiki/Terms_of_Use) by the Wikimedia Foundation.
- **Time Range**: The pageview data spans from July 1, 2015, through September 30, 2024.

### API Usage
The pageview data was collected using the Wikimedia Pageviews API for different access types (desktop, mobile-web, and mobile-app). Monthly pageviews were recorded for each article in the list, and the data was aggregated across mobile and desktop views for cumulative results.

The API endpoint used for data collection was:

```python
API_ENDPOINT = 'https://wikimedia.org/api/rest_v1/metrics/pageviews/per-article/{project}/{access}/{agent}/{article}/{granularity}/{start}/{end}'
```

## Files in the Repository

- [Code Notebook](analysis.ipynb): Jupyter Notebook containing the code for data collection, analysis, and visualization.
- [rare-disease_cleaned.AUG.2024.csv](rare-disease_cleaned.AUG.2024.csv): The cleaned dataset of rare disease articles provided by the professor.
- [data/rare-disease_monthly_mobile_201507-202409.json](data/rare-disease_monthly_mobile_201507-202409.json): JSON file with monthly mobile pageviews (combined mobile-app and mobile-web) for rare disease articles.
- [data/rare-disease_monthly_desktop_201507-202409.json](data/rare-disease_monthly_desktop_201507-202409.json): JSON file with monthly desktop pageviews for rare disease articles.
- [data/rare-disease_monthly_cumulative_201507-202409.json](data/rare-disease_monthly_cumulative_201507-202409.json): JSON file with cumulative monthly pageviews (desktop + mobile) for rare disease articles.
- [max_min_avg_pageviews.png](max_min_avg_pageviews.png): Graph showing the maximum and minimum average pageviews for both mobile and desktop access.
- [top_10_peak_pageviews.png](top_10_peak_pageviews.png): Graph showing the top 10 articles by peak pageviews for both desktop and mobile access.
- [fewest_months_pageviews.png](fewest_months_pageviews.png): Graph showing the articles with the fewest months of available data for both desktop and mobile access.
- [README.md](README.md): This file, providing an overview of the project and its contents.
- [LICENSE](LICENSE): MIT License for the project code.


## Libraries Used
The following Python libraries were used for this project:

- `json`: For handling and saving data in JSON format.
- `urllib.parse.quote`: For encoding article titles in URLs.
- `pandas`: For processing and analyzing the data.
- `tqdm`: To display progress bars when iterating through API requests.
- `os`: For handling file operations.
- `matplotlib.pyplot`: For generating visualizations.
- `time`: To control API request timing to avoid exceeding the rate limit.
- `requests`: To make API calls to the Wikimedia Pageviews API.

## How to Reproduce the Analysis

To reproduce the analysis, follow these steps:
1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-directory>
```

2. Install the required Python packages:
Install using pip:
```bash
pip install json urllib tqdm pandas matplotlib requests
```

3. Data Collection: 
The data is collected using the Wikimedia Analytics Pageviews API. You can run the provided code in `analysis.ipynb` to fetch data for each article and save it into JSON files.

4. Run the Jupyter Notebook:
Open and run `analysis.ipynb`  in a Jupyter environment to execute the analysis and generate the visualizations.

## Analysis and Visualizations
The analysis includes the following visualizations:

1. Maximum and Minimum Average Pageviews: Displays the articles with the highest and lowest average pageviews over the time period.
2. Top 10 Peak Pageviews: Shows the top 10 articles with the highest peak pageviews for both mobile and desktop access.
3. Fewest Months of Data: Highlights the articles with the fewest months of available pageview data for both mobile and desktop access.

## License Information

The code for this project is licensed under the MIT License (see the LICENSE file). The data obtained from the Wikimedia Pageviews API is licensed under CC-BY as per Wikimedia Foundation's Terms of Use.

