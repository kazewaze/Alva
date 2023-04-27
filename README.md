![Alva Logo](alva.png)

### A Zero Dependency Deep Learning Toolkit for composing datasets.

```py
alv = Alva()

# Code from Andrew Trask's Book "Grokking Deep Learning" below:

weights = [0.1, 0.2, 0]

# games: 1st  2nd  3rd  4th
toes =  [8.5, 9.5, 9.9, 9.0] # toes
wlrec = [0.65, 0.8, 0.8, 0.9] # win / loss record
nfans = [1.2, 1.3, 0.5, 1.0] # number of fans

input = alv.build_input(toes, wlrec, nfans) # Pass in the data points.

#                             Results for:
calc1 = input.dot(0, weights) # First game
calc2 = input.dot(1, weights) # Second game
calc3 = input.dot(2, weights) # Third game
calc4 = input.dot(3, weights) # Fourth game

results = alv.show_results([calc1, calc2, calc3, calc4]) # Print the results of each game.

arr = alv.array([[1, 2, 3], # (3, 3)
                 [4, 5, 6],
                 [7, 8, 9]])

matrix = alv.zeros((3, 3)) # (3, 3) matrix of 0's

shape = arr.shape()

print(shape)
print(results)
print(matrix)
```