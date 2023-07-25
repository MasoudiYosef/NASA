# A guideline for NASA
This document describes how respected users can utilize the Novel Algorithm for Sequence Alignment (NASA). 

Requirements for running the standalone version of NASA
NASA is executable in all the existing operating systems such as Windows, Linux, and Mac. To run NASA, you need one of the Python programming language versions. The current version has been developed in Python 3.8.0. After installing Python, you need to add numpy library to your operating system environment. To this end, you can follow Figure 1 (pip install numpy):


Figure 1: install numpy

From the required hardware properties perspective, the standalone version of NASA can be exploited in a system with the minimum power of CPU and volume of RAM. However, the higher the power of the computer system, the faster the outcome production process.

The existing functions
The current version of NASA includes 10 distinct functions explained below:
a)CallNasa: This function receives two sequences and calls other procedures to preprocess and score them.

b)Initial: For every residue, this function generates an empty list. It also creates score and counter arrays to show sub-scores and to count a specific residue from the beginning of a sequence to the identified position, respectively.

c)PRE_Positions: For every residue, this step determines what the position of other residues is before a specified position. 

d)SUC_Positions: For every residue, this step determines what the position of other residues is after a specified position.

e)NASA: This procedure applies the residues of shorter sequences to the larger sequence one by one and calls the score function. In other words, this procedure manages the alignment process in terms of specifying the alignment indices and integrating the outcomes.

f)Score: For a given residue, in a range determined by RTB, this function goes through the predefined positions (by the PRE_Positions) and updates the score array and the residues’ counter variable.

g)UpdateSucc: During the scoring step, for every residue, this function updates the residues’ counter variables and returns them to their positions observed before the current one, provided that the score value of the current position is more than the one indicated by the residue’s counter variable. 

h)UpdatePara: Like the UpdateSucc function, the UpdataPara function controls the residues’ counter variables to not exceed their observed range.

i)ShowSequence: Based on the calculated score array and the given sequences, this function determines the approximate relationship between the sequences.

j)ShortAlign: for very short parts of given sequences (at most 10 residues), the ShowSequence function calls the ShortAlign function to specify the matched residues. This function operates based on the classic alignment methods.


# Running the standalone version of NASA
For running the algorithm, import it into your source code and determine its parameters, as shown in Figure 2.


Figure 2: Running NASA and setting its parameters
