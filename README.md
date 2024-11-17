# EmbSW_Tasks

In this repository the mandatory tasks included in the course EmbeddedSoftware are included. 

Task 1: 
Pascal's triangle is an arithmetic and geometric figure where each line resembles the sum of the coefficients of the upper line. The first few lines look like this:   

         1
       1  1
    1   2   1
 1   3    3   1

The numbers of the next line can either be calculated by the sum of the upper two neighbors, or by using the binomial exponent calculation.
You can choose any implementation you like, but make sure that the full behavior is covered by unit tests.
It should be possible to output at least the first ten lines of the triangle, and the formatting of the output must be done in a way that the output when displayed in fixed size font (e.g. at the console) resembles the triangle shape.
The number of lines to produce is provided as command line parameter. (e.g. "~> pascal 5"). If no number is given 10 lines are to be displayed.
It is ok if the numbers are represented by 3 digit fixed size, e.g., 001, 025, 120, ... for easier formatting.

Please make sure you are familiar with the assessment criteria and check that you fulfill them before submitting the assignment. Make sure your code is readable, and use comments for documenting the parameters passed to each function and the expected return values.

Think about your functional design and make sure all functions are covered by unit tests. As proof please add the UnitTest Report. 

Please use the Github Assignment link (https://classroom.github.com/a/vnbFj_aD) to create a repository.
Compile and functionality will be verified based on that submission.

Task 2:  
# Seat Assignment Problem

You write a short program which reads a csv file containing students, and you produce a seating list for an exam seating in a room which has a defined number of seats in predefines positions (given as rows and columns). Your program makes sure the students are evenly distributed, and the result of your program is a csv file which contains the students plus the assigned seats (row, column).

(0,0,X)   (0,1,0)   (0,2,X)   (0,3,0)   (0,4,X)
(1,0,X)   (1,1,0)   (1,2,X)   (1,3,0)   (1,4,X)

This is a room with 10 seats in 2 rows, you assign 6 students. Then the resulting csv file will contain a list of students plus seat:

student1, 0, 0
student2, 0, 2
student3, 0, 4
student4, 1, 0
student5, 1, 2
student6, 1, 4

If you try to assign more than 6 students this should fail because there will not be an empty space between them. If you assign e.g. 4 students, try to place them evenly, where sitting behind is better than sitting diagonal. In this case a solution might be

student1, 0, 0
student2, 0, 2
student3, 0, 4
student4, 1, 2

This sample is small by intent to show the principle. For testing purposes, please assume a room that has 6 rows by 8 seats. Provide different input files with different numbers of students, and describe how you distribute them in the room. Please note that the csv file of course shall contain the student's names as provided in the input file (and maybe also the ID).

Think about your functional design and make sure all functions are covered by unit tests. This will be checked as well. Think about applying the object oriented principles you learned.


Task 3: 
Your friend owns a restaurant. He asks you to provide a program which allows to track the name of people sitting at the tables. The tables have fixed locations and distances, which are known by the program. Find a proper data representation for that information. The table locations and distances are read from a csv file; please define a proper format.

The visitors must be registered when they sit down, and the time of leaving must be registered as well. It must be possible to find guests who were at or near a table (the distance is given in the request) at a specific time interval. The data must be available for at least 14 days.
In case of a match all persons must be notified, therefore you either need an address or (better) a phone number.

Please note that for simplicity it is sufficient to store one contact person per group, together with the number of group members. Data can be stored in csv files again; please define a proper data structure.

Hint: If you store contacts per day in one file, the file can simply be removed after the holding time (minimum 14 days).

The Github Classroom is provided here: https://classroom.github.com/a/6eJS8zzK
