Introduction
This project is aboyt analyzing data from the historical disaster Titanic sinks. I will begint the analysis with looking into the data and make sure of following the tidy data outlines as possible. Also I will be using Python and four data analysis libraries: Pandas, Numpy, Matplotlib, Scipy, and Seaborn. In order to answer the questions that will be asked during the next steps and tell the true story. :)

Questions
"Joy, then. But the figures are awkward. As the Telegraph admits, in first class over a third of the men, almost all of the women and all the children survived. In second it was less than 10 per cent of the men, 84 per cent of the women and all the children. But in steerage 12 per cent of the men, 55 per cent of the women and less than one in three of the children survived. Interrogating the figures shows that - despite the strict 'women and children first' policy - a greater proportion of first class men survived, than of third class children." Full story

We conclude that some passengers had a preference for success based on their social status, regardless of their age or sex.

Did social class have an effect on survival rates?
Did sex have an effect on survival rates?
Did age, regardless of gender, have any effect on survival rates?

Dataset Description
(from https://www.kaggle.com/c/titanic)

survival: Survival (0 = No; 1 = Yes)
pclass: Passenger Class (1 = 1st; 2 = 2nd; 3 = 3rd)
name: Name
sex: Sex
age: Age
sibsp: Number of Siblings/Spouses Aboard
parch: Number of Parents/Children Aboard
ticket: Ticket Number
fare: Passenger Fare
cabin: Cabin
embarked: Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)

Variable Notes
pclass: A proxy for socio-economic status (SES)

1st = Upper

2nd = Middle

3rd = Lower

age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

sibsp: The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister

Spouse = husband, wife (mistresses and fiancés were ignored)

parch: The dataset defines family relations in this way...
Parent = mother, father

Child = daughter, son, stepdaughter, stepson

Some children travelled only with a nanny, therefore parch=0 for them.

============================
Cousins, nieces and nephews, aunts and uncles, and in-laws were also excluded from this study. Furthermore, some people traveled with very close friends or neighbors, but such relationships apparently aren't supported by the definitions.

According to kaggle


I started the anlysis with importing the packages and set plots to be embedded inline. Then I looked closely at the data. Using the functions of the libraries you imported such as shape() dtypes() head() info() etc...
After that, I found some data that needed to be fixed and cleaned, so I deleted the repeated values and identified the columns that I would need in the analysis process, which will contribute to raising the efficiency of the analysis and answering the questions posed in advance. This was followed by some decrease in the age data of passengers, whose total was approximately 177, which represents 20% of the entire data, which is a huge number. Later, I looked at the ages of the passengers, the types of their classes, and the number of passengers in each class inside the ship, and I found that there are infants under the age of one year. 

 And I got here...
Class 1 - female survival rate: 96.81%
Class 1 - male survival rate: 36.89%
-----
Class 2 - female survival rate: 92.11%
Class 2 - male survival rate: 15.74%
-----
Class 3 - female survival rate: 50.0%
Class 3 - male survival rate: 13.54%
And then I started the analysis process for the first question, which was did social class have an effect on survival rates?


From the statistics, it appears that C3 passengers had a similar survival rate as the C1 passengers, with 119 and 136 passengers surviving, respectively. Looking at the whole number of passengers and the percentage of passengers in each class, the calculation suggests that a passenger in Class 1 has about 2.5 times as much chance of surviving than a passenger in Class 3.
Class 1: 62.96%, Class 2: 47.28%, Class 3: 24.24%

And then I moved to the second question, did women have higher chance to survival than adult male? and women have a higher survival rate than men. "Laddy first" may have played a role in the survival of many people, according to the graphs.

And then I moved to the third question and concluded the analysis process, did age, regardless of gender, have any effect on survival rates?

We can conclude that no matter the gender the servive rate of Adult is lower than the survive rate of Children.

Conclusion
In the analysis, the results of the analysis do suggest that a female with an upper social-economic class would have better chance of surviving the Titanic disaster. Than if she wasn't a member of the upper social class. I could not find a significant correlation between age and surviving due to the huge missing data. The third class was the least likely to survive for one who was a man. Generally speaking, the survival rate of children and women is higher than that of men in general, however, this was not a guarantee.