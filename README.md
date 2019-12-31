# School-Database-Management-

PROCEDURE:-
First we created the tables and inserted the values in to the tables.
Courses Table:-
SQL> create table courses(
  Course_ID number(25),
  Course_names varchar(25),
  Staff_ID number(25),
  Student_ID number(25),
  CONSTRAINT courses_pk PRIMARY KEY(Course_ID,Staff_ID,Student_ID));
Table created.
Insert into courses values(201,’Python’,111,1);
Insert into courses values(202,’AI’,222,1);
Insert into courses values(203,’ML’,333,2);
SQL> select * from courses;
SQL> select * from courses;
 
 COURSE_ID     COURSE_NAMES    STAFF_ID     STUDENT_ID
       201         Python                               111              1
       202         AI                                       222              1
       203         ML                                   333              2
       204         R-prog                               444              3
       205         DBMS                                 555                  4
       206         BESM                                   666                  5
       207         BusiEnvi                             777              6
       208         WebDevelopment                  888              7
       209         Cloudcomputing                   999              8
       210         Datascience                         1211              9
       211         Statistics                          1311             10
       212         Matlab                              1411             11
       213         FinancialManagement         1511             12
       214         C prog                              1611             13
       215         java                                    1711             14
       216         Data structures                     1811             15
       217         Financial Derivatives           1911             16
       218         Mergers                             2011             17
       219         Neural Networks                 2111             18
       222         AWS                                 2121             19
 
20 rows selected.
Students Table:-
SQL> create table students(
  Gender varchar(25),
  first_name varchar(25),
  last_name varchar(25),
  Student_ID number(25),
  Aadhar_no number(25),
  birth_date DATE,
  Age number(25),
  Religion varchar(25),
 CONSTRAINT students_pk PRIMARY KEY(Student_ID));
                Table created.
               Insert into students values(‘F’,’Gunuru’,’Kumari’,1,229611088639,21-Apr-1999,20,Hindu);
    Insert into students values(‘M’,’Gunuru’,’Naveen’,2,268611088769,20-Jan-1999,19,Hindu);
    Insert into students values(‘F’,’Namballa’,’Keerthi’,3,695471089750,18-MAY-1999,21,Muslim);
    
SQL> select * from students;
 
GENDER  FIRST_NAME  LAST_NAME  STUDENT_ID  AADHAR_NO   BIRTH_DAT   AGE     Reli 
F                         Gunuru                    Kumari           1              2.2961E+11             21-APR-99         20   Hindu
M                         Gunuru                    Naveen           2              2.6861E+11             20-JAN-99         19   Hindu
F                         Namballa                  keerthi            3              6.9547E+11            18-MAY-90       21   Muslim
M                         kagitala                  Srinu               4                 6.5826E+11            11-MAR-95       26    Hindu
F                         seepana                   Tanmay            5                5.8713E+11           13-JUN-01         18    Christian
M                         korlam                    karthik            6               2.5796E+11             16-NOV-00       20     Hindu
M                         Bora                      Akhil                  7               2.5578E+11             16-JAN-00       20      Hindu
F                         Gulipilli                 Deepika              8               4.5876E+11              18-DEC-97       22     Hindu
F                         Bathina                   Abhigna             9               4.5875E+11             21-JUN-92       25     Muslim
F                         Pusarla                   Pratyusha         10               2.5976E+11             14-FEB-92       27     Islam
M                         Jitu                        Kunal                11               4.5829E+11            28-AUG-93      25     sikhism
M                         Potunuru               Sagar              12                 2.5649E+12          22-OCT-92       27    Buddhisim
F                         Yedla                       sai                   13                  3.5829E+11         15-FEB-92          26     Christian
M                         Allu                      Nandu                14                6.7833E+11          26-MAR-91       24     Hindu
M                         Deepesh               Kumar              15                 2.6829E+11           11-MAY-92     24      sikhism
M                         Roshan                    Kumar         16                 4.3769E+11              21-MAY-95       26  Buddhisim
F                         pooja                     Shree                17                  2.6568E+11            11-JUN-92       22   Christian
 
Departments Table:-
SQL> create table Department(
  Department_ID number(25),
  Department_name varchar(25));
Table created.
Insert into Department values(100,’Enginering’);
Insert into Department values(101,’Science’);
Insert into Department values(102,’Management’);
SQL> select * from Department;
DEPARTMENT_ID         DEPARTMENT_NAME
          100             Engineering
          101             Science
          102             Management
          103             Pharmacy
          104             Architeture
          105             Law
          106             Medical
          107             Nursing
          108             Psychology
          109             World Languages
          110             Mathematics
          111             Food and Nutrition
          112             Health Services
          113             Geology
          114             Physics
          115             Chemistry
          116             Ecnomics
          117             Accounting
          118             Sociology
          119             Arts
