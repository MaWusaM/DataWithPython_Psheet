# DataScienceWithPython_Psheet
This is my Practice sheet from my Data Science with Python course at Great learning

a1 = "Kofi dosen't share Pizza here"
a1
"Kofi dosen't share Pizza here"
a1[5:12]
"dosen't"
len(a1)
29
a1.upper()
"KOFI DOSEN'T SHARE PIZZA HERE"
type(a1)
str
#Tuples: these are immutable;objects cannot be add, removed or changed, contain various number of datatypes
tup1 = (1, "a", True, 23.0)
tup1
(1, 'a', True, 23.0)
tup1[1:4]
('a', True, 23.0)
#List: thses are similar to tuples just that these are mutable, ammenable etc
li = [1,"a", True, 30, "Good", "Nice"]
li
[1, 'a', True, 30, 'Good', 'Nice']
li.append("sword")
li
[1, 'a', True, 30, 'Good', 'Nice', 'sword']
li.append([1,2,3,4,5,6,7,8,9])
li
[1,
 'a',
 True,
 30,
 'Good',
 'Nice',
 'sword',
 [1, 2, 3, 4, 5, 6, 7, 8, 9],
 [1, 2, 3, 4, 5, 6, 7, 8, 9]]
li.pop()
[1, 2, 3, 4, 5, 6, 7, 8, 9]
li
[1, 'a', True, 30, 'Good', 'Nice', 'sword', [1, 2, 3, 4, 5, 6, 7, 8, 9]]
#Dictionaries: contains key are their corresponding values, mutable.
di = {"mango":54,"Ghana":69,"apple":20,"guava":30}
di
{'mango': 54, 'Ghana': 69, 'apple': 20, 'guava': 30}
di.keys()
dict_keys(['mango', 'Ghana', 'apple', 'guava'])
di.values()
dict_values([54, 69, 20, 30])
di["mango"]= 100
di
{'mango': 100, 'Ghana': 69, 'apple': 20, 'guava': 30}
#sets: these are unindexed, collection of values that does not allow duplication and are closed in a curly bracket
s1= {"a", 1, "great", 123, 9+3j, 49027}
s1
{(9+3j), 1, 123, 49027, 'a', 'great'}
s1.add("voice")
s1
{(9+3j), 1, 123, 49027, 'a', 'great', 'voice'}
s1.pop()
1
s1
{(9+3j), 123, 49027, 'a', 'great', 'voice'}
s1.add(1)
s1
{(9+3j), 1, 123, 49027, 'a', 'great', 'voice'}
#if statements
a=10
b=20
if (a>b):
    print("A is greater than B")
else:
    print("B is greater than A")
B is greater than A
a=10
b=20
c=30
if (a>b)&(a>c):
    print("A is the greatest")
elif (b>a)&(b>c):
    print("B is the greatest")
else:
    print("C is the greatest")
C is the greatest
#if statements with tuples
if "a" in tup1:
    print("a is present")
a is present
if "g" in tup1:
    print("g is present")
else:
    print("these are the values present",tup1[0:])
these are the values present (1, 'a', True, 23.0)
#if with list
li
[1, 'a', True, 30, 'Good', 'Nice', 'sword', [1, 2, 3, 4, 5, 6, 7, 8, 9]]
if li[0]==1:
    li[0]=100
li
[100, 'a', True, 30, 'Good', 'Nice', 'sword', [1, 2, 3, 4, 5, 6, 7, 8, 9]]
#if with dictionaries
di
{'mango': 100, 'Ghana': 69, 'apple': 20, 'guava': 30}
if di["mango"]==100:
    di["mango"]=di["mango"]+10

di
{'mango': 110, 'Ghana': 69, 'apple': 20, 'guava': 30}
i=1
while (i<=10):
    print(i)
    i=i+1
1
2
3
4
5
6
7
8
9
10
i=1
n=2
while (i<=10):
    print(n, "*",i,"=", n*i)
    i=i+1
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18
2 * 10 = 20
i=0
l1=[1,2,3,4,5]
while i<len(l1):
    l1[i]=l1[i]+100
    i=i+1
