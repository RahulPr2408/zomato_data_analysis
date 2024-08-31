# Zomato Data Analysis

## Project Overview
This project involves analyzing a dataset from Zomato, a popular restaurant discovery platform. The dataset, `zomato_data.csv`, contains information about various restaurants, including their ratings, votes, approximate costs, and availability of online orders and table bookings. The goal of this project was to perform data cleaning, processing, and visualization to extract meaningful insights from the data.

## Dataset Description
The dataset used in this project consists of the following columns:

| Column                       | Description                                                | Data Type |
|------------------------------|------------------------------------------------------------|-----------|
| `name`                        | Name of the restaurant                                     | Object    |
| `online_order`                | Availability of online ordering (`Yes`/`No`)               | Object    |
| `book_table`                  | Availability of table booking (`Yes`/`No`)                 | Object    |
| `rate`                        | Rating of the restaurant in the format `x.x/5`             | Object    |
| `votes`                       | Number of votes the restaurant received                    | int64     |
| `approx_cost(for two people)` | Approximate cost for two people in the local currency      | int64     |
| `listed_in(type)`             | Type of restaurant (e.g., Buffet, Café, Dessert Parlor)    | Object    |

The dataset contains a total of 148 entries, each representing a restaurant with various attributes related to customer experience and cost.

## Libraries Used
The following Python libraries were utilized for data analysis and visualization:
- **Pandas**: For data manipulation and analysis
- **Matplotlib**: For creating static, interactive visualizations
- **Seaborn**: For creating visually appealing statistical plots

## Analysis Performed

### Data Cleaning
- **Removing Unnecessary Characters**: Removed the `/5` from the `rate` column to extract numerical ratings.
- **Handling Missing Data**: Although the dataset did not contain null values, the data was checked for any inconsistencies or anomalies.

### Data Processing
- **Data Transformation**: Converted the `rate` column from a string to a float to enable numerical operations.
- **New Features**: Created a new feature, `cost_per_vote`, to calculate the average cost per two people per vote for each restaurant.

### Data Manipulation
- **Group By Operations**: Aggregated data by `listed_in(type)` to find the average rating, votes, and cost for each type of restaurant.
- **Filtering**: Filtered the dataset to identify top-rated and high-cost restaurants, as well as those offering online orders and table bookings.

### Data Visualization
- **Distribution of Approximate Costs**: Visualized the distribution of approximate costs for two people using an enhanced count plot.
- **Votes by Restaurant Type**: Created a line plot to show the total number of votes received by each type of restaurant.
- **Ratings Distribution**: Visualized the distribution of ratings across all restaurants using a customized histogram.

## Key Insights
- **Majority of Restaurants**: Most restaurants in the dataset have a rating between 3.5 and 4.0.
- **Popular Restaurant Types**: The majority of customers prefer ordering from certain types of restaurants, which were identified through count plots.
- **Cost Analysis**: Higher-rated restaurants tend to have a higher approximate cost, and the cost per vote metric helped in understanding customer spending patterns.

## Conclusion
This project demonstrated the power of data cleaning, processing, and visualization in uncovering trends and patterns in restaurant data. By applying various Pandas operations and creating informative visualizations with Matplotlib and Seaborn, meaningful insights were derived that could be useful for business decisions in the food industry.

## Future Work
- **Sentiment Analysis**: Incorporate customer reviews to perform sentiment analysis and correlate with restaurant ratings.
- **Geospatial Analysis**: Include location data to analyze regional trends and preferences.

## Installation and Usage
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/RahulPr2408/zomato_data_analysis.git
   cd zomato-data-analysis
