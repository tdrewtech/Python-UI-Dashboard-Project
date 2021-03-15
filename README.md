# Google Play Store Analytics
<img src="https://raw.githubusercontent.com/fafilia/capstone-UIFlask/master/full_capstone.png">
## Introduction
This project is about a simple web application (dashboard) using the Flask framework. This project will focus on the appearance of the Flask user interface. 

## Data Summary
The data used in this project is scraping data from the Google Playstore App. It consists of several variables with the following details:
- `App`: Application name
- `Category`: Application's category
- `Rating`: The overall rating given by the application user (when scraped)
- `Reviews`: Number of reviews given by application users (when scraped)
- `Size`: Application size (when scraped)
- `Installs`: Number of users who installed / downloaded the application (When scraped)
- `Type`: Application type (paid / free)
- `Price`: Application price (when scraped)
- `Content Rating`: The age group of this app is targeted - Children / Mature 21+ / Adult
- `Genres`: Application's genre.
- `Last Updated`: The date when the application was last updated on the Play Store (when it was scraped)
- `Current Ver`: Current version of the app available on Play Store (when scraped)
- `Android Ver`: Minimum Android version required (when scraped)

## Dependencies
- Flask
- Matplotlib
- Pandas
- Numpy

You can install all these modules by:
```
pip install -r requirements.txt
```

## Rubrics
In this project, the goal is to to build a Flask application that focuses on user interface. The first step is to download or clone this repository. The file in this repository is a skeleton for creating a Flask application dashboard. In the `app.py` and` templates / index.html` section there are several missing sections that you must complete. Some of the parts that must be considered are as follows:


### 1. Repository Github Setting and Environment (2 poin)
- Repository 

a. Create a new repository on Github

b. Clone the repository to local with git clone
- Environment

1. Created virtual environment called "capstone-flask"

The first thing to do is to set the conda environment. To prepare the conda environment and kernel, please use the following command:

```
conda create -n <ENV_NAME> python=3.7
conda activate <ENV_NAME>

conda install ipykernel
python -m ipykernel install --user --name <ENV_NAME>
```

2. Install packages: pandas, flask, matplotlib, and numpy
All dependecies have been exported into the requirements.txt file. Therefore, to install packages, you can use the following command:

```
pip install -r requirements.txt --user
```

### 2. Data Preprocessing and Exploratory Data Analysis (2 points)
In this preprocessing stage, you must duplicate data, change data types and modify data values. In the file `app.py` complete the overlapping data without changing the existing preprocessing flow.
The following are examples of sections that you must complete when preprocessing data:
``
playstore ._________ (subset = "_____", keep = '_____', inplace = True)
playstore.drop ([10472], inplace = True)
# Remove comma (,) and plus (+) then change the data type to an integer
playstore.Category = playstore.Category.astype ('category')
playstore.Installs = ________. apply (lambda x: x.replace (______))
playstore.Installs = ________. apply (lambda x: x.replace (______))
``
### 3. Data Wrangling
- Data wrangling is used to prepare the right data according to the analysis requested. In this capstone there is a dictionary object with the name `stats` and you are required to complete the gaps in order to generate the appropriate data / values. As an illustration, in the `stats` object there is a variable` rev_table` to group and aggregate the data used to create a data table as shown below:
<img src = "https://raw.githubusercontent.com/fafilia/capstone-UIFlask/master/table_rev.PNG" width = 400>

### 4. Data Visualization
- Create plot bars depicting top 5 Categories on Google Playstore
- Create a scatter plot that describes the distribution of the application when viewed based on reviews, ratings, and the number of installed applications.
- Create plot histograms to view application size distribution
- Create a bar chart to compare the average price of every categories

* Notes: You can see other examples of plots that should be created in this repository. Please clone / download this repository.

### 5. Build Flask App
Referring to the fourth point of Data Visualization above, apart from creating new plots you should demonstrate how to render these plots in a Flask application and display them on templates / html pages. All you need to pay attention to is the `app.py` section:
``
render_templates (__________)
``
and in `templates / index.html` you need to call the source plot.png where you will save the plot images.
``
<img src = "________________________" height = "450" ​​width = 500>
``