l1
[101, 102, 103, 104, 105]
#for loop with lists
g1=["ama","kwame","manga","wusa"]
for i in g1:
    print(i)
ama
kwame
manga
wusa
color=["green","blue","gray","black"]
item=["bowl","table","shirt","ring"]
for i in color:
    for j in item:
        print(i,j)
       
green bowl
green table
green shirt
green ring
blue bowl
blue table
blue shirt
blue ring
gray bowl
gray table
gray shirt
gray ring
black bowl
black table
black shirt
black ring
#functions
def hello():
    print("Hello World!")
hello()
Hello World!
def add_10(x):
    return(10+x)

    
add_10(5)
15
def odd_even(x):
    if x%2==0:
         print(x, "is even")
    else:
        print(x,"is odd")
odd_even(23)
23 is odd
#object oriented programming
#creating an object phone 
class Phone:

    #defining a method(function inside a class)
    def make_call(self): 
        print("making a call")

    def play_game(self):
        print("playing game")
#assigning the phone object to variable p1
p1=Phone()
#invoking an instance of the class
p1.make_call()
p1.play_game()
making a call
playing game
#adding elements to the class
class Phone:

    def add_color(self, color):
        self.color=color

    def add_cost(self,cost):
        self.cost=cost

    def show_color(self):
        return(self.color)

    def show_cost(self):
        return(self.cost)

    def make_call(self):
        print("making a call")

    def play_game(self):
        print("playing game")

p2=Phone()
p2.make_call()
        
making a call
#adding the cost and color of the object phone
p2.add_color("blue")
p2.add_cost(200)
#calling the color&cost of the object
p2.show_color()
p2.show_cost()
200
#inheritance:transfering the elements of on class to another
class Iphone(Phone):
    def cure_cancer(self):
        print("I can cure Cancer")

    
ip1=Iphone()
ip1.add_color("Gray")
ip1.add_cost(899)
ip1.cure_cancer()
I can cure Cancer
ip1.show_color()
'Gray'
ip1.show_cost()
899
#introduction to numpy
import numpy as np
#creating single array
n1=np.array([10,20,30,40,50])
n1
array([10, 20, 30, 40, 50])
type(n1)
numpy.ndarray
#creating multiple arrays
n2=np.array([[10,20,30,40,50],[60,70,80,90,100]])
n2
array([[ 10,  20,  30,  40,  50],
       [ 60,  70,  80,  90, 100]])
#creating an array containg zero elements
n3=np.zeros((3,3))
n3
array([[0., 0., 0.],
       [0., 0., 0.],
       [0., 0., 0.]])
n4=np.zeros((6,6))
n4
array([[0., 0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0., 0.],
       [0., 0., 0., 0., 0., 0.]])
#creating a numpy with 3x3 dimensions and filling it with the value 7 all way
n5=np.full((3,3),7)
n5
array([[7, 7, 7],
       [7, 7, 7],
       [7, 7, 7]])
#creating and filling an array with a particular serise 
n6=np.arange(10,20)
n6
array([10, 11, 12, 13, 14, 15, 16, 17, 18, 19])
#creating and filling an array with a particular serise with difference of 5
n7=np.arange(10,90,5)
n7
array([10, 15, 20, 25, 30, 35, 40, 45, 50, 55, 60, 65, 70, 75, 80, 85])
#creating an array of random 10n numbers between 100&200
n8=np.random.randint(100,200,10)
n8
array([153, 167, 158, 170, 139, 125, 187, 168, 176, 185])
#checking the shape of a created array
n5.shape
(3, 3)
n4.shape
(6, 6)
#changing the shape of a numpy array
n8.shape=(2,5)
n8.shape
(2, 5)
#arithmetics with arrays
a=np.array([10,20])
b=np.array([30,40])
#summing arrays without axis specification
np.sum([a,b])
100
#summing with axis set to zero; this does vertical summation
np.sum([a,b],axis=0)
array([40, 60])
#summing with axis set to one; this does horizontal summation
np.sum([a,b],axis=1)
array([30, 70])
#joining numpy arrays
#vstack:joins arrays vertically
np.vstack((a,b))
array([[10, 20],
       [30, 40]])
