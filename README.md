# Data-512 Homework 1: Wikipedia Pageviews for Rare Disease Articles

## Project Overview
The goal of this project is to collect, analyze, and visualize pageview data for a set of rare disease-related articles on English Wikipedia from July 1, 2015, through September 30, 2024. The analysis is part of Homework #1 for DATA 512 and focuses on understanding article traffic trends and ensuring best practices for open scientific research.

## Data Source
Data for this project is collected from the Wikimedia Analytics Pageviews API:
- API Documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
- Wikimedia Foundation Terms of Use: https://foundation.wikimedia.org/wiki/Terms_of_Use

## Files in the Repository
- `assessment.ipynb`: Jupyter Notebook that contains the code for data collection, analysis, and visualization.
- `rare-disease_monthly_mobile_201507-202409.json`: JSON file with monthly mobile pageviews for rare disease articles.
- `rare-disease_monthly_desktop_201507-202409.json`: JSON file with monthly desktop pageviews for rare disease articles.
- `rare-disease_monthly_cumulative_201507-202409.json`: JSON file with monthly cumulative pageviews (desktop + mobile) for rare disease articles.
- `max_min_avg_pageviews.png`: Image file containing a graph showing the maximum and minimum average pageviews for both mobile and desktop access.
- `top_10_peak_pageviews.png`: Image file showing the top 10 articles by peak pageviews for both desktop and mobile access.
- `fewest_months_pageviews.png`: Image file showing the articles with the fewest months of available data for both desktop and mobile access.
- `README.md`: This file, providing an overview of the project and its contents.
- `LICENSE`: MIT License for the project's code.

## Analysis
Three different analyses were conducted to visualize traffic trends:
1. **Maximum and Minimum Average Page Requests**: Shows the articles with the highest and lowest average pageviews over the entire time series for both mobile and desktop.
2. **Top 10 Peak Page Views**: Displays the top 10 articles with the highest peak pageviews in any single month, separately for mobile and desktop access.
3. **Fewest Months of Data**: Highlights the 10 articles with the fewest months of available data, separately for mobile and desktop.

All graphs are labeled with appropriate titles, axes, and legends for clarity.

## How to Reproduce the Analysis
1. Clone the repository or download the notebook and JSON data files.
2. Install the required Python packages by running:
   ```bash
   pip install json urllib tqdm pandas matplotlib requests
  
