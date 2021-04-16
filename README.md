import random
print("welcome to riddles")
s=0
b={}
with open ("riddles.txt","r")as f:
    ques=f.readlines()
    for c in ques:
        q,a=c.strip().split(":")
        b[q]=a
print()
print("Max. ques are five")
print("for the correct ans your mark will be 2")
print("for the wronge ans your mark will be -1")
d=0
ques=list(b.keys())
random.shuffle(ques)
for g in ques:
    print(g)
    h=input("enter your answer:")
    if h.lower()==b[g].lower():
        s+=2
        print("correct answer")
    else :
        print("your answer is wrong")
        print("the correct answer is:",b[g])
        s-=-1
    print("your score is:",s)
    d+=1
    if d==5:
        break
print("your total score is:",s)
