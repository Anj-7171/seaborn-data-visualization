# Seaborn Visualization Guide

This guide explains the different visualization techniques demonstrated in this project using the **Seaborn** library. Each section introduces the plot type, describes the example used from the Tips dataset, and provides a brief analysis of the resulting visualization.

---

# 1. Scatter Plot

## What is a Scatter Plot?

A scatter plot is used to visualize the relationship between two numerical variables. Each point represents a single observation in the dataset, making it useful for identifying trends, clusters, correlations, and potential outliers. It is one of the most commonly used plots in Exploratory Data Analysis (EDA).

### What is Plotted?

The scatter plot compares **Total Bill** (x-axis) with **Tip Amount** (y-axis) using the Tips dataset.

### Analysis

The visualization shows a clear positive relationship between the total bill and the tip amount. Customers with higher bills generally tend to leave larger tips. Although the trend is not perfectly linear, the upward distribution of points indicates a moderate positive correlation between the two variables.

<img width="382" height="263" alt="scatterplot" src="https://github.com/user-attachments/assets/f0b6e8e5-c9ba-4f7c-bd92-f002d1820e6f" />



---

# 2. Relational Plot (Colored by Day)

## What is a Relational Plot?

A relational plot extends a scatter plot by allowing additional variables to be represented using visual attributes such as color (`hue`), size, or style. This enables comparison between different categories while still preserving the relationship between two numerical variables.

### What is Plotted?

The relationship between **Total Bill** and **Tip Amount** is displayed, with points colored according to the **Day of the Week**.

### Analysis

The plot reveals that the positive relationship between total bill and tip remains consistent across all days. Coloring the points by day helps distinguish customer behavior throughout the week and allows us to identify whether certain days tend to have higher bills or tips than others.

<img width="410" height="353" alt="Relational plot by day" src="https://github.com/user-attachments/assets/b9240155-14fe-443e-84f3-88790e365c2e" />


---

# 3. Relational Plot (Colored by Time)

## What is a Relational Plot?

Relational plots are useful for comparing relationships across different categories without creating separate graphs. Using the `hue` parameter improves readability by grouping observations visually.

### What is Plotted?

The plot compares **Total Bill** and **Tip Amount**, while distinguishing observations based on whether the meal occurred during **Lunch** or **Dinner**.

### Analysis

Dinner transactions generally occupy the higher bill and higher tip ranges, while lunch transactions appear more concentrated at lower bill values. This suggests that dinner meals often involve larger bills and correspondingly larger tips.

<img width="419" height="353" alt="Relational plot by time" src="https://github.com/user-attachments/assets/37145f23-ffa4-4834-b5ad-b861845ad734" />


---

# 4. Faceted Relational Plot

## What is a Faceted Plot?

Faceting divides a visualization into multiple smaller plots based on a categorical variable. Instead of combining all observations into one figure, each category is shown separately, making comparisons much easier.

### What is Plotted?

Separate scatter plots are created for **Male** and **Female** customers, while colors continue to represent **Lunch** and **Dinner**.

### Analysis

Displaying separate plots makes it easier to compare customer groups independently. Both genders exhibit a similar positive relationship between bill amount and tip. The visualization also highlights that dinner transactions dominate in both groups.

<img width="783" height="353" alt="Faceted Relational Plots" src="https://github.com/user-attachments/assets/57ddf0c1-44d8-4c94-bdc2-f021d3708fd0" />


---

# 5. Bar Plot

## What is a Bar Plot?

A bar plot summarizes numerical data across different categories by displaying the average value of each category. Seaborn automatically computes the mean and includes confidence intervals, making it useful for comparing category-wise statistics.

### What is Plotted?

The average **Total Bill** is compared between **Male** and **Female** customers.

### Analysis

The plot indicates that male customers have a slightly higher average total bill than female customers. The confidence intervals also provide insight into the variability of the average values across the two groups.

<img width="383" height="262" alt="bar plot" src="https://github.com/user-attachments/assets/f6f2d177-8fa2-49b3-8a0c-d916d5c12ad4" />


---

# 6. Count Plot

## What is a Count Plot?

A count plot displays the frequency of observations in each category. Unlike a bar plot, it counts occurrences instead of calculating averages, making it useful for understanding the distribution of categorical variables.

### What is Plotted?

The number of restaurant visits is shown for each **Day of the Week**.

### Analysis

The visualization reveals that customer visits are not evenly distributed throughout the week. Some days have noticeably more observations than others, indicating busier periods for the restaurant.

