sen = " Data structures and Algorithmns are important in problem soving"
# a code to count the number of words in a sentence
count = sen.split()# splits the sen into words
print(len(count)) # counts the words present

sen = " Data structures and Algorithmns are important in problem soving"
# a code to count the number of words in a sentence
count = sen.split()# splits the sen into words
reversed = count[::-1]
print(reversed)

sen = " Data structures and Algorithmns are important in problem soving"
# replacing the word
new_sen = sen.replace("important", "essential")
print(new_sen)

list1 = [21, 10, 45, 32, 67, 5, 18]
list1.sort()  # sorting the list to prepare for binary search
target1 = int(input("Enter target value to search: "))

def binary_search(list1, target1):
    low = 0 # initialize left pointer
    high = len(list1) - 1 # initialize right pointer
 while low <= high: # continue searching while left pointer is less than or equal to right pointer else if only < the target is not found
        mid = (low + high) // 2  # find middle index
        if list1[mid] == target1:
            print(f"{target1} found at index", mid) 
            return True  # target found
        elif list1[mid] < target1: # target is in the right half so we move the low pointer UP by one it means discarding the left half
            low = mid + 1  # search in right half
        else:        # target is to the left of the  mid so the we move the high pointer DOWN by one meaning discarding the right half
            high = mid - 1  # search in left half
    return False  # target not found

result1 = binary_search(list1, target1)
print(result1)

def linear_search(num, key): # this function performs linear search on the list 'num' to find the 'key' value
    for index in range(len(num)):
        if num[index] == key:# check if the current element matches the key value it start comparing from index 0 to the last index of the list
            print(f"{key} found in index", index) # if the key is found in the list, print "Key found" along with the index where it was found
            break # exit the loop once the key is found
    else: # this else corresponds to the for loop, it executes if the loop completes without a break or if the key value is not found in the list
        print("Key not found")

list1 = [21, 10, 45, 32, 67, 5, 18]
key = int(input("Enter key value to serach: "))
linear_search(list1, key) #    

arr = [21, 10, 45, 32, 67, 5, 18]
n = len(arr)
for i in range(n-1): # i is assumed to be the first element in the 
    for j in range(n-i-1):
        if arr[j] > arr[j+1]:
            arr[j], arr[j+1] = arr[j+1], arr[j]
print("bubble sorted array", arr)     
# the time complexity is O(N^2)      

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class LinkedList:
    def LinkedList(self):
        self.head = None
    # inserting a node at the start
    def insert_at_beginning(self,data):
            New = Node(data)  # creating a new node  using the node class
            New.next =  self.head #the new node = head because  the next node will be the head of the previous node
            self.head = New 
 def insert_end(self,data):
        New = Node(data) # creating a new node object from the node  class
        if self.head is None:
            self.head =New
        else:
            n = self.head # creating a variable for the head of the last node (n represents the node)
            while n.next is not None:
                n = n.next
            n.next = New
    # display operation
    def display(self):
        if self.head is None:
            print("SingleLinkedList is empty")
        else:
            n = self.head
            while n is not None:
                print(n.data, end=" -> ")
                n = n.next
            print("None")
            # creating a linked list object
sll = LinkedList()
node1 = Node(9)
node2 = Node(10)
node3 = Node(18)
node4 = Node(12)
node5 = Node(25)

# linking the nodes (link all nodes first)
sll.head = node1
node1.next = node2
node2.next = node3
node3.next = node4
node4.next = node5
node5.next = None

# display before insertion
sll.display()

# insert a node at index 3 with data 20

sll.insert_at_beginning(13)
sll.insert_end(30)
sll.display()


from collections import deque
queue = deque()
queue.append('John')
queue.append('Sharon')
queue.append('stella')
queue.append('Mercy')
print(queue)


queue.popleft() # Remove 'John' from the front of the queue the first student
print(queue)

queue.append("Mufasa")
print(queue)


