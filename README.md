# League of Legends – Is Leona OP?

**Name(s):** Dimitrij Eli

## Introduction

The dataset used in this project contains detailed match-level and player-level statistics from professional League of Legends games. It includes information on champions, player roles, in-game events, and early-game performance metrics, providing a strong foundation for both exploratory data analysis and predictive modeling. Gaining an initial understanding of the structure and scope of the data is a crucial first step in the data science lifecycle.

Several questions emerge naturally from this dataset. For instance, how much do early-game advantages influence the final outcome of a match? Are certain champions associated with higher win rates? And to what extent can match outcomes be predicted using only information from the early stages of the game?

### Central Research Question

This project focuses on the following research question:

- **Is Leona a better pick as a support champion when it comes to winning a game?**

This question motivates the first part of the analysis, which examines champion-specific performance with a particular emphasis on Leona’s impact as a support pick.

### Prediction Objective

Building on the hypothesis-driven analysis, the project then shifts toward a predictive task. The goal is to determine whether early-game information, specifically statistics from the first 10 minutes of a match, is sufficient to predict the final outcome of a game. This objective provides a coherent theme that connects data exploration, hypothesis testing, and prediction.

---

## Data Cleaning and Exploratory Data Analysis

### Data Cleaning

To ensure a focused and consistent analysis, the dataset was reduced to a subset of relevant columns. The selected variables are grouped based on their purpose within the project.

#### General Columns
These columns are required for identifying games and assessing data completeness:
- `gameid`
- `datacompleteness`
- `league`
- `playerid`

#### Columns for Hypothesis 1
These features are used to analyze champion-related performance and in-game outcomes:
- `position`
- `champion`
- `gamelength`
- `result`
- `kills`
- `deaths`
- `assists`
- `teamkills`
- `teamdeaths`

#### Columns for Hypothesis 2 and Prediction
These early-game features capture events and advantages within the first 10 minutes and are used for the prediction task:
- `firstblood`
- `firstdragon`
- `goldat10`
- `xpat10`
- `csat10`
- `golddiffat10`
- `xpdiffat10`
- `csdiffat10`
- `killsat10`
- `assistsat10`
- `deathsat10`

---

### Dataset Overview (Placeholder)

The table below provides an overview of the cleaned dataset after selecting the relevant columns.

| Column Name | Description | Example Value |
|------------|-------------|---------------|
| *Placeholder* | *Placeholder description* | *Placeholder* |

> **Note:** This table serves as a placeholder. You can later replace it with a table generated from your analysis, for example by summarizing columns, missing values, or sample rows. GitHub supports Markdown tables directly, or you can export a table from Python and paste it here.

---

### Removal of Team-Level Rows

Upon inspection of the `position` column, rows labeled as `team` were identified as team-level statistics rather than individual champion or player statistics. Since the subsequent analyses focus on champion performance and player-level outcomes, all team-level rows were removed from the dataset before proceeding.
