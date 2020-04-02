# sumOf2DHourGlassArrays


This project is my solution to a challenge which was to write a program that takes an input of a 6X6 2 dimensional array and give the set containing the highest sum of all digits that could be added together in an hourglass shape. An example of this array is below:
101010
101010
101010
101010
101010
101010

The hourglass shape is as so:
abc
 d
efg

Going through the array from left to right we will find this first hourglass shape:
101
  0
101
The sum of this first set equals 4.

Notice that within the 2D array there are 4 iterations of hourglass shapes that can be found when traversing from left to right and 12 more iterations when following the same algorithm from top to bottom. This will give a total of 16 hourglass shapes that can be found.

My method of solving this challenge utilizes 4 functions—hourGlassSum (the main method that calls on sumOfHourglass), sumOfHourglass (which calls on the remaining two functions), sumOf3 and sumOf1. 

We iterate through the 2D array first left to right adding the sum within an hourglass shape to the master list. We utilize a counter to increment the index of the row until we reach the -1 index. We then increment the columns counter by one to begin a new iteration from left to right on the next column down and repeat until we iterate through all 16 hourglass shapes. We will reset the column counter to 0 when we iterate to the next row. We pass the column and row counters to the other functions in order to correctly iterate through the hourglass shape throughout the entire 2D array. 

When we feed the array and counters to sumOfHourglass it will increment a counter of the total sum of numbers found through calling somOf3 which adds up the first 3 numbers within the scope of the index that is defined by the column and row counters it is given. 

sumOfHourglass then calls sumOf1 (incrementing the row counter by one) 

followed by sumOf3 again (incrementing the row counter by two)

We return the total sum of each set to the master list.

After every iteration of hourglasses we return the maximum number found within the master list.

