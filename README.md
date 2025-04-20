# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import matplotlib.pyplot as plt
x1=[1,2,3]
y1=[2,4,1]
plt.plot(x1,y1,label="line 1",linewidth=6)
x2=[1,2,3]
y2=[4,1,3]
plt.plot(x2,y2,label="line 2",linewidth=6)
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title("Two lines on same graph")
plt.legend()
```
![img-1](https://github.com/user-attachments/assets/b073253b-1aeb-4653-8ec4-0fd3f307d2cb)

```
import matplotlib.pyplot as plt
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='blue',linestyle='dashed',linewidth=4,marker='o',markerfacecolor='red',markersize=14)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Some Cool Customizations')
```
![img-2](https://github.com/user-attachments/assets/ab5d303a-5d1c-447c-83c1-f8516132faa1)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896,]
plt.plot(years,apples,color='red',linewidth=5)
plt.plot(years,oranges,color='orange',linewidth=5)
plt.xlabel('YEAR')
plt.ylabel('Yields (tons per hectare)')
plt.title('Crop Yields in Kanto')
plt.legend(['Apples','Oranges'])
```
![img-3](https://github.com/user-attachments/assets/cc00d565-16c1-43dd-b67c-f4647f626d3b)

```
import matplotlib.pyplot as plt
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.scatter(x_values,y_values,s=100,c='red')
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Scatter Plot')
```
![img-4](https://github.com/user-attachments/assets/ee584de7-fee9-4bef-b645-72ed384e058c)

```
import matplotlib.pyplot as plt
x_values=[1,2,3,4,5,6,7,8,9,10]
y_values=[2,4,5,7,6,8,9,11,12,12]
plt.scatter(x_values,y_values,label='stars',marker='*',s=300,c='black')
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Scatter Plot Star')
plt.legend()
plt.savefig("StarScatter.png")
```
![img-5](https://github.com/user-attachments/assets/69f1ce35-d243-4eba-ac46-690c42feab0b)

```
import matplotlib.pyplot as plt
x=[1,2,3,4,5,6,7,8,9]
y=[1,4,9,16,25,36,49,64,81]
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Scatter Plot Star')
plt.subplot(2,2,1)
plt.plot(x,y,'ro--')
plt.subplot(2,2,2)
plt.plot(y,x,'g*--')
plt.subplot(2,2,3)
plt.plot(x,x,'bo')
plt.subplot(2,2,4)
plt.plot(y,y,'go')
```
![img-6](https://github.com/user-attachments/assets/edd80780-004e-42b4-8e36-184b6180596f)

```
import numpy as np
np.pi
```
![img-7](https://github.com/user-attachments/assets/7226002e-51ad-404b-a478-8b2d51439175)

```
X=np.arange(0,4*np.pi,0.1)
Y=np.sin(X)
plt.title("Sin Wave Form")
plt.plot(X,Y,linewidth=5,c='green',linestyle='dotted')
```
![img-8](https://github.com/user-attachments/assets/9096874f-c996-4b1b-87a3-bc95c72f9224)

```
import matplotlib.pyplot as plt
import numpy as np
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='red')
plt.fill_between(x,y2,color='blue')
plt.plot(x,y1,color='black')
plt.plot(x,y2,color='white')
plt.legend(['y1','y2'])
plt.show()
```
![img-9](https://github.com/user-attachments/assets/f41a06bc-090f-4a45-ae3b-56a874b4ac77)

```
import matplotlib.pyplot as plt
height = [10,24,36,40,5]
names=['One','Two','Three','Four','Five']
c1=['r','g']
plt.bar(names,height,width=0.8,color=c1)
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Bar Graph')
```
![img-10](https://github.com/user-attachments/assets/e99d3879-69c1-458b-967b-bf0fb8b85049)

```
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='g')
plt.bar(x2,y2,color='b')
plt.xlabel('X-AXIS')
plt.ylabel('Y-AXIS')
plt.title('Bar Graph')
```
![img-11](https://github.com/user-attachments/assets/a052324f-18c0-4ad7-af57-956553dafe57)

```
import matplotlib.pyplot as plt
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range=(0,100)
bins=10
plt.hist(ages,bins,range,color='blue',histtype='bar',rwidth=0.8)
plt.xlabel('age')
plt.ylabel('no.of people')
plt.title('Histogram')
```
![img-12](https://github.com/user-attachments/assets/9b532721-20d9-47e3-9aa2-bd0c29913d60)

```
import matplotlib.pyplot as plt
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='black',alpha=0.5)
plt.show()
```
![img-13](https://github.com/user-attachments/assets/75317110-a94f-4bc8-9763-6dcfdee4559f)

```
import matplotlib.pyplot as plt
import numpy as np
np.random.seed(0)
data = np.random.normal(loc=0,scale=1,size=100)
data
```
![img-14](https://github.com/user-attachments/assets/4a370671-4bb3-42f0-ba14-289c7e176d30)

```
fig,ax=plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Value')
ax.set_title('Box Plot')
```
![img-15](https://github.com/user-attachments/assets/85348cc8-831a-4566-a3cb-18a1574bc2cc)

```
import matplotlib.pyplot as plt
activities=['Eat','Sleep','Work','Play']
slices=[3,7,8,6]
colors=['yellow','blue','orange','red']
plt.pie(slices,labels=activities,colors=colors,startangle=90,shadow=True,explode=(0,0.1,0,0),autopct='%1.1f%%')
plt.title('Pie Chart')
plt.show()
```
![img-16](https://github.com/user-attachments/assets/602ad61d-7335-45fb-b16e-d0c19bf922d7)

```
labels=['Python','C++','Ruby','Java']
sizes=[215,130,245,210]
colors=['orange','yellow','red','blue']
explode=(0.1,0,0.1,0)
plt.pie(sizes,explode=explode,labels=labels,colors=colors,autopct='%1.1f%%',shadow=True,startangle=90)
plt.axis('Equal')
plt.show()
```
![img-17](https://github.com/user-attachments/assets/704edacf-dbe1-4f5f-97f6-001c793c2716)

# Result:
 Thus the program to perform Data Visualization using matplot python library for the given datas is implemented
