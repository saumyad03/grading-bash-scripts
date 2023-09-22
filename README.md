# Grading Bash Scripts
## Introduction
This repository contains Bash scripts I developed to automate my grading process as a TA at NJIT for CS 113, an introductory Java course. While I first started implementing this grading process in Spring 2023, this semester, I plan on improving my Bash scripts to make them more general.
## Documentation
### Organize
**Note:** This file assumes that it is being executed in a directory that contains a submissions folder, containing all the student submissions that were downloaded from Canvas and extracted from the zip file.
**Key Features:**
- Creates directories that correspond to each student, containing that student's files
- Corrects file naming issues that arise from downloading files from Canvas in bulk and multiple student submissions on Canvas
**Limitations:**
- Submissions containing underscores, although uncommon, are problematic
