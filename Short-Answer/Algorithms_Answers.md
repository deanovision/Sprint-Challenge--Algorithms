    a)  a = 0
    while (a < n * n * n):
      a = a + n * n

#### This is O(1) the function seems to only perform one operation regardless of input

b) sum = 0
for i in range(n):
i += 1
for j in range(i + 1, n):
j += 1
for k in range(j + 1, n):
k += 1
for l in range(k + 1, 10 + k):
l += 1
sum += 1

#### This is O(n^4) there is one outer loop plus 3 nested loops that all depend on n

c) def bunnyEars(bunnies):
if bunnies == 0:
return 0

      return 2 + bunnyEars(bunnies-1)

#### This is O(n) the number of n will be 1:1 with the number of recursive calls to this function

Suppose that you have an n-story building and plenty of eggs.
Suppose also that an egg gets broken if it is thrown off floor f or higher,
and doesn't get broken if dropped off a floor less than floor f.
Devise a strategy to determine the value of f such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

store current floor
move to the middle floor of the building
drop an egg:
if egg breaks:
while egg continue to not break:
move up one floor
update current floor
drop egg
floor f = current floor - 1
if egg breaks:
while egg continues to break:
move down one floor
update current floor
drop egg
floor f = current floor

#### Time complexity is O(n)
