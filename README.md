# Coffee Contains More Caffeine Than an Energy Drink

## Introduction

Caffeine is one of the world’s most popular stimulants, found in beverages such as coffee and energy drinks. There’s a common belief that energy drinks are more potent, but is that really the case? This project analyzes and compares the caffeine content in coffee and energy drinks using real-world data.

## Methodology

### Data Collection
- **Source:** Caffeine content data was scraped from [Caffeine Informer](https://www.caffeineinformer.com/the-caffeine-database), a comprehensive resource for beverage caffeine information.
- **Tools:** BeautifulSoup (for web scraping), Pandas (for data handling), Jupyter Notebook (for analysis and visualization).

### Data Processing
- Extracted beverage names, volumes (fl oz), calories, caffeine (mg), caffeine per fl oz, and drink type.
- Cleaned and normalized the data, categorizing drinks as `Coffee`, `Energy Drink`, `Tea`, `Soda`, `Water`, or `Energy Shot`.
- Converted all relevant fields to numeric types for analysis.

### Exploratory Analysis
- Calculated descriptive statistics for each drink type:
  - Mean, median, and maximum caffeine content per serving.
  - Distribution of caffeine per fluid ounce.
- Visualized data to showcase caffeine ranges and outliers using Matplotlib and Seaborn.

### Statistical Testing
To objectively compare caffeine content between coffee and energy drinks:
- **Test Used:** Independent two-sample t-test.
- **Purpose:** To determine if the difference in mean caffeine content per serving between coffee and energy drinks is statistically significant.
- **Procedure:**
  - Isolated caffeine values for each category.
  - Checked for normality and equal variance.
  - Ran the t-test, reporting p-value and confidence interval.

### Steps Performed
1. Scraped raw caffeine data for hundreds of beverages.
2. Loaded the dataset into a Pandas DataFrame.
3. Cleaned, normalized, and categorized drinks.
4. Generated summary statistics and visualizations.
5. Conducted a t-test to compare coffee and energy drink caffeine content.
6. Interpreted findings and visualized the results.

## Results & Insights

The analysis revealed several interesting findings:
- **Coffee:** Servings vary widely, but many popular coffees (especially brewed and specialty varieties) contain exceptionally high caffeine levels—often surpassing energy drinks.
- **Energy Drinks:** Most mainstream brands (Red Bull, Monster, Rockstar) cluster around 80–160 mg per serving, with some outliers reaching higher.
- **Statistical Test:** The t-test confirmed that the average caffeine content per serving in coffee is **significantly higher** than in energy drinks (p < 0.05).
- **Surprising Finds:** Some specialty coffees (e.g., Death Wish, Black Label) contain up to 1500 mg per serving—far beyond any energy drink.

## Conclusion

Despite marketing hype, **coffee contains more caffeine per serving on average than energy drinks**. While some energy drinks can match or exceed the lower end of coffee’s range, the strongest coffees far surpass the strongest energy drinks.

## How to Reproduce

1. Clone the repository.
2. Open the Jupyter Notebook (`caffeine data scrapping.ipynb`).
3. Run the notebook to view data scraping, cleaning, statistical testing, and visualizations.
4. Modify or extend the analysis with your own data or hypotheses.

## Repository Structure

- `caffeine data scrapping.ipynb`: Main analysis notebook, including data scraping, processing, and statistical testing.
- `drinks_data.csv`: Cleaned dataset (generated during analysis).
- `README.md`: Project overview and findings.

## References

- [Caffeine Informer - The Caffeine Database](https://www.caffeineinformer.com/the-caffeine-database)
- [Pandas Documentation](https://pandas.pydata.org/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Scipy Stats](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html)

---

**TL;DR:** By the data, by the stats, and by the story, coffee’s caffeine punch beats energy drinks!

---