# ML on Norwegian Fisheries Data

This project explores machine learning on fisheries activity data from the Norwegian Directorate of Fisheries. The work focuses on preprocessing, supervised learning, and clustering on fishery operations data.

## Project overview

The dataset used in this project contains fishery operation records reported by fishing vessels in Norwegian waters. The data mainly consists of Daily Catch Activity (DCA) reports and includes information related to when an activity was reported, when the fishing activity started and stopped, what gear was used, what fish was caught, and basic vessel-related information.

One important characteristic of the dataset is that a single catch activity can appear across multiple rows. Rows belonging to the same operation share the same message ID and the same start and stop times, while the fish-catch fields vary across rows. The dataset also contains Norwegian text and Norwegian number formatting, which made preprocessing an important part of the work.

## Purpose

The purpose of the project was to carry out a complete machine learning workflow on a real-world style fisheries dataset. The work included:

- understanding the structure of the dataset
- selecting and cleaning relevant variables
- preparing the data for modeling
- building several supervised learning models
- building a clustering model
- evaluating results and discussing limitations

## Preprocessing

A large part of the project was devoted to preprocessing. The raw data contains redundancy, repeated fishing operations across multiple rows, and Norwegian terminology. To prepare the dataset for modeling, I focused on:

- identifying meaningful fishing operations
- reducing redundant rows
- cleaning missing and inconsistent values
- translating relevant Norwegian labels and categories
- converting values to suitable numeric and categorical formats
- selecting a manageable modeling scope

Depending on the modeling task, preprocessing can include focusing on one species, one gear type, grouped species categories, or catch amounts for a specific target species.

## Machine learning tasks

The project includes both supervised and unsupervised learning.

### Supervised learning

For the supervised learning part, the goal was to predict or classify fish catch related outcomes based on information about the fishing operation. Possible targets include:

- species caught
- whether a specific species was present
- catch amount for a chosen species
- catch category or grouped fish types

At least three supervised learning models were built and compared, including one deep learning model.

### Unsupervised learning

For the unsupervised learning part, I used clustering to explore whether fishing operations could be grouped into meaningful patterns based on variables such as timing, gear, vessel information, location, and catch composition.

## Methods

The notebook includes:

- data exploration
- preprocessing and feature selection
- model training
- model evaluation and comparison
- clustering analysis
- discussion of strengths and weaknesses in the results

The focus of the project is not only on model performance, but also on making reasonable preprocessing choices and explaining the reasoning behind the full workflow.

## Challenges and limitations

This dataset was not originally collected for machine learning, which creates several challenges:

- repeated rows for the same fishing activity
- mixed data quality across variables
- categorical variables in Norwegian
- missing values and inconsistent formatting
- potentially limited predictive power depending on the chosen target

Because of this, the project should be understood as a practical machine learning investigation on a complex dataset rather than a polished production model.

## Repository contents

```text
.
├── info284_groupExam.ipynb
├── README.md
├── docs/
└── outputs/
```

## Running the project

Install the required libraries first:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn tensorflow jupyter openpyxl
```

Then open the notebook:

```bash
jupyter notebook info284_groupExam.ipynb
```

## Results

The final results should be interpreted in light of the preprocessing decisions, the target chosen, and the overall complexity of the dataset. The main value of the project lies in the full investigation from raw data to evaluated models, as well as the reflections on what worked and what did not.

## Note

The public version of this repository should not include confidential raw course data. If the project is uploaded publicly, it is better to include code, documentation, and descriptions of the workflow rather than the original dataset itself.
