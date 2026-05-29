# Series Queues with infinite capacity - Open Jackson Network

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory

![image](https://user-images.githubusercontent.com/103921593/203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54.png)


## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203239789-bc870dce-6727-487b-a0e2-4fc3f5114889.png)

## Program
```
arr=float(input("Enter mean arrival time : "))
s1=float(input("ENter the mean serive1 time : "))
s2=float(input("Enter the mean service2 time : "))
s3=float(input("Enter the mean service3 time : "))

s=float(input("Enter the mean service time : "))

lam=1/arr
mu1=1/(s1+s)
mu2=1/(s2+s)
mu3=1/(s3+s)

print(f"Arrival rate : {lam:.3f}")
print(f"Service rate1 : {mu1:.3f}")
print(f"Service rate2  : {mu2:.3f}")
print(f"Service Rate3  : {mu3:.3f}")

if mu1>lam and mu2>lam and mu3>lam:
  Ls1=lam/(mu1-lam)
  Ls2=lam/(mu2-lam)
  Ls3=lam/(mu3-lam)

  Lq1=Ls1-(lam/mu1)
  Lq2=Ls2-(lam/mu2)
  Lq3=Ls3-(lam/mu3)

  Ls=Ls1+Ls2+Ls3

  Wq1=Lq1/lam
  Wq2=Lq2/lam
  Wq3=Lq3/lam

  Ws=Ls/lam

  print(f"Ls1 : {Ls1:.4f}")
  print(f"Ls2 : {Ls2:.4f}")
  print(f"Ls3 : {Ls3:.4f}")

  print(f"Lq1 : {Lq1:.4f}")
  print(f"Lq2 : {Lq2:.4f}")
  print(f"Lq3 : {Lq3:.4f}")

  print(f"Ws : {Ws:.4f}")



```

## Output

<img width="426" height="314" alt="image" src="https://github.com/user-attachments/assets/9f9acc0e-6297-4cda-b962-d220c343496c" />

## Result

The arrival rate, service rates, average number of objects in each system, average number of objects in each conveyor, and average waiting time in the system are calculated successfully using Python.
