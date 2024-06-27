a=np.array([1, 6, 3, 0, 8, 4, 1, 7])
s=7
t=[]
for i in range(len(a)):
    for j in range(i+1,len(a)):
        for k in range(j+1,len(a)):
            if a[i]+a[j]+a[k]==s:
                t.append((a[i],a[j],a[k]))
s=set()
for i in range(len(t)-1):
    for j in range(i+1,len(t)):
        if set(t[i]).issubset(set(t[j])):
            s.add(t[i])
t=set(t)
t=t-s
print(t)
