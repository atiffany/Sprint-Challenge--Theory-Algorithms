_I should start by saying I'm not certain of any of these at all_

## Exercise I
a. O(N)
    linear growth of adding n^2 to a count repeatedly
b. O(log N)
    halves a set each time, growth starts large, decreases quickly
c. O(N^3)
    Triple nested for loop
d. O(N^2)
    nested for loop
e. O(N^4)
    Quad nested for loop
f. O(N)
    This recursion is similar to an iterative for loop in terms of Big O
g. O(N)
    Again, this recursion is an iteration over the list through each item. Best possible outcome is O(1)--if the first item sent is the correct one, otherwise worst outcome I think is O(N)

## Exercise II
a. 
int maxNum = 0;
for (int i = 0; i < n-1; i++ )
{
    int j = i + 1;
    if (maxNum = 0)
    {
        maxNum = a[j]-a[i];  
    }
    else
    {
        maxNum = max(maxNum, a[j]-a[i]);
    }
    j++
}
_this should have a big O of O(N), as it iterates through the array 1x

b. My strategy is to try for O(log N). Toss an egg out at the middle floor. If it breaks, you know your breaking point is somewhere on the first half of the building. Then you can split that half in half, try again, so on and so forth.
Of course, if it doesn't break then you treat the top half of the building the same way and go halfway up the top half, etc.

This works since I have a lot of eggs.

Even if I only have two eggs, going to the middle floor seems like a pretty good way to start, because it tells you what half you will need to iterate over, so you can save half your workload.

## Exercise III
a. A quicksort is always going to iterate over every element in the array. If the array is already sorted, and if we choose the first item as the pivot we get really poor performance. We have to recurse for each item in the sorted array. In an unsorted array there is a difference based on the pivot that you choose in order to make it more efficient.

b. If you randomly choose a pivot, your run time may be altered from one run to the next. Choosing the first item makes your quicksort inefficient.
