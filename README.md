# string-is-a-palindrome-or-not.-
class Stack:
    def   __init__(self):
        self.items = []
 
    def empty(self):
        return self.items == []
 
    def push(self, data):
        self.items.append(data)
 
    def pop(self):
        return self.items.pop()
stck = Stack()
text = input('ENTER YOUR STRING : ')
for char in text:
    stck.push(char)
    reverse_text = ''
while not stck.empty():
    reverse_text = reverse_text + stck.pop()
 
if text == reverse_text:
    print('THIS STRING IS A PALINDROME.')
else:
    print('THIS STRING IS NOT A PALINDROME.')
