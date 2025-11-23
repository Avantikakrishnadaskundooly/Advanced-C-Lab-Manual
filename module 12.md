

# EXP NO 26: C PROGRAM TO DISPLAY STACK ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display stack elements using linked list.

## Algorithm:
1.	Define a structure Node with two members: data to store the integer value and next to point to the next node in the linked list.
2.	Declare a global variable head representing the starting node of the linked list.
3.	Define a function display to print the elements of the linked list.
4.	Declare a pointer p and initialize it with the head of the linked list.
5.	Use a while loop to traverse the linked list:
6.	Print the data of the current node.
7.	Move to the next node using the next pointer.
 
## Program:
```
struct Node{  
    char data[100];  
    struct Node *next;  
}*head; 

void display(){
    struct Node *temp=head;
    while(temp!=NULL){
        printf("%s\n",temp->data);
        temp=temp->next;
    }
}
```

## Output:
<img width="1192" height="600" alt="image" src="https://github.com/user-attachments/assets/831ab022-98ed-4af1-b011-10d1e39b9652" />



## Result:
Thus, the program to display stack elements using linked list is verified successfully. 



# EXP.NO 27: C PROGRAM TO POP AN ELEMENT FROM THE GIVEN STACK USING LINKED LIST.
## Aim:
To write a C program to pop an element from the given stack using liked list.

## Algorithm:
1.	Check for Empty Stack
2.	If head is equal to NULL, Print "Stack is empty."
3.	Else Proceed to the next step.
4.	Set head to point to the next node in the stack.
 
## Program:
```
struct Node{  
    int data;  
    struct Node *next;  
}*head;  
void pop(){
    struct Node *temp=head;
    if(head==NULL){
        printf("stack is empty\n");
    }else{
        head=temp->next;
        free(temp);
    }
}
```

## Output:
<img width="1193" height="725" alt="image" src="https://github.com/user-attachments/assets/eff5c9bf-a065-44c3-9ff9-a05f1ac9b530" />




## Result:
Thus, the program to pop an element from the given stack using liked list is verified successfully.

 
# EXP NO:28 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING LINKED LIST.
## Aim:
To write a C program to display queue elements using linked list.
## Algorithm:
1.	Check if Queue is Empty
2.	Display Queue Elements
3.	Print the data of the current node pointed to by front
4.	Update front to point to the next node.
5.	End the display function.
 
## Program:
```
struct Node{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void display(){
    if(front==NULL){
        printf("queue is empty\n");
    }else{
        printf("Queue elements:\n");
        struct Node *temp=front;
        while(temp!=NULL){
            printf("%.3f\n",temp->data);
            temp=temp->next;
        }
    }
}
```


## Output:
<img width="1195" height="647" alt="image" src="https://github.com/user-attachments/assets/222c3259-7b6a-40e3-be54-f61ab1287669" />


## Result:
Thus, the program to display queue elements using linked list is verified successfully.


 
# EXP NO:29 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING LINKED LIST

## Aim:
To write a C program to insert elements in queue using linked list

## Algorithm:
1.	Allocate Memory for New Node
2.	Set Data and Next Pointer
3.	Check if Queue is Empty
4.	Set both front and rear to point to the new node p.
5.	Set the next pointer of the current rear to point to the new node p.
6.	End of Enqueue Operation
 
## Program:
```
struct Node{
   int data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void enqueue(int data){
    struct Node *temp=(struct Node*)malloc(sizeof(struct Node));
    temp->data=data;
    temp->next=NULL;
    if(rear==NULL){
        front=rear=temp;
    }else{
        rear->next=temp;
        rear=temp;
    }
}
```


## Output:
<img width="1194" height="565" alt="image" src="https://github.com/user-attachments/assets/96415d8d-9a29-4469-86eb-cebdde7c6c07" />



## Result:
Thus, the program to insert elements in queue using linked list is verified successfully.



# EXP NO:30 C FUNCTION TO FIND THE PEEK OF QUEUE USING LINKED LIST.


## Aim:

The aim of this function is to retrieve the "peek" (the front element) of a queue implemented using a linked list

## Algorithm:

1.	Check if the queue is empty:
o	If the queue is empty (i.e., the front pointer is NULL), return an error or a message indicating that the queue is empty.
2.	Access the front element:
o	If the queue is not empty, return the data stored in the front node of the linked list (i.e., the element at the head of the queue).

## Program:
```
struct Node{
   float data;
   struct Node *next;
}*front=NULL,*rear=NULL;
void peek(){
    printf("%.2f",front->data);
}
```

## Output:
<img width="1195" height="674" alt="image" src="https://github.com/user-attachments/assets/ddc96451-f812-486e-85ff-82b1072762ad" />




## Result:

Thus, the program to retrieve the "peek" (the front element) of a queue implemented using a linked list is verified successfully.


