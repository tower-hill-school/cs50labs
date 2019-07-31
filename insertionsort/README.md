# Insertion Sort

In this lab you will learn about:

- How insertion sort works
- Computational Complexity

## What is Insertion Sort?

Another sorting algorithm that again has different trade-offs is **insertion sort**. Rather than multiple iterations over the list, **insertion sort** splits the array into two parts: a sorted portion and an unsorted portion. It builds the sorted portion one element at a time by looking at each element in the unsorted portion and **inserting** it into the sorted portion of the array.

<!--<img src="http://labs.cs50nestm.net/bubblesort.gif" width="450">-->
## INSERTION SORT ANIMATION TO COME

While this can be relatively efficient for small arrays, the trade-off for larger arrays is that many elements must be shifted around to created the sorted portion of the array.

{% next %}

The pseudocode for **insertion sort** would look like this:

```
for i from 1 to n-1
    call 0'th through i-1'th elements the "sorted side"
    remove i'th element
    insert it into sorted side in order
```


## Computational Complexity



{% next %}

## Your Turn

Complete the `insertions_sort()` function on the right to sort the supplied array. 

Notice that the insertion sort function has a return type of `void`. This means the function doesn't return anything. What it does do is sort the array.

The `print_array()` function is given to you to print out the array after you've sorted it, to make sure your algorithm works properly.

{% spoiler "Hint" %}

1. You might want to start this by simply using an outer `for` loop that begins at `i = 1` and iterates through to the end of the array.
2. Since we assume that elements up to arr[i - 1] are sorted, and arr[i] is the next unsorted element of the array, you might temporarily store the value of arr[i] in a new variable for use later on (`element = arr[i]`). Since we'll be moving through the sorted portion of the array to see where the variable `elemement` will fit in, save the current index, `i` in a new variable `j`.
3. Now, while `j > 0 && arr[j - 1] > element`, the element needs to keep moving to the left, and the values in the sorted portion of the array need to shift one space to the right. You can shift a value to the right by setting it's value to the value of the element one space to the left, `arr[j] = arr[j - 1]`. Now decrease `j` by one to look at the next element in the next iteration of your `while` loop.
4. Finally when this condition is no longer true, you've found the correct spot in the sorted portion of the array for `element`. You can now set it's value into the proper spot in the sorted array, arr[j] = element.
{% endspoiler %}





[Download our CS50 Reference sheet on Insertion Sort](https://ap.cs50.school/assets/pdfs/unit3/insertion_sort.pdf)