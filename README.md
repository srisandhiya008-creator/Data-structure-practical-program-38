# SINGLY LINKED LIST
print("Singly Linked List (Playlist)")

class Node:
    def __init__(self,data):
        self.data=data
        self.next=None

head=Node("Song1")
head.next=Node("Song2")
head.next.next=Node("Song3")

temp=head
while temp:
    print(temp.data,end=" -> ")
    temp=temp.next
print("None")


# DOUBLY LINKED LIST
print("\nDoubly Linked List (Playlist)")

class DNode:
    def __init__(self,data):
        self.data=data
        self.prev=None
        self.next=None

d1=DNode("SongA")
d2=DNode("SongB")
d3=DNode("SongC")

d1.next=d2
d2.prev=d1
d2.next=d3
d3.prev=d2

temp=d1
while temp:
    print(temp.data,end=" <-> ")
    temp=temp.next
print("None")


# CIRCULAR LINKED LIST
print("\nCircular Linked List (Playlist)")

class CNode:
    def __init__(self,data):
        self.data=data
        self.next=None

c1=CNode("Track1")
c2=CNode("Track2")
c3=CNode("Track3")

c1.next=c2
c2.next=c3
c3.next=c1   # circular link

temp=c1
for i in range(3):
    print(temp.data,end=" -> ")
    temp=temp.next
print("(Back to Start)")# Data-structure-practical-program-38