#hstack:joins arrays horizontally
np.hstack((a,b))
array([10, 20, 30, 40])
#column_stack:creates two-dimensional array with the given array
np.column_stack((a,b))
array([[10, 30],
       [20, 40]])
#introduction to pandas: its used for data manipulation and analysis
import pandas as pd
s1=pd.Series([10, 20, 30, 40, 50])
s1
0    10
1    20
2    30
3    40
4    50
dtype: int64
#labeling the index of a panda series
s1=pd.Series([10, 20, 30, 40, 50],index=['a','b','c','d','e'])
s1
a    10
b    20
c    30
d    40
e    50
dtype: int64
#creating series objects from dictionary
s2=pd.Series({'a':10,'b':20,'c':30,'d':40})
s2
#or
d1={'a':10,'b':20,'c':30,'d':40}
s3=pd.Series(d1)
s3
a    10
b    20
c    30
d    40
dtype: int64
#pandas dataframes:these consist of 2-dimensional label structure of data
d1=pd.DataFrame({"Name":['sam','joe','musk','gram'],"marks":[20,30,40,50]})
d1

                
Name	marks
0	sam	20
1	joe	30
2	musk	40
3	gram	50
students={"Students":['sam','joe','musk','gram'],"Marks":[20,30,40,50]}
students
{'Students': ['sam', 'joe', 'musk', 'gram'], 'Marks': [20, 30, 40, 50]}
#creating a data frame from pre-existing dictionary
pd.DataFrame(students)
Students	Marks
0	sam	20
1	joe	30
2	musk	40
3	gram	50
#dataframe in-built functions
iris=pd.read_csv(r"C:\Users\user\Downloads\iris.csv")#reading a file from its directory and assigning it.
iris.head()#viewing the top five rows of the data
Sepal.Length	Sepal.Width	Petal.Length	Petal.Width	Species
0	5.1	3.5	1.4	0.2	setosa
1	4.9	3.0	1.4	0.2	setosa
2	4.7	3.2	1.3	0.2	setosa
3	4.6	3.1	1.5	0.2	setosa
4	5.0	3.6	1.4	0.2	setosa
iris.tail()#viewing the bottom five rows of the data
Sepal.Length	Sepal.Width	Petal.Length	Petal.Width	Species
145	6.7	3.0	5.2	2.3	virginica
146	6.3	2.5	5.0	1.9	virginica
147	6.5	3.0	5.2	2.0	virginica
148	6.2	3.4	5.4	2.3	virginica
149	5.9	3.0	5.1	1.8	virginica
#describing the data
iris.describe()
Sepal.Length	Sepal.Width	Petal.Length	Petal.Width
count	150.000000	150.000000	150.000000	150.000000
mean	5.843333	3.057333	3.758000	1.199333
std	0.828066	0.435866	1.765298	0.762238
min	4.300000	2.000000	1.000000	0.100000
25%	5.100000	2.800000	1.600000	0.300000
50%	5.800000	3.000000	4.350000	1.300000
75%	6.400000	3.300000	5.100000	1.800000
max	7.900000	4.400000	6.900000	2.500000
#accessing specific rows and columns with the iloc(index location)function;it returns the specific rows and columns you called for
iris1=iris.iloc[99:127,2:4]#assigning it to dataframe iris1
iris1
Petal.Length	Petal.Width
99	4.1	1.3
100	6.0	2.5
101	5.1	1.9
102	5.9	2.1
103	5.6	1.8
104	5.8	2.2
105	6.6	2.1
106	4.5	1.7
107	6.3	1.8
108	5.8	1.8
109	6.1	2.5
110	5.1	2.0
111	5.3	1.9
112	5.5	2.1
113	5.0	2.0
114	5.1	2.4
115	5.3	2.3
116	5.5	1.8
117	6.7	2.2
118	6.9	2.3
119	5.0	1.5
120	5.7	2.3
121	4.9	2.0
122	6.7	2.0
123	4.9	1.8
124	5.7	2.1
125	6.0	1.8
126	4.8	1.8
iris2=iris.iloc[10:21,[0,4]]#accessing rows 10 to 20 with columns 1 and 2
iris2
Sepal.Length	Species
10	5.4	setosa
11	4.8	setosa
12	4.8	setosa
13	4.3	setosa
14	5.8	setosa
15	5.7	setosa
16	5.4	setosa
17	5.1	setosa
18	5.7	setosa
19	5.1	setosa
20	5.4	setosa
#accessing data points using the loc()(location)function;this takes row indexes and column names to index data points
iris.head()
iris3=iris.loc[33:44,("Sepal.Length","Petal.Length")]
iris3
Sepal.Length	Petal.Length
33	5.5	1.4
34	4.9	1.5
35	5.0	1.2
36	5.5	1.3
37	4.9	1.4
38	4.4	1.3
39	5.1	1.5
40	5.0	1.3
41	4.5	1.3
42	4.4	1.3
43	5.0	1.6
44	5.1	1.9
iris4=iris.loc[0:11,("Sepal.Length","Petal.Length")]
iris4
Sepal.Length	Petal.Length
0	5.1	1.4
1	4.9	1.4
2	4.7	1.3
3	4.6	1.5
4	5.0	1.4
5	5.4	1.7
6	4.6	1.4
7	5.0	1.5
8	4.4	1.4
9	4.9	1.5
10	5.4	1.5
11	4.8	1.6
#manipulating data based on conditions
iris['Sepal.Length']>5
0       True
1      False
2      False
3      False
4      False
       ...  
