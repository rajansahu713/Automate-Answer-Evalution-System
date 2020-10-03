## Automate-Answer-Evalution-System
● A database is created at first along with a student table. (employee.db)

● An interface is built up using python flask to accept answers from students.

● There are two types of questions namely- Short type and Descriptive type.

● For evaluating Short questions we have taken 3 parameters into consideration. They are

keyword matching, grammar checking (using API), synonym checking(You need to download 'GoogleNews-vectors-negative300.bin' from https://s3.amazonaws.com/dl4j-distribution/GoogleNews-vectors-negative300.bin.gz).

● For evaluating Descriptive questions we have taken 1 more parameter i.e length

checking. Suppose for writing an essay if the given word limit is 400 words and a student

has written everything relevant but the essay has ended within 300 words, then marks

will be deducted considering the word limit.

● After evaluation, the student will not be able to see his/her marks but the marks will be

stored in the database.

● Total marks and other relevant information will be accessed by the institution/admin end.

## Demo

[![Watch the video](https://www.youtube.com/watch?v=B0dVSpPT2h0)

https://www.youtube.com/watch?v=B0dVSpPT2h0


## Requirement 

1. Python

2. Flask

3. Tensorflow


