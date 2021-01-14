# Netflix Data Visualization

## Description
This is my first try at data visualization. The project uses a Netflix data set from Kaggle. It can parse the data using Python and create graphs using matplotlib. I only focused on which countries produce the most TV shows and movies on Netflix, but many more data visualizations and analyses can be performed.

## Getting Started
#### Folder setup:
1. Open powershell/terminal
2. Create a folder on your desktop
3. cd into that folder
3. make a project folder
4. cd into project folder
5. make a data folder

#### Get the Data:
1. Get the data csv from
[kaggle.com netflix-shows](https://www.kaggle.com/shivamb/netflix-shows)

2. Add it to the data folder

#### Install Dependencies:
1. Make a venv in your project folder:
    windows: py -m venv venv
    mac/linux: python3 -m venv venv

2. Activate the venv:
    windows: .\venv\Scripts\Activate.ps1
    mac/linux: source venv/bin/activate

3. Install requirements:
    pip install -r requirements.txt

4. Before running Jupyter Lab:
    *point the ipykernel to the venv*
    python -m ipykernel install --user --name=data_vis
    
5. Run Jupyter Lab:
    jupyter lab

#### Importing and setting up our data:
1. Add the following imports to a new .ipynb file:

    import matplotlib.pyplot as plt

    import csv

    from collections import Counter

2. Bring the CSV data into Python and parse it. For example:

```
with open('data/netflix_titles.csv', 'r', encoding ='utf-8') as file:
    netflix_data = csv.DictReader(file)
    data_list = []

    for row in netflix_data:
        data_list.append(row)
```


3. Pull your desired data!