Parents Table:-
SQL> create table parents(
  father_name varchar(25),
  mother_name varchar(25),
  mobile_no number(25),
  Student_ID NOT NULL,
  FOREIGN KEY(Student_ID) REFERENCES students(Student_ID));
         Table created.
Insert into parents values(‘Naidu’,’Parvathi’, 9457832879,1);
Insert into parents values(‘Raju’,’Sandhya’, 9457837679,2);
Insert into parents values(‘Srinu’,’Padmavathi’, 8765832879   ,3);
SQL> select * from parents;
 
FATHER_NAM    E    MOTHER_NAME    MOBILE_NO        STUDENT_ID
Naidu                         Parvathi                      9457832879              1
Raju                          Sandhya                       9457837679             2
Srinu                         Padmavathi                    8765832879               3
Nandu                         Deepika                       7654832879              4
Kiran Kumar                   Harika                        9986432879             5
Mohan                         Lakshmi                       8884832879              6
Vishwa                        Poorna                        7547567439              7
Suresh                    Nalini                                8767835679                  8
Sagar                     Divya                                       7654832876                  9
Karthik                   Hamsikha                              6785839876                 10
Kishore                   Teja                                        7254832986                 11
Mahesh                   namrutha                              8975832897                 12
Rajesh                    Priya                                 8436832444                 13
Ram                       Sindhu                                6787833456                14
Varun                     Bhanu                                 7123832665                 15
Sharath                   Ramya                                    6678835876                 16
karan Pratap         Tejaswi                                    8765832886                 17
Rajesh                    Raashi                                 6123832446                 18
Pradeep                 Amrutha                                 8898832557                 19
Surendra               Varsha                                  7789832223                 20
School Table:-
SQL> create table school (
Staff_id number(25),
Staff_name varchar(25),
Staff_role varchar(25));
Table created
Insert into school values(111,’karan’,’prof’);
Insert into school values(222,’neelam’,’asst.prof’);
Insert into school values(333,’josh’,’Associate.prof’);
SQL> SELECT * FROM SCHOOL;
 
  STAFF_ID     STAFF_NAME        STAFF_ROLE
       111         karan                         prof
       222         neelam                        asst.prof
       333         josh                          Associate.prof
       444         priya                         Associate.prof
       555         vishnu                        prof
       666         Nagalakshmi             principal
        777         Yasodha                       Asst.principal
       888         Yamini                        JR.proff
       999         Leela                         SR.proff
      1211         Maya                          JR.Asstproff
      1211         Maya                          SR.Asstproff
      1311         jony                          Receptionist
      1411         rick                          system tester
      1511         rick                          chemical tester
      1711         rocky                         peon
      1811         fatima                        Teacher
      1911         Leben                         Coordinator
      2011         Divakar                       Asst.Coordinator
      2111         rupa                          HOD
      2121         keerti                        lecturer
                                                               QUERIES
Get details of the students
SQL> select * from students;
Print number of students from the student table
SQL> select count(student_id) from students;

COUNT(STUDENT_ID)
               20
Print first_name,last_name from students where age greater than 2
SQL> select first_name,last_name from students where age > 22; 
FIRST_NAME                LAST_NAME
kagitala                      Srinu
Bathina                       Abhigna
Pusarla                       Pratyusha
Jitu                          Kunal
Potunuru                      Sagar
Yedla                         sai
Allu                          Nandu
Deepesh                       Kumar
Roshan                        Kumar
Ratan                         Yadav
Sourabh                       Kumar

Print first name and last name whose gender is male from students
SQL> select first_name,last_name from students where gender = 'M';
FIRST_NAME                LAST_NAME
Gunuru                        Naveen
kagitala                      Srinu
korlam                        karthik
Bora                          Akhil
Jitu                          Kunal
Potunuru                      Sagar
Allu                          Nandu
Deepesh                       Kumar
Roshan                        Kumar
Ratan                         Yadav
Sourabh                       Kumar

Print number of females in the students table
SQL> select COUNT(first_name) from students where gender = 'F';
COUNT(FIRST_NAME)
                9

Print Maximum and Minimum age of the students  
SQL> select MAX(age), MIN(age) from students;
MAX(AGE)     MIN(AGE)
28               18

Print  staff name  whose  course id is 208
SQL> select staff_name from school where staff_id in (select staff_id from courses where course_id = 208);

STAFF_NAME
Yamini

Print  staff details  who  are  professors
SQL> SELECT * FROM school WHERE staff_role='prof';
      STAFF_ID         STAFF_NAME          STAFF_ROLE
           111             karan                         prof
                  555         vishnu                        prof

