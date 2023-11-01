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
#### grade
Instructions identical to hw2.
#### input
Instructions identical to hw2.
### hw4
Due to the complexity of this homework, it was manually graded.
#### dependencies
This file is run in the submission folder's parent directory. Die.java and Point.java must also be in the same directory as this file, because this script places these files in each of the student's respective directories.
### hw5
#### grade
While previous grading scripts automated grading by letting a TA pass the student directory's name as a command line argument to the grader, this one automatically iterates through each student's directory. This file is run in the submission folder's parent directory. It goes into each student's directory, compiles the files, runs them with automatically fed input, and displays that to ensure the code is written correctly. This script allows the TA to go through each of these steps individually, clicking enter once they're ready to move on. That way, they may assign points appropriately on the rubric for each step without being bombarded with terminal output.
### input
This file should be in the same directory as grade. It stores user input needed for the driver program and is used by the grade script.
### hw6
#### grade
This week's homework will use a grader that iterates through each student's directory like hw5. However, we will have to manually grade the files, because the homework involves writing methods which can be done in multiple ways. This file is run in the submission folder's parent directory. Die.java should also be placed in the same directory, so the grader can place it into each student's directory prior to compilation. After compiling the files, the grader displays the file to standard output for manual grading. Then, it runs the file so the output can be analyzed and graded.
## Ideas
For grading class definitions, we can utilize RegEx patterns as follows:
1. Extract method using more generic RegEx pattern
2. Grade method using specific RegEx pattern representative of the correct answer
3. If RegEx doesn't match, manually check method
For grading methods, we can write Java programs that call the methods with multiple test cases in order to ensure method accuracy.
