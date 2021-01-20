# Save-List-to-File
### Read the .txt file and save it to the list
### To subsequently reorder the inputs as desired by the user and save them to another .txt file

```python
a=open('students.txt','r')
b=a.readlines()
a.close()

c=[]
for i in b:
  i=i.split()
  t=int(i[-3]+int(i[-2])+int(i[-1]))
  i.append(t)
  del (i[1:-1])
  i[0],i[1] = i[1],i[0]
  c.append(i)
  
c.sort(serve=True)

d=open('students_sorted.txt','w')

for i in c:
  d.write(i[1]+' '+str(i[0])+'\n')
  
d.close()
```
