# Grading Bash Scripts
## Introduction
This repository contains Bash scripts I developed to automate my grading process as a TA at NJIT for CS 113, an introductory Java course. While I first started implementing this grading process in Spring 2023, this semester, I plan on improving my Bash scripts to make them more general.
## Documentation
### Organize
This file assumes it is being executed in the same directory as the zip file containing all student submissions downloaded from Canvas. After execution, in the current directory, there will be a submissions directory. The submissions directory contains directories that correspond to each student. Each student's directory will contain their submission's files.
- Removes package declarations
- Addresses file naming issues that arise from multiple identically-named student submissions on Canvas
- Correctly names files for easy compilation and running
- Submissions containing underscores, although uncommon, are problematic for this script
### hw2
#### grade
This file is run in the submission folder's parent directory with the student's directory name as a command line argument. Therefore, if a TA is not grading all student submissions, they may pick and choose which student's submission they will grade. It compiles the files, runs them, and displays the java file contents to the terminal to check for the fulfillment of specific rubric criteria.
#### input
This file should be in the same directory as the previous file. Since one of the files being graded requires user input, this file it used to store the inputs that will be fed into the file being graded by the grader.
### hw3
Initially, I was considering using RegEx patterns to extract methods from each class, comparing them to another RegEx pattern that is a correct implementation of the method. Based on this comparison, I could assign the credit for each method. Although I am eager to try this, I do not believe it is worth investing the time in doing this for this assignment. Instead, I will manually check the class to ensure methods are implemented correctly. However, I will utilize a grading script that compiles the files, runs them, and feeds input into the driver. Then, I will check the output and file to ensure it was done correctly.
#### grade

#### input