145     True
146     True
147     True
148     True
149     True
Name: Sepal.Length, Length: 150, dtype: bool
#extracting data where iris['Sepal.Length']>5 is true
iris[iris['Sepal.Length']>5]
Sepal.Length	Sepal.Width	Petal.Length	Petal.Width	Species
0	5.1	3.5	1.4	0.2	setosa
5	5.4	3.9	1.7	0.4	setosa
10	5.4	3.7	1.5	0.2	setosa
14	5.8	4.0	1.2	0.2	setosa
15	5.7	4.4	1.5	0.4	setosa
...	...	...	...	...	...
145	6.7	3.0	5.2	2.3	virginica
146	6.3	2.5	5.0	1.9	virginica
147	6.5	3.0	5.2	2.0	virginica
148	6.2	3.4	5.4	2.3	virginica
149	5.9	3.0	5.1	1.8	virginica
118 rows × 5 columns

#extracting observations where petal length is greater than 2 and species is virginica to a variable iris_final
iris_final = iris[(iris['Petal.Length']>2) &(iris['Species']=='virginica')]
iris_final.head()
Sepal.Length	Sepal.Width	Petal.Length	Petal.Width	Species
100	6.3	3.3	6.0	2.5	virginica
101	5.8	2.7	5.1	1.9	virginica
102	7.1	3.0	5.9	2.1	virginica
103	6.3	2.9	5.6	1.8	virginica
104	6.5	3.0	5.8	2.2	virginica
#data visualization with matplotlib
from matplotlib import pyplot as plt #importing pyplot from matplotlip
x=np.arange(1,11)
x
array([ 1,  2,  3,  4,  5,  6,  7,  8,  9, 10])
#creating an array one
y1 = 2 * x
y1
array([ 2,  4,  6,  8, 10, 12, 14, 16, 18, 20])
#creating an array two
y2 = 3*x
y2
array([ 3,  6,  9, 12, 15, 18, 21, 24, 27, 30])
#creating a line plot
plt.plot(x,y1)
plt.show()
No description has been provided for this image
#adding color, tittle, labels, line width and style to the plot
plt.plot(x,y1,color='green',linewidth=5,linestyle=':')
plt.title('Line Plot')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.show()
No description has been provided for this image
#ploting multiple lines with color, tittle, labels, line width, style and grid to the plot
plt.plot(x,y1,color='green',linewidth=2,linestyle=':')
plt.plot(x,y2,color='red',linewidth=2,linestyle=':')
plt.title('Line Plot')
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.grid(True)
plt.show()
No description has been provided for this image
students
{'Students': ['sam', 'joe', 'musk', 'gram'], 'Marks': [20, 30, 40, 50]}
names=list(students.keys())
marks=list(students.values())
names
marks
[['sam', 'joe', 'musk', 'gram'], [20, 30, 40, 50]]
#bar plotting
gvt={"sam":20,"bob":30,"joe":40}#dictionary
gvt
names=list(gvt.keys())#extracting the keys as a list
marks=list(gvt.values())#extracting the values as a list
names, marks
plt.bar(names,marks,color='green')
plt.title("Student_Performance")
plt.xlabel("Names_Students")
plt.ylabel("Marks_Students")
plt.show()
No description has been provided for this image
# Horizontal bar plotting
gvt={"sam":20,"bob":30,"joe":40}#dictionary
gvt
names=list(gvt.keys())#extracting the keys as a list
marks=list(gvt.values())#extracting the values as a list
names, marks
plt.barh(names,marks,color='green')
plt.title("Student_Performance")
plt.ylabel("Names_Students")
plt.xlabel("Marks_Students")
plt.show()
No description has been provided for this image
#doing a scatter plot of the of the iris data
plt.scatter(iris['Sepal.Length'],iris['Petal.Width'])
plt.title('ScatterPlot_irisD')
plt.xlabel('Sepal_Length')
plt.ylabel('Petal_Length')
plt.grid(True)
plt.show()
No description has been provided for this image
#histogram
plt.hist(iris['Sepal.Length'],bins=40)
plt.show
<function matplotlib.pyplot.show(close=None, block=None)>
No description has been provided for this image
#box plot petal width by species
iris.boxplot(column='Petal.Width', by='Species')
<Axes: title={'center': 'Petal.Width'}, xlabel='Species'>
No description has been provided for this image
#boxplot with the seaborn library
import seaborn as sns
sns.boxplot(x=iris['Species'],y=iris['Sepal.Length'])
<Axes: xlabel='Species', ylabel='Sepal.Length'>
No description has been provided for this image
#pie chat
plt.pie(marks,labels=names,autopct='%0.2f%%')
plt.show()
plt.figure(figsize=(10,10))#adjusting the size of the chat
No description has been provided for this image
<Figure size 1000x1000 with 0 Axes>
<Figure size 1000x1000 with 0 Axes>
#Data pre processing demo
from sklearn.linear_model import LinearRegression
car_sales = pd.read_csv(r"C:\Users\user\Downloads\car_sales.csv") 
car_sales.head(2).transpose()#viewing data in transpose form
0	1
Unnamed: 0	1	2
Manufacturer	Acura	Acura
Model	Integra	Legend
Type	Small	Midsize
Min.Price	12.9	29.2
Price	15.9	33.9
Max.Price	18.8	38.7
MPG.city	25	18
MPG.highway	31	25
AirBags	NaN	Driver & Passenger
DriveTrain	Front	Front
Cylinders	4	6
EngineSize	1.8	3.2
Horsepower	140	200
RPM	6300	5500
Rev.per.mile	2890	2335
Man.trans.avail	Yes	Yes
Fuel.tank.capacity	13.2	18.0
Passengers	5	5
Length	177	195
Wheelbase	102	115
Width	68	71
Turn.circle	37	38
Rear.seat.room	26.5	30.0
Luggage.room	11.0	15.0
Weight	2705	3560
Origin	non-USA	non-USA
Make	Acura Integra	Acura Legend
car_sales.dtypes#checking the data types in the dataset
Unnamed: 0              int64
Manufacturer           object
Model                  object
Type                   object
Min.Price             float64
Price                 float64
Max.Price             float64
MPG.city                int64
MPG.highway             int64
AirBags                object
DriveTrain             object
Cylinders              object
EngineSize            float64
Horsepower              int64
RPM                     int64
Rev.per.mile            int64
Man.trans.avail        object
Fuel.tank.capacity    float64
Passengers              int64
Length                  int64
Wheelbase               int64
Width                   int64
Turn.circle             int64
Rear.seat.room        float64
Luggage.room          float64
Weight                  int64
Origin                 object
Make                   object
dtype: object
