#input number of testcases
for i in range(int(input())):
    #input number of elemrnts in an array
    s=int(input())
    #input the elements
    n=input().split()
    n=[int(i) for i in n]
    m=n[0]
    k=0
    #remove the elements from right until first max
    for i in range(len(n)-1):
        z=n[i]-n[i+1]
        if z<0:
            m=n[i+1]
            k=i+1
    l=0
    #find max element in the array
    max_element=max(n)
    #get the position of the max element from the left
    for i in range(k+1):
        if n[i]==max_element:
            max_element_lpos=i
            break
    #get the position of the max element from the right 
    for i in range(k,-1,-1):
        if n[i]==max_element:
            max_element_rpos=i
            break
    #let mx be the first element and update mx with the next large element untill max_element from left subtract mx with the
    #present element
    mx=n[0]
    for i in range(max_element_lpos):
        x=mx-n[i]
        if x>0:
            l=l+x
        else:
            mx=n[i]
    #here do the same thing from the right untill max_element
    mx=n[k]
    for i in range(k,max_element_rpos,-1):
        x=mx-n[i]
        if x>0:
            l=l+x
        else:
            mx=n[i]
    #if there are multiple max_elements from left max_element to right max_element subtract the middle elements with
    #max_element
    if max_element_lpos!=max_element_rpos:
        for i in range(max_element_lpos+1,max_element_rpos):
            l=l+max_element-n[i]
    print(l)
