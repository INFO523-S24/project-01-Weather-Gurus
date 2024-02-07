---
title: "Global Temperature Datasets"
format: html
editor: visual
jupyter: python3
---

# Dataset Description

This repository contains datasets about temperature changes across different geographical zones of the Earth, sourced from the TidyTuesday project. The temperature datasets were featured in the week of July 11, 2023, available on their GitHub repository [here](https://github.com/rfordatascience/tidytuesday/tree/master/data/2023/2023-07-11).

## Data

### Global Temperatures (`global_temps.csv`)

- **Description**: The global temperatures dataset encompasses worldwide temperature averages, providing a comprehensive overview of climate change on a global scale.
- **Dimensions**: 144 rows × 19 columns


```{python}
#| label: load-global
#| message: false
#| echo: false

global_temps

```

```{python}
#| label: load-global-description
#| message: false
#| echo: false

print(tabulate(global_temps_description, headers='keys', tablefmt='pipe', showindex=False, stralign='center'))

```





### Northern Hemisphere Temperatures (`nh_temps.csv`)

- **Description**: This dataset focuses on temperature changes within the Northern Hemisphere, offering detailed insights into seasonal and annual temperature variations.
- **Dimensions**: 144 rows × 19 columns

```{python}
#| label: load-nh
#| message: false
#| echo: false

nh_temps

```

```{python}
#| label: load-nh-description
#| message: false
#| echo: false

print(tabulate(nh_temps_description, headers='keys', tablefmt='pipe', showindex=False, stralign='center'))

```


### Southern Hemisphere Temperatures (`sh_temps.csv`)

- **Description**: The Southern Hemisphere temperatures dataset provides a detailed look at temperature trends and changes in the Southern Hemisphere.
- **Dimensions**: 144 rows × 19 columns

```{python}
#| label: load-sh
#| message: false
#| echo: false

sh_temps

```

```{python}
#| label: load-sh-description
#| message: false
#| echo: false

print(tabulate(sh_temps_description, headers='keys', tablefmt='pipe', showindex=False, stralign='center'))

```


### Zonal Annual Temperatures (`zonann_temps.csv`)

- **Description**: This dataset breaks down temperature data by specific zones, offering a granular view of climate change across different latitudes.
- **Dimensions**: 143 rows × 15 columns


```{python}
#| label: load-zonann
#| message: false
#| echo: false

zonann_temps

```

```{python}
#| label: load-zonann-description
#| message: false
#| echo: false

print(tabulate(zonann_temps_description, headers='keys', tablefmt='pipe', showindex=False, stralign='center'))

```



## Codebook for Datasets

### Variable Names and Descriptions

For all datasets, the following variables are commonly found:

- `Year`: The year of the observation.
- `Jan` to `Dec`: Average temperatures for each month.
- `J-D`: The annual average temperature.
- `D-N`: The December to November average temperature.
- `DJF`, `MAM`, `JJA`, `SON`: Seasonal average temperatures for Winter, Spring, Summer, and Autumn, respectively.

### Data Types

#### Global, Northern Hemisphere, and Southern Hemisphere Temperatures

- `Year`: Integer
- Monthly columns (`Jan` to `Dec`): Float
- `J-D`, `D-N`, `DJF`, `MAM`, `JJA`, `SON`: Float








#### Zonal Annual Temperatures

- `Year`: Integer
- `Glob`, `NHem`, `SHem`, and zonal breakdowns (`24N-90N`, `24S-24N`, etc.): Float

```{python}
#| label: load-zonann
#| message: false
#| echo: false

zonann_temps

```

```{python}
#| label: load-zonann-description
#| message: false
#| echo: false

print(tabulate(zonann_temps_description, headers='keys', tablefmt='pipe', showindex=False, stralign='center'))

```



---

Please refer to the specific dataset files for more detailed analysis and exploration of the temperature data. Each file is provided in CSV format for easy use with a variety of data analysis tools and software.


```{python}
#| label: load-dataset
#| message: false
#| echo: false

# Read in manually
global_temps = pd.read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-07-11/global_temps.csv')
nh_temps = pd.read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-07-11/nh_temps.csv')
sh_temps = pd.read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-07-11/sh_temps.csv')
zonann_temps = pd.read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-07-11/zonann_temps.csv')

global_temps_description = pd.read_csv("global_temps_description.csv")
nh_temps_description = pd.read_csv("nh_temps_description.csv")
sh_temps_description = pd.read_csv("sh_temps_description.csv")
zonann_temps_description = pd.read_csv("zonann_temps_description.csv")
```



