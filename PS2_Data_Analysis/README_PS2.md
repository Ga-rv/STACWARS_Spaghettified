# STAC WARS — PS2: Solar Radiation Analysis

This folder contains the code, dataset, generated plots, and report for **Problem Set 2 (PS2)**. The notebooks analyze solar radiation measurements and explore how radiation varies with time of day and environmental factors.

## Folder structure

```text
PS2_Data_Analysis/
├── Mission/
│   ├── PartA.ipynb
│   ├── PartB.ipynb
│   └── PartC.ipynb
├── solar_radiation_data/
│   └── SolarPrediction.csv
├── plots/
│   ├── solar_radiation_vs_time.png
│   ├── radiation_vs_temperature_day.png
│   ├── radiation_vs_humidity_day.png
│   └── correlation_with_radiation.png
├── report/
│   └── Correlations.txt
├── STACWARS_Spaghettified_ps2_report.pdf
├── requirements.txt
└── README.md
```

## Notebooks

### `Mission/PartA.ipynb` — Radiation visualizations

- Converts the `Time` column into a decimal hour value.
- Plots radiation against time of day, including a closer view of low radiation values.
- Groups observations into half-hour time intervals and overlays mean and median radiation.
- Compares daytime radiation with temperature and humidity.
- Colors scatter plots by distance from noon to help show how time of day relates to the observed patterns.

Generated figures:
- `plots/solar_radiation_vs_time.png`
- `plots/radiation_vs_temperature_day.png`
- `plots/radiation_vs_humidity_day.png`

### `Mission/PartB.ipynb` — Correlations

- Calculates correlations between radiation and temperature, humidity, pressure, and wind speed (`Speed`).
- Compares correlations across all observations, daytime observations (06:00–19:00), and near-noon observations (11:00–13:00).
- Displays the results as a heatmap and prints the correlation table.

Generated figure:
- `plots/correlation_with_radiation.png`

The correlation values are measures of association; they do not, by themselves, establish causation.

### `Mission/PartC.ipynb` — Daily and solar-day analysis

- Creates a combined datetime column from `Data` and `Time`.
- Calculates daily maximum, mean, and count of radiation readings.
- Finds the date with the highest recorded radiation and retrieves the corresponding time, temperature, humidity, and wind speed.
- Calculates elapsed time from sunrise to the peak reading.
- Lists the five dates with the highest average radiation.
- Checks humidity values above 100%.
- Identifies the day with the lowest mean radiation among days with at least 200 observations and reports that day's maximum reading.

This notebook prints its results in the notebook; the current code does not save a separate plot from Part C.

## Requirements

The notebooks use Python and the following main packages:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn` (used for the correlation heatmap)
- `jupyter` (to run the notebooks)

Install the packages in the Python environment you intend to use. For example:

```bash
python -m pip install pandas numpy matplotlib seaborn jupyter
```

A `requirements.txt` file is included in this folder. If you use it, check that it is compatible with your Python environment before installing all listed packages; the notebooks only require the main packages listed above.

## How to run

**Important:** The notebooks use relative paths such as `../solar_radiation_data/SolarPrediction.csv` and `../plots/...`. Run them with the notebook working directory set to the `Mission` folder so the paths resolve correctly.

From a terminal, change into this folder:

```bash
cd PS2_Data_Analysis/Mission
```

Then start Jupyter:

```bash
jupyter notebook
```

Open and run the notebooks in this order:

1. `PartA.ipynb`
2. `PartB.ipynb`
3. `PartC.ipynb`

You can also open the notebooks in VS Code, but make sure their working directory is `PS2_Data_Analysis/Mission`. If you run them from a different directory, update the relative file paths accordingly.

## Dataset

The source dataset is `solar_radiation_data/SolarPrediction.csv`. The notebooks use columns including `Data`, `Time`, `Radiation`, `Temperature`, `Pressure`, `Humidity`, `WindDirection(Degrees)`, `Speed`, `TimeSunRise`, and `TimeSunSet`.

## Existing outputs

- `plots/` contains saved figures produced by the visualization and correlation notebooks.
- `report/Correlations.txt` contains a saved correlation table.
- `STACWARS_Spaghettified_ps2_report.pdf` is the report included with this project.

Re-run the relevant notebook cells if you want to regenerate the plots or reproduce the printed analysis results.
