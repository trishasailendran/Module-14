# Exp No: 14b  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM

```
#Reg.NO 212222060280
#Name Trisha
class Queue:
    def __init__(self,limit):
        self.queue=[]
        self.rear=0
        self.front=0
        self.limit=limit
    def isempty(self):
        if len(self.queue)==0:
            return True
        else:
            return False
    def enqueue(self,item):
        if len(self.queue)==self.limit:
            print("The queue is full")
        else:
            if self.front==self.limit:
                self.front=self.rear-1
            self.queue.insert(self.front,item)
            self.front+=1
    def dequeue(self):
        if self.rear==self.limit:
            self.rear=0
        self.queue.pop(self.rear)
        self.rear+=1
    def display(self):
        print(self.queue)
size=int(input())
a=Queue(size)
str=int(input())
str1=int(input())
str2=int(input())
a.enqueue(str)
a.enqueue(str1)
a.enqueue(str2)
a.display()
a.dequeue()
a.display()



```

### OUTPUT

<img width="820" height="329" alt="image" src="https://github.com/user-attachments/assets/f9d60abf-00e4-42de-b2c2-5f3f9dd2ed56" />

### RESULT
Thus the Circular Queue is implemented and verified successfully.