Print student_id who do not enroll the course DBMS
        SQL> select student_id from students where student_id NOT IN
                2   (select student_id from courses where course_id IN
                3  (select course_id from courses where course_names = 'DBMS'));
STUDENT_ID
                     1
                     2
                     3
                     5
                     6
                     7
                     8
                     9
                    10
                    11
                    12
13
14
15
16
17
18
19
20

Print department names whose department is between 100 and 110
SQL> select department_name from department
2  where department_id BETWEEN 100 AND 110;
DEPARTMENT_NAME
-------------------------
Engineering
Science
Management
Pharmacy
Architeture
Law
Medical
Nursing
Psychology
World Languages
Mathematics

11 rows selected.

Print the course deails and staff details
SQL>SELECT * FROM courses left join school on courses.staff_id =school.staff_id;
COURSE_ID  COURSE_NAMES  STAFF_ID  STUDENT_ID  STAFF_ID  STAFF_NAME  STAFF_ROLE
201         Python                      111          1                    111        karan                     prof

Print the student details whose first name have letter ‘ll’ in their names
SQL> select * from students where FIRST_NAME like '%ll%';
GENDER  FIRST_NAME  LAST_NAME  STUDENT_ID  AADHAR_NO  BIRTH_DAT  AGE  RELIGION
F                      Namballa       keerthi      3                   6.9547E+11   18-MAY-90     21 Muslim

F                      Gulipilli           Deepika    8                   4.5876E+11      8-DEC-97      22 Hindu

M                     Allu                 Nandu      14                 6.7833E+11     26-MAR-91    24  Hindu

Print the average age of the students
SQL> select avg(age) from students;
AVG(AGE)
23.6

Print the religion count of the students
SQL> select religion, count(religion) as count from students group by religion;
RELIGION                       COUNT
--------------------             ----------
Muslim                             2
Islam                                 1
Buddhisim                        3
Christian                           3
Hindu                                7
sikhism                              4

6 rows selected.

Print student names along with parent names
SQL> SELECT last_name,father_name,mother_name FROM students join parents on students.student_id =parents.student_id;
LAST_NAME                 FATHER_NAME      MOTHER_NAME
Kumari                        Naidu                         Parvathi
Naveen                        Raju                          Sandhya
keerthi                       Srinu                         Padmavathi
Srinu                         Nandu                         Deepika
Tanmayi                       Kiran Kumar                   Harika
karthik                       Mohan                         Lakshmi
Akhil                         Vishwa                        Poorna
Deepika                       Suresh                        Nalini
Abhigna                       Sagar                         Divya
Pratyusha                     Karthik                       Hamsikha
Kunal                         Kishore                       Teja
Sagar                         Mahesh                        namrutha
sai                           Rajesh                        Priya
Nandu                         Ram                           Sindhu
Kumar                         Varun                         Bhanu
Kumar                         Sharath                       Ramya
Shree                         karan Pratap                  Tejaswi
Yadav                         Rajesh                        Raashi
Kumar                         Pradeep                       Amrutha
Shree                         Surendra                      Varsha

Print student names with their ages in ascending order
SQL> SELECT  last_name,age FROM students order by age asc;
LAST_NAME                          AGE
Tanmayi                                 18
Naveen                                19
Kumari                                20
karthik                                   20
Akhil                                     20
keerthi                                   21
Shree                                     22
Deepika                               22
Kumar                                 24
Kumar                                    24
Nandu                                 24
Abhigna                              25
Kunal                                     25
sai                                       26
Kumar                                    26
Srinu                                     26
Pratyusha                            27
Sagar                                     27
Yadav                                 28
Shree                                     28

Print student last name and age with ALL operator whose religion is  Hindu
SQL> select last_name,age
 2  from students
3  where age > ALL
4  (SELECT age from students where religion='Hindu');
LAST_NAME               AGE
Pratyusha                        27
Sagar                                 27
Yadav                             28
Shree                                 28




Print student last_name, first_name , age with ANY operator whose age is greater than 20
SQL> select last_name,first_name,
2  age from students
3  WHERE age > ANY
4  (select age from students where age > 20);
LAST_NAME                 FIRST_NAME            AGE
Yadav                         Ratan                                 28
Shree                         Tanu                                  28
Sagar                         Potunuru                         27
Pratyusha                     Pusarla                               27
Srinu                         kagitala                              26
Kumar                         Roshan                           26
sai                           Yedla                     26
Kunal                         Jitu                                  25
Abhigna                       Bathina                           25
Nandu                         Allu                                  24
Kumar                         Deepesh                          24
Deepika                       Gulipilli                            24