<img width="382" height="262" alt="Count plot" src="https://github.com/user-attachments/assets/5987d2a1-7623-45a0-8f7b-8b790fab5b64" />


---

# 7. Box Plot

## What is a Box Plot?

A box plot summarizes the distribution of numerical data using the median, quartiles, whiskers, and outliers. It provides an effective way to compare distributions across multiple categories while highlighting variability and unusual observations.

### What is Plotted?

The distribution of **Total Bill** is compared across different **Days**, with separate boxes representing **Smokers** and **Non-Smokers**.

### Analysis

The plot allows easy comparison of spending behavior across days and smoking status. It highlights differences in median bill amounts, spread of the data, and the presence of outliers. Certain categories show greater variability, suggesting that spending patterns differ between groups.

<img width="383" height="262" alt="box plot" src="https://github.com/user-attachments/assets/1d14f139-c21b-49ad-8004-4ce56e3d9087" />


---

# 8. Distribution Plot

## What is a Distribution Plot?

A distribution plot combines a histogram with a Kernel Density Estimation (KDE) curve to visualize the overall distribution of a numerical variable. It helps determine whether the data is normally distributed, skewed, or contains multiple peaks.

### What is Plotted?

The distribution of **Total Bill** values is displayed.

### Analysis

The histogram shows that most restaurant bills fall within a moderate price range, while fewer observations occur at very high bill amounts. The KDE curve provides a smooth estimate of the distribution, indicating that the data is positively skewed with a longer tail toward larger bills.

<img width="392" height="263" alt="distribution plot" src="https://github.com/user-attachments/assets/27280b32-b94c-42df-820c-283bdef80960" />


---

# 9. Joint Plot

## What is a Joint Plot?

A joint plot combines a scatter plot with the individual distributions of each variable along the margins. It provides both the relationship between two variables and the distribution of each variable in a single visualization.

### What is Plotted?

The relationship between **Total Bill** and **Tip Amount**, along with their individual distributions.

### Analysis

The scatter plot confirms the positive association between total bill and tip amount. The marginal histograms show that both variables are concentrated around lower values, with fewer observations at higher amounts.

<img width="421" height="424" alt="joinplot" src="https://github.com/user-attachments/assets/4c51aa96-0d81-4279-9533-4cc9a8582497" />


---

# 10. Pair Plot

## What is a Pair Plot?

A pair plot automatically generates scatter plots for every combination of numerical features and histograms along the diagonal. It is widely used during exploratory data analysis to quickly identify relationships, correlations, clusters, and feature distributions.

### What is Plotted?

Pairwise relationships between **Total Bill**, **Tip Amount**, and **Party Size** are displayed, with observations colored by **Gender**.

### Analysis

The pair plot highlights positive relationships between several numerical variables, particularly between total bill and tip amount. Coloring the observations by gender shows that both groups exhibit similar overall patterns, indicating no major differences in the relationships between these variables.

<img width="610" height="533" alt="pair plot" src="https://github.com/user-attachments/assets/08d854fb-b104-4e74-8d1c-adecf337db51" />


---

# 11. Correlation Heatmap

## What is a Heatmap?

A heatmap represents numerical values using color intensity. When applied to a correlation matrix, it provides a quick visual summary of the strength and direction of relationships between numerical variables.

### What is Plotted?

The correlation matrix of the numerical features in the Tips dataset.

### Analysis

The heatmap shows which variables are positively or negatively correlated. Darker shades indicate stronger relationships, while lighter colors represent weaker correlations. It provides a quick overview of feature interactions before building predictive models or performing deeper analysis.


<img width="350" height="253" alt="heatmaps" src="https://github.com/user-attachments/assets/c2a54e8b-ec49-40b4-a314-b3cab1ccb558" />


---

# 12. Annotated Heatmap

## What is an Annotated Heatmap?

An annotated heatmap extends a standard heatmap by displaying the exact numerical values inside each cell. This makes interpretation easier by combining both visual color cues and precise correlation coefficients.

### What is Plotted?

The same correlation matrix is displayed with correlation values annotated inside each cell and a customized color map.

### Analysis

The annotations make it easy to quantify the strength of each relationship instead of relying solely on color intensity. Variables with coefficients closer to **1** exhibit stronger positive relationships, while lower values indicate weaker associations. This visualization provides a more detailed understanding of feature correlations.

<img width="350" height="253" alt="annotated heatmaps" src="https://github.com/user-attachments/assets/45d729fd-219f-4ffe-8ac0-d971787f5687" />
