# <a name="Loops"></a>Loops
* [While Loop](#While-Loop)
* [For Loop](#For-Loop)

### <a name="While-Loop"></a>While Loop
* A while loop is used to repeat a block of code multiple times.
For example, let's say we need to process multiple user inputs, so that each time the user inputs something, the same block of code needs to execute.

Below is a while loop containing a variable that counts up from 1 to 5, at which point the loop terminates.
### Example Program
```i = 1
while i <=5:
   print(i)
   i = i + 1

print("Finished!")
```
### Output
```
1
2
3
4
5
Finished!
```

* During each loop iteration, the i variable will get incremented by one, until it reaches 5. So, the loop will execute the print statement 5 times.
* The code in the body of a while loop is executed repeatedly. This is called iteration.
*You can use multiple statements in the while loop. For example, you can use an if statement to make decisions. This can be useful, if you are making a game and need to loop through a number of player actions and add or remove points of the player. The code below uses an if/else statement inside a while loop to separate the even and odd numbers in the range of 1 to 10:

### Example Program
```
x = 1
while x < 10:
  if x%2 == 0:
    print(str(x) + " is even")
  else:
    print(str(x) + " is odd")

  x += 1 
  ```
### Output
  ```
  1 is odd
2 is even
3 is odd
4 is even
5 is odd
6 is even
7 is odd
8 is even
9 is odd
```
* str(x) is used to convert the number x to a string, so that it can be used for concatenation.
### break
* To end a while loop prematurely, the break statement can be used. For example, we can break an infinite loop if some condition is met:
```
i = 0
while True:
  print(i)
  i = i + 1
  if i >= 5:
    print("Breaking")
    break

print("Finished")
```
### Output
```
0
1
2
3
4
Breaking
Finished
```
* while True is a short and easy way to make an infinite loop.

* An example use case of break:
* An infinite while loop can be used to continuously take user input. For example, you are making a calculator and need to take numbers from the user to add and stop, when the user enters "stop". In this case, the break statement can be used to end the infinite loop when the user input equals "stop". Using the break statement outside of a loop causes an error.
### continue
* Another statement that can be used within loops is continue. Unlike break, continue jumps back to the top of the loop, rather than stopping it. Basically, the continue statement stops the current iteration and continues with the next one.
### For example:
```
i = 1
while i<=5:
    print(i)
    i+=1
    if i==3:
      print("Skipping 3")
      continue
  ```
 ### Output
 1
Skipping 2
3
4
Breaking
Finished

* An example use case of continue:
* An airline ticketing system needs to calculate the total cost for all tickets purchased. The tickets for children under the age of 1 are free. We can use a while loop to iterate through the list of passengers and calculate the total cost of their tickets. Here, the continue statement can be used to skip the children.

### for Loop
* The for loop is used to iterate over a given sequence, such as lists or strings.

* The code below outputs each item in the list and adds an exclamation mark at the end:
```
words = ["hello", "world", "spam", "eggs"]
for word in words:
  print(word + "!")
  ```
  ### Output
  ```
  hello!
world!
spam!
eggs!
```
* In the code above, the word variable represents the corresponding item of the list in each iteration of the loop.
* During the 1st iteration, word is equal to "hello", and during the 2nd iteration it's equal to "world", and so on.
### <a name="For-Loop"></a>for Loops
* The for loop can be used to iterate over strings.
### For example:
```
str = "testing for loops"
count = 0

for x in str:
  if(x == 't'):
    count += 1

print(count) 
```
### Output
```
2
```
* The code above defines a count variable, iterates over the string and calculates the count of 't' letters in it. During each iteration, the x variable represents the current letter of the string. The count variable is incremented each time the letter 't' is found, thus, at the end of the loop it represents the number of 't' letters in the string.
* Similar to while loops, the break and continue statements can be used in for loops, to stop the loop or jump to the next iteration.
### for vs while
* Both, for and while loops can be used to execute a block of code for multiple times.

* It is common to use the for loop when the number of iterations is fixed. For example, iterating over a fixed list of items in a shopping list.

* The while loop is used in cases when the number of iterations is not known and depends on some calculations and conditions in the code block of the loop.
* For example, ending the loop when the user enters a specific input in a calculator program.

* Both, for and while loops can be used to achieve the same results, however, the for loop has cleaner and shorter syntax, making it a better choice in most cases.
