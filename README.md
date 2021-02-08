# Hurricanes.csv

# Load the data from the dataset into your program and plot a Bar Graph of the data, taking
#the Year as the x-axis and the number of hurricanes occurring as the Y-axis. 

import pandas as pd
import matplotlib.pyplot as plt

df=pd.read_csv('Hurricanes.csv')
df.head()
x=df['Year']
y=df['Hurricanes']
#plt.xlim(0,10)
#plt.ylim(10,50)
plt.bar(x,y,color='red')
plt.show()


# Plot the histogram of the temperatures over this period for the cities of San Francisco and Moscow.

import pandas as pd
import matplotlib.pyplot as plt

df=pd.read_csv('CityTemps1.csv')
df.head()
plt.hist(df.Moscow,color='red')
plt.hist(df.SanFrancisco,color='blue')
plt.xlabel('Temperature')
plt.ylabel('Frequency')
plt.show()

# Create csv file from the data file available in LMS which goes by the name ‘M4_assign_dataset’ and read this file into a pandas data frame

df = pd.to_csv('M4_assign_dataset')

# Let the x axis data points and y axis data points are. Draw a Simple plot

x = [1,2,3,4]
y = [20, 21, 20.5, 20.8]

plt.bar(x,y)
plt.plot(x,y)

# Configure the line and markers in simple plot
plt.grid
plt.show()

# configure the axes
plt.setp(plt.gca().get_xticklabels(),rotation=90,horizontalalignment='right')
plt.show()


#Give title of Graph & labels of x axis and y axis

plt.title('show')
plt.xlabel('Temperature')
plt.ylabel('Frequency')

# Give error bar if y_error = [0.12, 0.13, 0.2, 0.1]

y_error = [0.12, 0.13, 0.2, 0.1]
plt.plot(x,y,y_error)
plt.show()

# define width, height as figsize=(4,5) DPI and adjust plot dpi=100
plt.figure(figsize(3,4),dpi=100)

# Give a font size of 14

plt.rcParams.update({'font.size': 14})

#Draw a scatter graph of any 50 random values of x and y axis

import numpy as np
x=np.random.random(50)
y=np.random.random(50)
plt.scatter(x,y)


# Create a dataframe from following data

arr = {'first_name': ['Jason', 'Molly', 'Tina', 'Jake', 'Amy'],
        'last_name': ['Miller', 'Jacobson', 'Ali', 'Milner', 'Cooze'],
        'female': [0, 1, 1, 0, 1],
        'age': [42, 52, 36, 24, 73],
        'preTestScore': [4, 24, 31, 2, 3],
        'postTestScore': [25, 94, 57, 62, 70]}

df = pd.DataFrame(arr)
df

#Draw a Scatterplot of preTestScore and postTestScore, with the size of each point determined by age

s1=df['age']
plt.scatter(df.preTestScore,df.postTestScore,s=s1)
plt.show()

#Draw a Scatterplot from the data in question 9 of preTestScore and postTestScore with the size = 300 and the color determined by sex

colors=df['female']
plt.scatter(df.preTestScore,df.postTestScore,c=colors,s=300)
plt.show()
