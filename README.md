# Race Bar Chart Visualization for Canada's Population (1971-2021)

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
## Racebar Chart Implementation:

## Step1: Set Up the Bar Chart: Initialize a horizontal bar chart using matplotlib.

```python
fig, ax = plt.subplots()
```

## Step2: Define the Animation Function: Create a function to update the chart dynamically as the race progresses.

```python
def update(frame):
    # Code to update the chart bars based on population per age group
    ax.clear()
    ax.barh(ages, population_data)
```

## Step3: Implement FuncAnimation:

This function animates the bar chart for each frame, updating the values of the bars to reflect population changes.

```python
anim = FuncAnimation(fig, update, frames=len(df), repeat=False)
```

## Step4: Saving the Animation: Save the final animation using PillowWriter:

```python
writer = PillowWriter(fps=10)
anim.save("population_race_chart.gif", writer=writer)
```

## Experience and Challenges

### Experience:
I have experience in Python and its associated libraries like Pandas and Matplotlib. However, working with **FuncAnimation** and **PillowWriter** to create a dynamic, animated race bar chart was a new challenge. Managing data transformations and ensuring the race bar chart was visually appealing required a good grasp of Pandas data manipulation techniques and matplotlib visual customization options.

### Challenges Faced:

#### Data Transformation:

- **Challenge**: Ensuring the data was in the correct format for animation, especially in terms of structure, sorting, and updating the population values across frames.

#### Maintaining Bar Labels Consistency:

- **Challenge**: The bar labels (age groups) sometimes overlapped or misaligned during animation.
- **Overcome**: I used Matplotlib's formatting capabilities to handle dynamic resizing and ensure labels aligned with their corresponding bars.

#### Animation Performance:

- **Challenge**: Rendering the race bar chart animation was initially slow due to the number of frames.
- **Overcome**: I optimized the animation by limiting the number of frames rendered per second (FPS) and caching some intermediate results to avoid redundant recalculations.

### Label Consistency:
I adjusted the font size and spacing using `ax.text()` and `ax.set_xlabel()` in each animation frame to ensure readability without overcrowding the visualization.

### Animation Optimization:
By setting the animation FPS to a lower rate (10 frames per second) and fine-tuning the range of values displayed per frame, I significantly improved the overall performance of the animation.

### Final Visualization:

![Racebar Chart](https://github.com/shanthan98/Racebarchart_Population/blob/main/assets/images/canadapop_racebarchart.gif)







