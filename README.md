# Race Bar Chart Visualization for Canada's Population (1980-2001)

This project creates a race bar chart visualization of the population of Canada over the years. The animation dynamically displays the population distribution across different age groups and sexes over time.

## Table of Contents

- [Languages and Libraries Used](#languages-and-libraries-used)
- [Concepts Used](#concepts-used)
- [Data Preparation](#data-preparation)
- [Race Bar Chart Implementation](#race-bar-chart-implementation)
- [Experience and Challenges](#experience-and-challenges)
- [How I Overcame the Challenges](#how-i-overcame-the-challenges)
- [How to Run the Code](#how-to-run-the-code)
- [Acknowledgments](#acknowledgments)

## Languages and Libraries Used

### Languages:
- **Python**

### Libraries:
- **Pandas**: For data manipulation and preprocessing.
- **Matplotlib**: For data visualization.
- **FuncAnimation**: To animate the race bar chart.
- **PillowWriter**: To save the animated chart as a GIF or video.

## Concepts Used

1. **DataFrame Manipulation**: 
   - Loading and transforming the data using Pandas for easier manipulation during the animation.
   
2. **Bar Chart Creation**:
   - Visualizing population data by sex and age group using horizontal bar charts.

3. **Animation with FuncAnimation**:
   - Animating the population change over time using FuncAnimation from Matplotlib.

4. **File Writing (GIF or Video)**:
   - Saving the animated chart to a file format (GIF) using `PillowWriter`.

5. **Customization**:
   - Adding colors, legends, labels, and title formatting to enhance the readability and presentation of the chart.

## Data Preparation

1. The **Canada Population dataset** is read using Pandas.
2. The dataset includes age groups, sex (male and female), and population values for each group.
3. The data is transformed to fit the structure required for the race bar chart.

```python
import pandas as pd
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter

# Load dataset
df = pd.read_csv('Canada_pop.csv')
```
##Race bar chart Implementation:
#Steps
