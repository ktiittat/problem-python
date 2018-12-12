# problem-python
โจท์หาเลขที่ มีจำนวนซ้ำกันมากที่สุด 
input : 3
       4 5 5
output : 5
#####
import numpy as np
n = int(input())
my_list = list(map(int,input().split()))
arr = np.array(my_list)
sort_list =np.sort(arr)
max_count = 1
res = arr[0]
curr_count = 1
for i in range(n):
    if  sort_list[i] == sort_list[i-1] :
        curr_count = curr_count +1
    else:
        if curr_count>max_count:
            max_count=curr_count
            res = sort_list[i-1]
        curr_count=1
if curr_count>max_count:
    max_count=curr_count
    res = sort_list[i-1]
print(res)
#######
