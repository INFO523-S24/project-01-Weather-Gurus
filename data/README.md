# Data
-   **[Dataset]**: Description of the dataset 

# Codebook for [chosen] Dataset

## Variable Names and Descriptions:

-   **variable**: Description

## Data Types:

-   **Column**: data type

Below you can find the datasets and a brief description of the variables.
:::

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

#### Northern Hemisphere Annomalies and Description

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

#### Southern Hemisphere Annomalies and Description

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

#### Zonnal Annomalies and Description

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


