

We have a total of eight instances. The folders in each instance are the same four folders of T, C, K, and D, and the format of the instance size is "Class-Number of Courses-Number of Teachers-Number of Weeks".
The scale of each instance is shown in the following table

| instance | scale |
|  ----  | ----  |
| Instance1  | 4-5-5-18 |
| Instance2  | 3-5-5-18 |
| Instance3  | 4-7-7-18 |
| Instance4  | 8-30-28-18 |
| Instance5  | 10-30-28-18 |
| Instance6  | 8-32-28-18 |
| Instance7  | 8-30-30-18 |
| Instance8  | 8-30-28-20 |


# Data description

The data of each instance is divided into four folders: T, C, K, and D.

## Simplified description of the processing of the data

1. Number all teachers, the number can be seen in table K-K0.xlsx;
2. All course numbers, numbered can be seen in Form C-C0.xlsx;
3. All class numbers, the number can be seen in T table -T0.xlsx;
4. The number of classrooms of each type, see Table D-D.xlsx;
5. Simplify the time period and divide it into 5 time periods a day. Suppose you attend classes 5 days a week for a total of 25 time periods. Suppose a semester of 18 weeks, and study 8 is 20 weeks.
6. Class hours are not currently simplified to sections, because 3 lessons at a time in the evening class require 3 credit hours; During the day, 2 lessons are taught at a time, and 2 hours are recorded.
7. Professional experiments completed within one week are not considered and treated as special courses.

## Description of the contents of the table

1. Table D：

   1. Table T0：Class Number Table. Classes and their corresponding numbers are recorded.

   2. T1-T10：Majors table for each class. That is, the class cannot schedule classes during that time period. where T2-5 is the same and T6-10 is the same, there are no duplicate files here. The first row in the table represents the number of weeks, the first column represents the time period, the position of the number in the middle represents the lesson, and the course of each number can be found below the table。
2. Table C: Table C0: Course Information Form. The number of the course, the name, the corresponding class of the class, the number of the teacher, the number of class hours, and the number of soft constraints are recorded. The soft constraint numbers are shown in the appendix.
3. Table K: Form K0: Teacher Information Form. The teachers and their corresponding numbers are recorded, and the time period when each teacher has an affair. where soft constraint 2 is merged with this table. The time portion, each column is a time period of the week, each behavior is a teacher's information, corresponding to the intersection of the weeks of things.
4. Table D: The number of classrooms of each type is recorded

## Appendix: Table C Soft Constraint Correspondence

The soft constraint order of table C is encoded as follows:

1. Teachers try to avoid 1 and 2 a.m. and 7 or 8 p.m. class hours: Most teachers have special matters to deal with during this time 
2. Teachers have other schedules at certain times of the week and cannot schedule classes: some teachers have meeting schedules, or need to travel, etc. **(merged into Form K)**
3. Classes or classes taught by the same teacher are scheduled to take place in two adjacent time periods: for example, if a teacher is also responsible for teaching two courses on computer network technology and databases, he will prefer to schedule both courses in the morning or afternoon on the same day**（Table C example: Lessons numbered 15 and number 24 should be attended together: 3:24 3:15) **
4. Some courses are scheduled to complete all class hours within a certain number of weeks: for example, the course mathematical modeling is scheduled to complete all class hours from the first week to the ninth week**（Table C: The first half of the semester is scheduled: 4:1, 9)**
2. A course is scheduled to take place after the end of a particular course or at the same time: for example, operations research (ii) is scheduled to be conducted after the end of operations research (i), and econometrics and financial management are arranged to end in the same week
3. Some courses are arranged in succession for a specific period of time, and up to four sessions are arranged: for example, the matlab logistics management experimental course requires four consecutive sessions to be taught
7. The more difficult courses should be arranged as separately as possible: for example, calculus and C++ should not be arranged on the same day as possible, and the arrangements should be arranged separately to alleviate students' academic pressure
2. Different courses have different maximum lessons in a week: e.g. operations research can be arranged up to four times a week **(Example C: two lessons a week: twice a week: 8:2)**
3. Do not run multiple consecutive time periods or consecutive days: for example, try to arrange the operations research every other day, rather than arranging four class hours a week in adjacent time periods or two adjacent days.
10. Several lessons a week are scheduled in the evening (three consecutive lessons)**(Example C: one evening lesson a week: 10:1)**
2. Teachers want to attend classes at a certain time**(Example C: Wednesday night 9-12: 11:15)**
