# repeating-a-character-in-string-as-vc-cc-wc
#problem1=repeating charachter in string    
#approach1
'''
s=input()
c=1
r=""
for i in range(1,len(s)):
  if s[i] == s[i-1]:
    c=c+1
  else:
    r=r+s[i-1]+str(c)
    c=1
r=r+s[len(s)-1]+str(c)
print(r)


#first repeating charachter
#approach2
t=int(input())
for _ in range(t):
  s=input()
  for i in range(len(s)):
      if s[i] in s[i+1:]:
        print(s[i])
        break
  else:
    print(".")
    
  
#problem3=count of vowels,words,consonants in string
#approach1
a=input().split()
wc=len(a)
vc=0
cc=0
v="aeiouAEIOU"
for i in a:
  for j in i:
    if j.isalpha():
      if j in v:
        vc=vc+1
      else:
        cc=cc+1
print(wc,vc,cc) 

'''
#approach2
t=int(input())
v="aeiouAEIOU"
for _ in range(t):
  s=input()
  vc=0
  cc=0
  for i in s:
    if i.isalpha():
      if i in v:
        vc=vc+1
      else:
        cc=cc+1
  a=s.split()
  wc=len(a)
  print(wc,vc,cc)
