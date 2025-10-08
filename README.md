# PRODIGY_DS_01
Population Data Visualization

# PRODIGY_DS_01: Population Data Visualization

## Project Overview
This project analyzes and visualizes global population data from 1960 to 2024 using a Jupyter Notebook. The dataset includes total population figures for various countries, regions, and aggregates (e.g., "World"). The primary visualization is a line plot showing global population growth over time, created with Seaborn and Matplotlib.

Although the objective specifies creating a bar chart or histogram for the distribution of a categorical or continuous variable (e.g., ages or genders in a population), this notebook focuses on temporal trends in total population. For distribution visualization, a histogram could be adapted (e.g., for population sizes across countries in a specific year), but the current implementation uses a line plot for time-series analysis.

## Objective
Create a bar chart or histogram to visualize the distribution of a categorical or continuous variable, such as the distribution of ages or genders in a population.

(Note: The notebook implements a line plot for global population trends. To align more closely with the objective, consider extending it to include histograms of population distributions by country or region.)

## Dataset
- **Source**: `population data.csv` (sourced from Google Drive in the notebook; likely from World Bank or similar public data).
- **Description**: Contains total population data for countries and regions from 1960 to 2024.
- **Columns** (after processing):
  - `Country Name`: Name of the country or region (e.g., "Aruba", "World").
  - Yearly columns: Population figures from `1960` to `2024`.
- **Key Features**:
  - Includes aggregates like "World" for global totals.
  - Data is numerical (population counts) with potential for time-series and distribution analysis.

## Tools and Libraries
- **Python Version**: 3.x
- **Libraries**:
  - `pandas`: For data manipulation and reading CSV.
  - `numpy`: For numerical operations.
  - `matplotlib.pyplot`: For plotting.
  - `seaborn`: For enhanced statistical visualizations.
- **Environment**: Google Colab (with Google Drive mounting for file access).

## Project Structure
- **PRODIGY_DS_01.ipynb**: The main Jupyter Notebook containing the code.
  - Imports libraries.
  - Mounts Google Drive and loads the dataset.
  - Cleans data by dropping unnecessary columns (`Indicator Name`, `Indicator Code`, `Country Code`).
  - Displays dataset previews.
  - Creates a line plot of global population growth (1960–2023) using Seaborn.
- **population data.csv**: The input dataset (not included in repo; assume it's available or downloadable from sources like World Bank Open Data).

## Steps in the Notebook
1. **Import Libraries**: Load pandas, numpy, matplotlib, and seaborn.
2. **Mount Google Drive**: Access files in Colab.
3. **Load Data**: Read `population data.csv`.
4. **Data Cleaning**: Drop irrelevant columns and preview the data.
5. **Visualization**:
   - Set Seaborn style for aesthetics.
   - Plot global population (`y=data["World"]`) over years (`x=data.index`) as a line graph with markers.
   - Add title, labels, and grid for readability.
   - Display x-ticks every 5 years.

## Visualization Example
The notebook generates a line plot titled "Global Population Growth (1960–2023)":
- **X-Axis**: Years (1960 to 2024).
- **Y-Axis**: Population.
- This shows the continuous growth trend, which could be extended to a histogram for distribution (e.g., population bins across countries).

To create a histogram aligning with the objective:
- Example code snippet (not in notebook, but suggested):
  ```python:disable-run
  # Histogram of population distribution for a specific year (e.g., 2023)
  plt.figure(figsize=(10, 6))
  sns.histplot(data['2023'], bins=20, kde=True, color='skyblue')
  plt.title('Distribution of Population Across Countries/Regions in 2023')
  plt.xlabel('Population')
  plt.ylabel('Frequency')
  plt.show()
  ```

## How to Run
1. Clone the repository:
   ```
   git clone https://github.com/your-username/PRODIGY_DS_01.git
   ```
2. Open in Jupyter/Colab:
   - If using Google Colab, upload the notebook and dataset to Drive.
   - Run cells sequentially.
3. Ensure dependencies are installed:
   ```
   pip install pandas numpy matplotlib seaborn
   ```
4. Mount Google Drive in Colab and update the CSV path if needed.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Data sourced from public datasets (e.g., World Bank).
- Built as part of Prodigy Infotech Internship tasks.
```
