# Airbnb Data Cleaning

A Jupyter notebook that starts cleaning an Airbnb listings dataset with pandas, keeping only the columns that are useful for analysing listings, hosts and prices.

## Dataset

`AirBnb_DataSet/Airbnb_Open_Data.csv` (about 35 MB): 102,599 Airbnb listings in New York City (Manhattan, Brooklyn, Queens, the Bronx and Staten Island) with 26 columns, including host details, neighbourhood, coordinates, room type, construction year, price, service fee, minimum nights, reviews and house rules.

## Tech Stack

- Python 3
- pandas
- Jupyter Notebook

## Cleaning Steps

The notebook (`AirBnb_DataSet/NoteBook.ipynb`) currently does the following:

1. Loads `Airbnb_Open_Data.csv` into a pandas DataFrame.
2. Lists the dataset's columns.
3. Drops the columns not needed for the analysis: `id`, `number of reviews`, `last review`, `reviews per month`, `review rate number`, `calculated host listings count`, `availability 365`, `house_rules` and `license`.

This leaves 17 columns: `NAME`, `host id`, `host_identity_verified`, `host name`, `neighbourhood group`, `neighbourhood`, `lat`, `long`, `country`, `country code`, `instant_bookable`, `cancellation_policy`, `room type`, `Construction year`, `price`, `service fee` and `minimum nights`.

## How to Run

```bash
pip install pandas notebook
cd AirBnb_DataSet
jupyter notebook NoteBook.ipynb
```

Run the cells from top to bottom (**Kernel → Restart & Run All**). The CSV is read with a relative path, so the notebook must be started from the `AirBnb_DataSet` folder.
