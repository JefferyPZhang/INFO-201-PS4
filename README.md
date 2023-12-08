# INFO 201 Problem Set: Data Frames
October 31, 2023

1 Working directory
Before we get into any work with data, we have to talk about working directory.
1. What is the working directory of your RStudio console?
2. What is the folder where your homework .rmd file is saved?
3. Are these the same folder? Why does it matter?
1
2 Create your own data
Here your task is to create a dataset of student grades, and do some related computations
1. Create a vector “names” with (at least) 5 names in it
2. Create a vector “math” with grades (0 - 100) in a math course, one grade for each student.
Hint: you can just invent these numbers, but you can also create random data, e.g.
by sample(100, 5, replace=TRUE) (there are other options, check out the documenta-
tion).
3. Create a vector “japanese” with grades for the Japanese course (use different numbers,
not exactly the same as for math)
4. Create a similar vector “dance” with grades for a dance class
5. Create a data frame “grades” by combining your names, and math, Japanese and dance
grades
6. Compute the number of students in your data!
7. Compute number of courses in data– number columns in your data minus one (b/c of
their names)
8. Print the last two lines of your data
9. Save your students’ data into a new .csv file inside of data/ directory as “grades.csv”
(you may need to create it first). You can save either as comma-separated or as tab-
separated. We recommend to use write_tsv or write_csv functions from readr library.
use relative path for saving!
10. Use list.files() to show that your saved grades.csv is there
3 Indirect variable names
1. create a variable “col” that contains name of one of the courses–dance.
2. Print your dance grades using the variable “col”. Do not use the word “dance” here!
3. Now assign name of another course to “col” and print the best grade in that course!
4. Now write a for-loop over all columns in the data frame Inside of the loop, print the
name of the variable, and its average value
Hint: you cannot compute average “name”. Add an if-else statement there that checks
if variable is numeric and only print average if it is (check out is.numeric()).
4 Data manipulations
1. Compute
GPA = 1
3 (math + Japanese + dance)
Use vectorized operations, not loops! Save it as variable ’gpa’ in your data frame, and
show that it is there.
2
2. Who has the best GPA? Print that line of your data!
3. Now print only the best student’s name
4. Now print your data. Did you get the name right?
5. Compute variable that is TRUE/FALSE, depending on if the student better at math
than in Japanese
Show three lines of your data that includes the new variable.
6. How many students are there in your data who are better at math than in Japanese?
5 Life expectancy
In this section we work with a real dataset life-expectancy.csv (canvas: files/data). It is based
on gapminder data, and represents life expectancy and GDP per capita for most countries in
1960 and 2010. The non-obvious variables are
le life expectancy at birth
GDP_PC GDP per capita
5.1 Load data
1. Load the csv file.
2. How many rows and columns does it contain?
3. Print its variable names
4. print a few lines of the data.
The lines your printed should look like a dataset with text, numbers, and maybe a few
missing values. It should not look carbled or empty. Does it look good? Explain!
5. what does each row in this dataset represent?
6. write a loop over all variables that prints the variable name, and a number of missing
values in that variable.
Comment it: which variables are good, which ones not-so-good?
5.2 Analyze data
1. Create a new variable in the dataset–the growth in life expectancy from 1960 to 2019.
Display a few lines of your augmented data to show it worked.
2. What is the average improvement in LE over these years?
3. Which country gained most in terms of LE and which country gained least?
4. How many countries were there where LE improved less than 5 years?
5. How many countries were there were LE decreased over this time period?
