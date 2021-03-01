f=open('text.txt','r')
f1=open('output.txt','w')
for line in f.readlines():
  #запись в переменные по словам с разделением на пробелы в файле
  a,b,c=map(float,line.split(' '))
  print('a=',a,'b=',b,'c=',c)
  D=b**2-4*a*c
  print("D=",D)
  if D<0:
    print("Нет решений D<0\n")
    s='a='+str(a)+' b='+str(b)+' c='+str(c)+' Нет решений D<0'
  elif D==0:
    x1=(-b)/(2*a)
    x1=round(x1,2)
    print("x=",x1,'\n')
    s='a='+str(a)+' b='+str(b)+' c='+str(c)+' x='+str(x1)
  else:
    x1=((-b)+D**(1/2))/(2*a)
    x2=((-b)-D**(1/2))/(2*a)
    x1=round(x1,2)
    x2=round(x2,2)
    print("x1=",x1)
    print("x2=",x2,'\n')
    s='a='+str(a)+' b='+str(b)+' c='+str(c)+' x1='+str(x1)+' x2='+str(x2)
  f1.write(s+'\n');
f.close()
f1.close()
