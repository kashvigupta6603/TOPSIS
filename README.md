# TOPSIS using Python

This project implements the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method using Python.
It ranks multiple alternatives based on multiple criteria and produces a TOPSIS score and rank for each alternative.

## Files in this Repository

- topsis.py : Command-line TOPSIS implementation
- topsis.ipynb : Google Colab / Jupyter Notebook version
- data.csv : Sample input data file
- output.csv : Output file generated after running the program

## Input File (data.csv)

- Input file must be in CSV format
- First column contains the name of alternatives
- From second column onwards, all values must be numeric
- Minimum three columns are required

Example input file:

Fund Name,P1,P2,P3,P4,P5  
M1,0.67,0.45,6.5,42.6,12.56  
M2,0.60,0.36,3.6,53.3,14.47  
M3,0.82,0.67,3.8,63.1,17.10  

## How to Run (Command Line)

python topsis.py data.csv "1,1,1,1,1" "+,+,+,+,+" output.csv

## Parameters Explanation

- data.csv : Input data file
- 1,1,1,1,1 : Weights for criteria
- +,+,+,+,+ : Impacts (+ for benefit, - for cost)
- output.csv : Output file name

## Output File (output.csv)

The output file contains all input columns along with:
- Topsis Score
- Rank (1 indicates the best alternative)

## TOPSIS Methodology

1. Normalize the decision matrix
2. Apply weights to normalized values
3. Determine ideal best and ideal worst solutions
4. Calculate distance from ideal best and worst
5. Compute TOPSIS score
6. Rank alternatives based on the score

## Requirements

- Python 3
- Pandas
- NumPy

## Note

The notebook file (topsis.ipynb) is provided only for testing and demonstration.
The final evaluation-ready implementation is the command-line program (topsis.py).

## Author

Academic implementation of TOPSIS using Python.