Print course names whose staff_id is equal to course_id 
SQL> SELECT course_names FROM courses WHERE EXISTS (SELECT * FROM school WHERE course_id = staff_id);
COURSE_NAMES
AWS

Creating a VIEW and print a VIEW  of Female students
SQL> CREATE VIEW female_students AS SELECT first_name, last_name FROM students WHERE gender='F';
FIRST_NAME                LAST_NAME
------------------------- -------------------------
Gunuru                        Kumari
Namballa                      keerthi
seepana                       Tanmayi
Gulipilli                     Deepika
Bathina                       Abhigna
Pusarla                      Pratyusha
Yedla                         sai
pooja                         Shree
Tanu                          Shree

9 rows selected.

A correlated query to print staff name and their role
SQL> select a.staff_name,a.staff_role
2  from school a
3  where a.staff_id=(
4  select b.staff_id
5  from courses b where b.staff_id=222);
STAFF_NAME            STAFF_ROLE
------------------------- -------------------------
neelam                        asst.prof

Print father_name whose student opted for Artificial Intelligence
SQL> select father_name, mobile_no from parents where student_id in (select student_id from courses where course_names='AI');
FATHER_NAME          MOBILE_NO
-------------------------     ----------
Naidu                         9457832879

A correlated query to print maximum age of the student with a certain condition
SQL> select last_name, first_name, age, student_id from students s1 where age =(select max(age) from students where student_id<s1.student_id);
LAST_NAME                 FIRST_NAME                       AGE         STUDENT_ID
Sagar                         Potunuru                          27                 12
Shree                         Tanu                                  28                 20

Print course id which intersects the staff id
SQL> select course_id from courses intersect select staff_id from school;
COURSE_ID
----------
           222

Print students first and last names along with the parent names
SQL> select first_name, last_name from students union select father_name, mother_name from parents;
FIRST_NAME                LAST_NAME
Allu                          Nandu
Bathina                       Abhigna
Bora                          Akhil
Deepesh                       Kumar
Gulipilli                     Deepika
Gunuru                        Kumari
Gunuru                        Naveen
Jitu                          Kunal
Karthik                       Hamsikha
Kiran Kumar                   Harika
Kishore                       Teja
Mahesh                        namrutha
Mohan                         Lakshmi
Naidu                         Parvathi
Namballa                      keerthi
Nandu                         Deepika
Potunuru                      Sagar
Pradeep                       Amrutha
Pusarla                       Pratyusha
Rajesh                        Priya
Rajesh                        Raashi
Raju                          Sandhya
Ram                           Sindhu
Ratan                         Yadav
Roshan                        Kumar
Sagar                         Divya
Sharath                       Ramya
Sourabh                       Kumar
Srinu                         Padmavathi
Surendra                      Varsha
Suresh                        Nalini
Tanu                          Shree
Varun                         Bhanu
Vishwa                        Poorna
Yedla                         sai
kagitala                      Srinu
karan Pratap                  Tejaswi
korlam                        karthik
pooja                         Shree
seepana                       Tanmayi

40 rows selected.

Print Course names whose student age is greater than 22
SQL> select course_names from courses where student_id in (select student_id from students where age>22);
COURSE_NAMES
-------------------------
DBMS
Datascience
Statistics
Matlab
FinancialManagement
C prog
java
Data structures
Financial Derivatives
Neural Networks
AWS

11 rows selected.

Print staff details whose staff role is HOD
SQL> select * from school where staff_role like 'HOD';
  STAFF_ID     STAFF_NAME            STAFF_ROLE
----------     -------------------------     -------------------------
      2111     rupa                          HOD

Print course_names along with respective staff_id whose staff role is Professor
SQL> select course_names, staff_id from courses where staff_id in(select staff_id from school where staff_role like 'prof');
COURSE_NAMES         STAFF_ID
-------------------------        ----------
Python                                  111
DBMS                               555

Print student details whose student_id has 1 in their ID
SQL> select last_name, first_name from students where student_id in (select student_id from courses where student_id like '%1');
LAST_NAME                 FIRST_NAME
------------------------- -------------------------
Kumari                        Gunuru
Kunal                         Jitu


Print the count of staff roles
SQL> select staff_role, count(staff_role) as count from school group by staff_role;
STAFF_ROLE                     COUNT
-------------------------          ----------
prof                                       2
Associate.prof                      2
SR.Asstproff                          1
Coordinator                            1
JR.Asstproff                           1
system tester                          1
chemical tester                        1
peon                                       1
asst.prof                              1
Asst.principal                         1
SR.proff                               1
lecturer                                   1
Receptionist                           1
HOD                                    1
principal                              1
JR.proff                               1
Teacher                                1
Asst.Coordinator                       1

18 rows selected.

