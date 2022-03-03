**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report #3 – Code Coverage, Adequacy Criteria and Test Case Correlation**

| Group \#:       | 7 |
|-----------------|---|
| Student Names:  | Graydon Benson  |
|                 | Eli St. James   |
|                 | Seher Dawar     |
|                 | Maxwell Botham  |

(Note that some labs require individual reports while others require one report
for each group. Please see each lab document for details.)

# 1 Introduction
The purpose of this lab was for the group to develop our knowledge in the area of automated testing and code coverage. By strengthening our code from assignment two with a focus on developing more thorough branch and line coverage, the group developed a better test suite for the methods in the Range Class and Data Utilities Class. The use of automated testing in JUnit with the combination of code coverage in EclEmma was a great way to gain experience testing. Each section of the lab allows the team to refine their skills in the design, development, and execution of testing, and after being able to evaluate the quality of these tests written.

# 2 Manual data-flow coverage calculations for X and Y methods

Range
public boolean contains(double value) {
        return (value >= this.lower && value <= this.upper);
    }
<Image>
  <table>
value: (143,144)
value (nodal): (1,2) , (1,3), (1,4), (1,5), (1,6)

upper: (143,144)
upper (nodal): (1, 4), (1, 5), (1, 6)

lower: (143,144)
lower (nodal): (1, 2), (1, 3)

DU Path Sets
du (1, value) = {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}
du (1, upper) = {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}
du (1, lower) = {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}


DU Pair Sets
du (1, 2, value) = {[1,2]}
du (1, 3, value) = {[1,3]}
du (1, 4, value) = {[1,2,4]}
du (1, 5, value) = {[1,3,5]}
du (1, 6, value) = {[1,2,6], [1,3,6]}
du (1, 7, value) = {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}

du (1, 2, lower) = {[1,2]}
du (1, 3, lower) = {[1,3]}
du (1, 7, lower) =  {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}


du (1, 4, upper) = {[1,2,4]}
du (1, 5, upper) = {[1,3,5]}
du (1, 6, upper) = {[1,3,6], [1,2,6]}
du (1, 7, upper) = {[1,2,4,7], [1,2,6,7], [1,3,6,7], [1,3,5,7]}

positiveIntegerContainsTest()
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

negativeIntegerContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

zeroRangeContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

upperBoundContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

lowerBoundContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

outsideUpperBoundContainsTest()
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

outsideLowerBoundContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

doubleContainsTest() 
DU pairs covered:
value:  (143, 144)
upper: (143, 144)
lower: (143, 144)

We have 100% coverage, as we missed no DU-pairs in contains.


# 3 A detailed description of the testing strategy for the new unit test

Text…

# 4 A high level description of five selected test cases you have designed using coverage information, and how they have increased code coverage

Text…

# 5 A detailed report of the coverage achieved of each class and method (a screen shot from the code cover results in green and red color would suffice)

Text…

# 6 Pros and Cons of coverage tools used and Metrics you report

Text…

# 7 A comparison on the advantages and disadvantages of requirements-based test generation and coverage-based test generation.

Text…

# 8 A discussion on how the team work/effort was divided and managed

Text…

# 9 Any difficulties encountered, challenges overcome, and lessons learned from performing the lab

Text…

# 10 Comments/feedback on the lab itself

Text…
