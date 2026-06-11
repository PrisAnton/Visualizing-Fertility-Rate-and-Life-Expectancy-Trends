# Global Fertility Rate and Life Expectancy Dashboard

This project is an interactive data visualization dashboard that explores how fertility rates and life expectancy changed across the world from 1964 to 2013.

The dashboard is built with Python and Bokeh using Gapminder demographic data. It allows users to explore global patterns, regional differences, and country-level development trajectories through animation, filters, hover tooltips, and linked charts.

## Project Overview

The main research question behind this project is:

> How have global fertility rates and life expectancy evolved from 1964 to 2013, and how can interactive visualization reveal patterns, correlations, and regional disparities in this relationship?

The project focuses on two main ideas:

1. How countries moved from high fertility and low life expectancy toward lower fertility and higher life expectancy over time.
2. How interactive tools can make regional and country-level differences easier to observe than static charts.

## Features

* Animated scatter plot of fertility rate and life expectancy by year
* Year slider for manually exploring changes from 1964 to 2013
* Autoplay button for watching the global demographic transition over time
* Region filter for comparing geographic groups
* Country search and click-to-select interaction
* Population-scaled points in the scatter plot
* Hover tooltips with country, region, year, fertility rate, life expectancy, and population
* Linked country trend chart showing selected country changes over time
* Regional comparison chart showing average fertility and life expectancy trends
* Standalone HTML dashboard that works in a browser without a Python server

## Dataset

The project uses a Gapminder dataset with country-level demographic data from 1964 to 2013.

Main variables used in the dashboard:

* `Year`
* `Country`
* `Region`
* `Fertility`
* `lifeExp`
* `pop`

Before visualization, the data is cleaned by removing missing values and standardizing data types. The notebook also creates additional variables for visualization and analysis, including scaled population values for point size and a simple development index for comparing overall progress.

## Dashboard Design

The dashboard contains three coordinated views.

### 1. Animated Scatter Plot

The main scatter plot shows fertility rate on the x-axis and life expectancy on the y-axis. Each point represents a country. Point size represents population, and color represents region.

This chart makes the broad global transition visible: over time, many countries move from the lower-right area of the chart, with high fertility and low life expectancy, toward the upper-left area, with lower fertility and higher life expectancy.

### 2. Linked Country Trend Chart

The linked line chart updates when a country is selected. It shows how fertility rate and life expectancy changed for that country over the full time period.

This makes it possible to move from the global overview to a specific country-level trajectory.

### 3. Regional Comparison Chart

The regional comparison chart shows average fertility and life expectancy trends across regions. It helps reveal regional differences, convergence, and divergence over time.

## Main Findings

The visualization shows several important patterns:

* Most countries experienced a long-term shift toward lower fertility and higher life expectancy.
* Life expectancy became more similar across regions over time.
* Fertility differences between regions remained more visible and, in some cases, became more separated.
* Some countries showed especially strong transformations, with large life expectancy gains and major fertility declines.
* The relationship between fertility rate and life expectancy is generally negative, but the strength of this relationship differs by region.

## Technologies Used

* Python
* Pandas
* NumPy
* Bokeh
* CustomJS
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook

## Project Structure

```text
.
├── README.md
├── project1_final.ipynb
├── gapminder.csv
└── fertility_life_expectancy_dashboard.html
```

`project1_final.ipynb` contains the full code for data cleaning, analysis, visualization design, interactivity, and HTML export.

`gapminder.csv` is the input dataset. It should be placed in the same folder as the notebook.

`fertility_life_expectancy_dashboard.html` is the exported interactive dashboard. It is generated after running the notebook.

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Create a virtual environment

For macOS or Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

For Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install required packages

```bash
pip install pandas numpy matplotlib seaborn bokeh scipy notebook
```

### 4. Add the dataset

Make sure `gapminder.csv` is in the same folder as `project1_final.ipynb`.

### 5. Run the notebook

```bash
jupyter notebook project1_final.ipynb
```

Run all cells in order. The notebook will process the data, build the Bokeh dashboard, and export the final interactive visualization as an HTML file.

### 6. Open the dashboard

After running the notebook, open:

```text
fertility_life_expectancy_dashboard.html
```

The dashboard can be opened directly in a browser. It does not require a running Python server because the interactivity is handled with Bokeh and CustomJS in the browser.

## Usage Guide

Use the dashboard controls to explore the data:

* Move the year slider to inspect a specific year.
* Click autoplay to watch the global trend over time.
* Use the region filter to focus on one region.
* Search for a country to inspect its individual trajectory.
* Click a country point in the scatter plot to update the linked line chart.
* Hover over points to view detailed country-level information.
* Compare regional trends using the regional comparison chart.

## Notes for GitHub

The notebook version included in this repository has been cleaned so that large old outputs are not stored inside the `.ipynb` file. This helps the notebook open faster and makes the repository easier to browse on GitHub.

The main interactive output is the exported HTML file. If the dashboard does not display directly inside GitHub's notebook preview, download or open the HTML file locally in a browser.

## Possible Improvements

Future improvements could include:

* Deploying the dashboard with GitHub Pages
* Adding GDP per capita or education indicators
* Adding more country comparison options
* Improving the page layout for smaller screens
* Adding downloadable filtered data tables
* Including more detailed statistical explanations for regional differences

## License

This project is intended for academic and portfolio use. If you reuse the dataset, please follow the original data provider's terms of use.
