# Female Tennis Match Performance Analysis Using Decision Trees

## Project Overview
This project investigates the match-performance characteristics that contribute to successful outcomes for female tennis players on hard court surfaces. The analysis uses match statistics to explore patterns associated with winning and losing matches and applies Decision Tree classification models to identify the most influential performance variables.
Both a baseline and an optimised Decision Tree model were developed and compared. Model performance was evaluated using cross-validation, confusion matrices, accuracy, precision, recall, and F1-score. Feature importance was also examined to determine which match statistics had the strongest relationship with match outcomes.

The objective of this investigation is to identify and explore the match-performance qualities that contribute to successful performance among female tennis players on hard court surfaces.

The project also aims to determine whether these performance statistics can be used to distinguish between winning and losing match outcomes using a Decision Tree classification model.

The target variable used in the model was Result, where:

- 0 -> Player 1 Loss
- 1 -> Player 1 Win

## Installation and Setup
Project developed: Jupyter Notbook

To run the project locally:

1. Clone or download this repository.
2. Make sure Python is installed on your computer.
3. Install the required Python packages.
4. Place the Bank Marketing dataset in the same project directory as the notebook, or update the dataset path inside the notebook.
5. Female-Tennis-Court-Code.ipynb.
6. Run the notebook cells from top to bottom.
Packages required before: pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter

## Code and Resources Used
Programming Language: Python 3

Development Environment: Jupyter Notebook

Version Control: Git and GitHub

Main Project File: Female-Tennis-Court-Code.ipynb

## Python Packages Used
- PANDAS
- NUMPY
- MATPLOTLIB
- SEABORN
- PLOTLY
- SCIPY
- SCIKIT-LEARN

## Data
The combined dataset contains 452 women's tennis matches from four Grand Slam tournaments held in 2013:

Variables used for the machine-learning model include:
- First serve percentage (FSP)
- First serve points won (FSW)
- Second serve percentage (SSP)
- Second serve points won (SSW)
- Aces (ACE) 
- Double faults (DBF)
- Winners (WNR)
- Unforced errors (UFE)
- Break point created (BPC)
- Break points won (BPW)
- Net point attempts (NPA)
- Net points won (NPW)


## Source Data
Four CSV datasets were used:

- AusOpen-women-2013.csv
- FrenchOpen-women-2013.csv
- USOpen-women-2013.csv
- Wimbledon-women-2013.csv
  
Dataset link:  [Tennis Major Tournament Match Statistics]([https://archive.ics.uci.edu/dataset/222/bank+marketing](https://archive.ics.uci.edu/dataset/300/tennis+major+tournament+match+statistics))


## Data Acquisition
The dataset was obtained as an existing structured dataset and imported into Python using Pandas.
**Aus_F_T = pd.read_csv('AusOpen-women-2013.csv')**

**Fre_F_T = pd.read_csv('FrenchOpen-women-2013.csv')**

**US_F_T = pd.read_csv('USOpen-women-2013.csv')** 

**Wimb_F_T = pd.read_csv('Wimbledon-women-2013.csv')**

Before combining the datasets, the column names were compared because some attributes were labelled differently between tournaments.

The inconsistent column names were standardised before the four datasets were combined into a single DataFrame.



## Conclusion
The results show that match-performance statistics can provide meaningful insight into successful performance in women's hard court tennis. Both the baseline and optimised Decision Tree models were effective in classifying match outcomes, although the optimised model provided a simpler and more interpretable structure.

The baseline Decision Tree contained 61 nodes and achieved a cross-validation score of 0.8504. After optimisation, the model was reduced to 22 nodes while maintaining strong predictive performance. On the test set, the optimised model achieved an accuracy of 91.2%, precision of 89.36%, recall of 93.33%, and an F1-score of 91.30%. The confusion matrix showed that 41 losses and 42 wins were correctly classified, with only six matches misclassified.

Feature importance analysis identified Player 1 Break Points Created (BPC.1) as the most influential performance characteristic. This suggests that creating opportunities to break an opponent's serve may be an important factor associated with successful match outcomes.

Overall, the findings support the objective of identifying performance characteristics associated with success on hard court surfaces. The optimised Decision Tree demonstrated that reducing model complexity can improve interpretability without significantly compromising predictive performance, while also providing useful insight into the match statistics that influence tennis outcomes.

## Acknowledgments and References
The project uses women's Grand Slam tennis match data from the 2013 Australian Open, French Open, US Open and Wimbledon tournaments.

Dataset reference:

Jauhari, S., Morankar, A., & Fokoue, E. (2014). Tennis Major Tournament Match Statistics [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C54C7K.

The project was developed for educational and portfolio purposes to demonstrate data exploration, preprocessing, machine learning, and model evaluation using Python.

## License
This project is released under the MIT License.
