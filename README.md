# EX8-Implementation of Hierarchical Clustering using linkage methods
## DATE:
## AIM:
To implement Hierarchical Clustering using single and complete linkage method

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Compute the distance matrix between all data points.

2.Identify the two closest cluster and merge them.

3.Update the distance matrix to reflect the new cluster.

4.Repeat steps 2 and 3 until only one cluster remains.

## Program:
```
/*
Program to implement Hierarchical Clustering using single and complete linkage method
Developed by: JENISHA TEENA ROSE F
RegisterNumber: 2305001010

*/
import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.cluster.hierarchy import dendrogram, linkage,fcluster
 from sklearn.preprocessing import StandardScaler
 import pandas as pd
 import numpy as np
 import matplotlib.pyplot as plt
 from scipy.cluster.hierarchy import dendrogram, linkage,fcluster
 from sklearn.preprocessing import StandardScaler
x = df[['StudentID','Marks']].values
x
z=linkage(x,method='complete')
plt.figure(figsize=(5,2))
plt.title("Dendogram for student segmentation")
labels=range(1,len(df)+1)
dendrogram(z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
max_cluster=2
clusters=fcluster(z,max_cluster,criterion='maxclust')
clusters
plt.figure(figsize=(5,2))
plt.scatter(x[:,0],x[:,1],c=clusters,cmap='rainbow',s=100)
plt.title("Student segmented(Hierarchical clustering)")
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()
z=linkage(x,method='single')
plt.figure(figsize=(5,2))
plt.title("Dendogram for student segmentation")
labels=range(1,len(df)+1)
dendrogram(z,labels=labels)
plt.xlabel("Student ID")
plt.ylabel("Marks")
plt.show()

```

## Output:

![377362348-22390058-6bd8-45d7-a323-89a462d02921](https://github.com/user-attachments/assets/e23a41dc-2d0c-4164-ae07-2918acb4189c)

![377362431-5d9bb049-6277-431d-9d57-ee900df3f4cd](https://github.com/user-attachments/assets/d741e35b-7e9a-4a2a-bc73-f7f0221cb894)
![377362566-897cde68-ccca-4060-b84a-ba9a450b696a](https://github.com/user-attachments/assets/90f5acf1-bc45-4305-8599-2ce144324b3c)
![377362717-407e8271-2014-4ae0-8995-996087deb2bc](https://github.com/user-attachments/assets/4c090265-b6a8-4add-a49e-1977008dff9b)
![377362906-591d5a66-5b1d-4f13-8363-2ff5d9d39ff6](https://github.com/user-attachments/assets/f71ab279-258d-4392-8708-4d7b4262c243)
![377363251-367b45e9-6f57-409c-82d5-5840460e31b9](https://github.com/user-attachments/assets/b69e799d-88ed-4a77-8e77-002f97d7f0cf)






## Result:
Thus the implementation of Hierarchical Clustering using single and complete linkage method in python programming and verified successfully.
