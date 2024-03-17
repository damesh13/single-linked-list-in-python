# create-single-linked-list-l
#hiiii everyone in this repository i am creating single linked list in python programming language and i am also displaying the inserted elements in the linked list 
class node:
    def __init__(self,value):
        self.value=value
        self.next=None

class single_linked_list:
    def __init__(self):
        self.head=None

    def create(self,value):
        newnode=node(value)
        if self.head ==None:
            print("\ncreating a new linked list ")
            self.head=newnode
        else:
            print("\nlist is already created so adding this number to the list ")

            temp=self.head
            while temp.next!=None:
                temp=temp.next
            temp.next=newnode
    def display(self):
        temp=self.head
        if temp==None:
            print("\nno list is present ")
        else:
            while temp!=None:
                print(temp.value)
                temp=temp.next

obj=single_linked_list()
while True:
    n=int(input("1.to create the linked list 2.to display the linked list 3.to exit from the program",))
    if n==1:
        value=int(input("enter the number "))
        obj.create(value)
    elif n==2:
        obj.display()
    else:
        break

