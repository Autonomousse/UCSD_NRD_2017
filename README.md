# UCSD_NRD_2017

UCSD Health - NRD 2013 and 2017 IBD Research

## Proposal

Develop new prediction models using tree based algorithms to identify healthcare patients who require extensive hospital utilization. These patients will be defined as high-need, high cost (HNHC). With a successful model, our goal is to create a tool that empowers hospitals to identify HNHC patients ahead of time and be able to put cost saving measures in place, while still providing satisfactory service.

## Findings

Starting with the patients in the Nationwide Readmission Database (NRD) from 2013, we extracted and transformed the data, merging it with other available data to create our cohort. Patients consist of adults who were hospitalized with inflammatory bowel disease (IBD) since these patients typically have high hospital utilization costs due to unplanned hospitalizations. HNHC patients are a subgroup of IBD patients who have the most healthcare utilization. Of this subgroup of HNHC patients, we found the top decile and used that group as our final cohort.

Using this cohort and all of the features associated with them, we ran Recursive Feature Elimination (RFE) to identify the top features in three model types. By using RFE and not hand selecting features, we are allowing an algorithm to articulate which features it deems the most important based on the parameters that are given. This also negates any confirmation bias that a researcher may have based on prior knowledge of feature importance as RFE has no outside knowledge of how these features may be related to the target variable. 

The three models consisted of a traditional Logistic Regression (LR) model, a Decision Tree Classifier (DTC) model, and a gradient boosted decision tree model referred to as XGBoost (XGB). Passing in the features from RFE, we came to the conclusion that the tree based models were outperforming the logistic regression model. Established on these findings, we decided to validate our models and feature selections by attempting to replicate our work on the 2017 NRD dataset. There were a few features that were missing or had different definitions when NRD swapped from ICD-9 to ICD-10 codes. ICD is the International Classification of Diseases and Related Health Problems, a globally accepted standard coding practice which is updated from time to time.

Below we can see some of the comparisons between the two years, 2013 (test set) and 2017 (validation set):

[insert charts here]

There is strong evidence that tree based models such as DTC and XGB are outperforming traditional models like LR. We can conclude that the tree based models are significantly better than traditional models at predicting patients who are at risk of becoming HNHC.


## Getting Started

See below for required tools in order to run or replicate this project. Users may have to install and set up certain programs/software, links provided where applicable/available.

### Prerequisites and Installation

* [Python](https://www.python.org/) - Working Python coding environment with editor of choice.
* [pandas](https://pandas.pydata.org/) - Data analysis and manipulation tool.
* [NumPy](https://numpy.org/) - Scientific computations including statistics.
* [matplotlib](https://matplotlib.org/) - Visualization tool for Python.
* [scikit-learn](https://scikit-learn.org/stable/) - Machine learning library for Python.
* [Dask](https://dask.org/) - Allows advanced parallelism for analytics.
* [tqdm](https://tqdm.github.io/) - Progress timer for processes.
* [Jupyter Notebook](https://jupyter.org/) - Breaks down workflow processes into steps for validation.
* Please install any additional Python dependencies, as needed, depending on your coding environment.

## Steps to Run Code

1. Install and set up all of the prerequisites per the instructions provided by the developers.
2. Create a clone of the repository to your local system.
3. [continue once we know what files will be available on the repo]

## Built With

* [Python](https://www.python.org/) - Working Python coding environment with editor of choice.
* [pandas](https://pandas.pydata.org/) - Data analysis and manipulation tool.
* [NumPy](https://numpy.org/) - Scientific computations including statistics.
* [matplotlib](https://matplotlib.org/) - Visualization tool for Python.
* [scikit-learn](https://scikit-learn.org/stable/) - Machine learning library for Python.
* [Dask](https://dask.org/) - Allows advanced parallelism for analytics.
* [tqdm](https://tqdm.github.io/) - Progress timer for processes.
* [Jupyter Notebook](https://jupyter.org/) - Breaks down workflow processes into steps for validation.
* [Visual Studio Code](https://code.visualstudio.com/) - Open source code editor.

## Contributors

[do we want links to github, linkedin, elsewhere?]
* [Nghia Nguyen](https://github.com/nghia-h-nguyen) - 
* [Alexander Qian](https://github.com/alexsqian) - 
* [Peter Chen](https://github.com/datailluminations) - 
* [Sagar Patel](https://github.com/Autonomousse) - 

## Acknowledgments

* [HCUP](https://www.hcup-us.ahrq.gov/) - Largest collection of longitudinal hospital care data in the United States.
* [ICD10Data.com](https://www.icd10data.com/) - Medical coding reference.
[need to site where we got nrd data, hospital data, severity data?]
[any others?]

## Publications and Recognition

[should we add the acceptance we got for the proposal here?]

## License

All rights reserved 2020. The team members (contributors) above own all rights to the project and code they have created.
[does ucsd health have a specific license we need to include, some other licenses?]