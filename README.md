A begginer's guide to Counting sort
- This is ONE of a series made to be helpful to newbs in the Data struuctures and algorithms, to help them grasp the algorithms
  and its intuitions, i hope you find it helpful, if you want any more clarification or an algorithm to be broken down by me in this
  style just send a mail, thanks a lot for checking this.
  
- This algorithm's basic idea is counting how many times a certain number is repeated, then it saves the numbers in order by how
  many times they are repeated, like if the counting array is {0, 1, 1,3,1}, the array will be {2, 3, 4, 4, 4, 5}, if you start counting
  from 1 in the coutning array, then the 1 is repeated 0 times, 2 is repeated 1 time, also 3, then 4 is repeated 3 times, then 5 
  is repeated 1 time, so you use the index to count the numbers by how many times they are repeated then write the numbers in the original
  array. A note here, sometimes the counting array starts from 0 not 1, so make sure of the starting point.
- As you probably figured out, this algorithm does not compare values in the array with each other.
- This algorithm needs to make assumptions about the data, in the implementation it needs to know the maximum and minimum values in the array.
- A drawback in this algorithm is that it needs to work in a range, like from 0 to 5000.
- Another drawback is that it needs to not use it if there is a huge diversity in the numbers in an array, like if an array has 10 items,
  and those items range from 9 to 99999, then this algorithm is really bad to use, because it uses the index of a temporary array to store
  the occurrences of values, so it will make a new array of size 99999 to store only 10 items.
- Not a stable algorithm, it could be made stable but some extra steps will be needed.
- It is not an in-place algorithm, it needs another array to count the occurrences of numbers, so it will need extra memory.
- O(N), because it traverses the array once to count the numbers' occurrences.
