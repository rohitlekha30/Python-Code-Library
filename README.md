name1=input("Enter the first name - ")
name2=input("Enter the second name - ")

len1=len(name1)
len2=len(name2)
count=0
matchcount=0

if len1==len2:
    for i in range(0,len1) :
        print(f"Going to match {name1[i]}") 
        count=0
        for j in range(0,len2)  :
            if name1[i]==name2[j]:
                print(f"{name1[i]} is matched at position {j} in {name2}")
                count+=1
                matchcount+=1
                break
        if count==0:
            print(f"{name1[i]} is not matched in {name2}")

    print(f"matchcount= {matchcount}")
    if matchcount==len1:
        print(f"{name1} and {name2} are Anagramm")
    else:
        print("Sorry not Anagram")
else:
    print("As Length is not equal, so no comparision is done")
