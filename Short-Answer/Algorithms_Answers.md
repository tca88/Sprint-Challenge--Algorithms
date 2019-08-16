Add your answers to the Algorithms exercises here.

##Exercise 1a

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

###ANSWER
This would be O(n), and an algorithm with a linear runtime based on the sample size inputted (n) while the sample size to the power of 3 (n _ n _ n) is greater than a.

##Exercise 1b

```
b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```

###ANSWER
This would be O(n^3), as the algorithm involves a nested iteration of the dataset, where the first 3 loops run in a way where the outer most loop runs n times, and and our 2nd inner loop runs n times for each iteration of the outer-most loop, and the 3rd inner loop runs n times for each iteration of the 2nd outer loop.

##Exercise 1c

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

###ANSWER
This would be O(n), where the algorithm would have a linear runtime and loop based on the input given.

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

###ANSWER
Binary Search would work to solve this problem, as we can break it out as within that _n_-story building, eggs will break on floors _f_ and higher, and eggs won't break on floor _f_ and lower. So,

I would first find the middle floor and break into top, middle and lower floors.

Then I would check throwing the egg from the middle floor and IF it breaks, find the middle floor of the lower floors and then throw the egg from that floor, and if that breaks, find the new middle floor of the new lower range, and keep repeating until a floor is found where the egg doesn't break.

ELSE if the egg doesn't break, then find middle floor of top floors and then throw an egg from that floor, and if the egg doesn't break from that floor then again keep dividing and testing until the egg breaks on that floor in the upper bound.

Step 2 and 3 will repeat until we find right floor. The runtime complexity would be O(log n).
